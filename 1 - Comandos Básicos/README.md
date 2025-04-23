# Comandos básicos em Bash🐧

## Índice
1. [Comandos de navegação do sistema](#Navegação-do-Sistema)
2. [Manipulação de arquivos e pastas](#Manipulação-de-arquivos-e-pastas)

Terminal bash é um programa shell onde podemos executar linhas de comandos e controlar sistemas operacionais, comumente utilizado no Linux.

Clique abaixo para acessar a documentação oficial do GNU Bash:
[Manual GNU Bash](https://www.gnu.org/software/bash/manual/bash.html)

Para começar vamos abrir o terminal. Podemos abrir de duas formas:
- Acessamos o terminal pelo ícone no desktop.
- Acessamos o terminal pressionando as teclas de atalho _Ctrl + Alt + T_.

![image](https://github.com/user-attachments/assets/96317331-2bce-4091-977f-187af0ab36cb)

## Comandos essenciais

Para você que está começando a utilizar o terminal bash, é essencial aprender os comandos básicos do GNU Bash, como comandos de navegação, gerenciar arquivos, ver informações do sistema e até automatização de tarefas.

## Navegação do Sistema 

| Comando      | descrição |
| ----------- | ----------- |
| pwd | Exibe o caminho completo do diretório atual  | 
| ls  | Exibe no terminal os arquivos e pastas do diretório atual |
| cd | Navega entre os diretórios, exemplo: `cd pasta `; `cd ..` (retorna um nível do caminho atual); `cd ~` (Navega para o diretório Home) |

Exemplo Prático:

`pwd`
> ![image](https://github.com/user-attachments/assets/c41b0791-e2cc-4a6f-b799-1be4d6d17f3f)

`ls`
> ![image](https://github.com/user-attachments/assets/405abe07-f298-4074-8992-fb55d5939ae1)

`cd`
> ![image](https://github.com/user-attachments/assets/77b0e59f-0d78-40bc-9e96-c7225197d181)

## Comandos para Manipulação de arquivos e pastas

| Comando | Descrição | Exemplo |
|--------|-----------|---------|
| mkdir | Cria uma nova pasta/diretório | `mkdir fotos` |
| touch | Cria um novo arquivo vazio | `touch nota.txt` |
| cp | Copia arquivo ou diretório (`-r` para diretórios) | `cp nota.txt /home/user/Desktop` |
| rm | Remove arquivo (use `-r` para remover diretórios) | `rm nota.txt` |
| rmdir | Remove diretório vazio | `rmdir fotos` |
| mv | Move ou renomeia arquivos/diretórios | `mv nota.txt /home/user/Documents/` |

> Obs: É recomendado que teste esses comandos em algum sistema operacional Linux. Crie uma pasta e exclua, crie um arquivo vazio.

## Comando para visualização de conteúdo de arquivos

| Comando | Descrição | Exemplo |
| --------| --------- | ------- |
| cat     | Exibe o conteúdo do arquivo diretamente no terminal | `cat nota.txt` |
| less    | Exibe o conteúdo do arquivo de forma paginada, caso o arquivo for grande | `less nota.txt` |
| head    | Exibe somente as 10 primeiras linhas do arquivo | `head nota.txt` |
| tail    | Exibe somente as 10 últimas linhas do arquivo | `tail nota.txt` |
| tail -f | Exibe o conteudo, e atualiza em tempo real | `tail -f auth.log` |

