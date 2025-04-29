# Comandos básicos em Bash🐧

## Índice
1. [Comandos de navegação do sistema](#Navegação-do-Sistema)
2. [Manipulação de arquivos e pastas](#Manipulação-de-arquivos-e-pastas)

O terminal Bash é uma interface de linha de comando (CLI) onde podemos executar comandos para controlar o sistema operacional. Ele é um dos shells mais populares e é comumente utilizado em distribuições Linux.

Clique abaixo para acessar a documentação oficial do GNU Bash:
[Manual GNU Bash](https://www.gnu.org/software/bash/manual/bash.html)

Para começar vamos abrir o terminal. Podemos abrir de duas formas:
1. Acessamos o terminal pelo ícone no desktop.
2. Acessamos o terminal pressionando as teclas de atalho _Ctrl + Alt + T_.

![image](https://github.com/user-attachments/assets/96317331-2bce-4091-977f-187af0ab36cb)

## Comandos essenciais

Para você que está começando a utilizar o terminal, é essencial aprender os comandos básicos do GNU Bash, como comandos de navegação, gerenciar arquivos, ver informações do sistema e até automatização de tarefas. Abaixo poderá ver o comando e seu exemplos de uso.

## Navegação do Sistema 

| Comando      | Descrição |
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

Estes comandos 

| Comando | Descrição | Exemplo |
|--------|-----------|---------|
| mkdir | Cria uma nova pasta/diretório | `mkdir fotos` |
| touch | Cria um novo arquivo vazio | `touch nota.txt` |
| cp | Copia arquivo ou diretório (`-r` para diretórios) | `cp nota.txt /home/user/Desktop` |
| rm | Remove arquivo (use `-r` para remover diretórios) | `rm nota.txt` |
| rmdir | Remove diretório vazio | `rmdir fotos` |
| mv | Move ou renomeia arquivos/diretórios | `mv nota.txt /home/user/Documents/` |

> Obs: É recomendado testar esses comandos em algum sistema operacional Linux. Você pode criar e excluir pastas, criar arquivos vazios, navegar pelos diretórios etc. A medida que vai utilizando os comandos, fica mais fácil manipular o sistema.

## Comandos para visualização do conteúdo de arquivos

| Comando | Descrição | Exemplo |
| --------| --------- | ------- |
| cat     | Exibe o conteúdo do arquivo diretamente no terminal | `cat nota.txt` |
| less    | Exibe o conteúdo do arquivo de forma paginada, caso o arquivo for grande | `less nota.txt` |
| head    | Exibe somente as 10 primeiras linhas do arquivo | `head nota.txt` |
| tail    | Exibe somente as 10 últimas linhas do arquivo | `tail nota.txt` |
| tail -f | Exibe o conteudo, e atualiza em tempo real | `tail -f auth.log` |

## Comandos para busca em arquivos

Com esses comandos, você poderá realizar buscas de arquivos, diretórios e padrões de forma prática diretamente no terminal (shell).

| Comando | Descrição | Exemplo 1 | Exemplo 2 |
| ------- | -------- | --------- | --------- |
| grep    | Faz uma busca de um padrão específico em arquivos | grep "date" [caminho do arquivo] | grep "usuário" *.txt |
| egrep   | Busca padrões em arquivos usando expressões regulares, este comando equivale ao egrep -E, já que o mesmo está absoleto. | egrep "palavra" log.txt | egrep "palavra" [caminho1] [caminho2] |
| awk '{print $[coluna]}' | Exibe a uma coluna específica de um arquivo | awk '{print $2}' log.txt | awk '/error/ {print $0}' log.txt |

## Comando de busca em diretórios

| Comando | Descrição | Exemplo 1 | Exemplo 2 |
| ------- | --------- | --------- | --------- |
| find    | Encontrar um arquivo em um diretório específico | find [caminho] --name "*.txt" | find [caminho] -type d -name "lib" |
| locate  | Buscar arquivos e diretórios | locate "dados.csv" | locate log (retorna todos os arquivos e diretórios com log no nome)
| history | Exibe o histórico de comandos | history | - |
| clear   | Limpa o terminal | clear | - |

> Obs: O comando `locate` é uma alternativa do comando `find`, pois ele é mais rápido ao realizar pesquisas. Isso ocorre porque o primeiro apenas verifica seu banco de dados Linux em vez de todo o sistema. Além disso, a sintaxe é relativamente mais fácil de escrever.

Às vezes, o comando `locate` padrão pode retornar arquivos que foram excluídos, se o banco de dados não foi atualizado. A melhor solução é atualizar manualmente o banco de dados executando o seguinte:

```bash
sudo updatedb
```

## Permissões

Os comandos a seguir são comandos que envolve permissões de execução, escrita e leitura no sistema, com base nos grupos e usuários do sistema.

