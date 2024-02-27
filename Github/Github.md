# Github

### Iniciando Repositório no Github a partir dos arquivos do PC

1. git init
2. git add + [Opção]
3. git commit
4. git branch -M + [Nome da Branch]
5. git remote add origin git@github.com:LuizGustavoVTacin/[Nome do Repositorio]
6. git push -u origin [Nome da Branch]

### Sincronizando Repositórios local e Github:

* git push + [Opções]:                               
Envia atualizações ao repositório Github

**Opções**:                                         
* Vazio:                                            
Atualização serão enviadas ap branch principal

* --set-upstream origin master:                     
Envia atualizações para uma branch específica

### Verificando Histórico de commits:

* git reflog:                                       
Exibe histórico de commits

Pressionae **q** para sair

* git reset --hard + [ID do commit]:                    
Retorna o repositório para o conteúdo de determinado commit

### Branchs:

* git branch:                                       
Exibe todas as branchs

* git branch + [Nome da Branch]:                        
Cria uma nova branch

* git checkout + [Opção] + [Nome da Branch] + [Branch Atual]:                                               
Selecionar em qual branch trabalhar

**Opção**:                                      
* -b + [Branch Atual]:                               
Para criar a branch inserida a partir de outra branch

### Atualizar os repositórios local e Github:

* git merge + [Nome da Branch]:                         
Atualizar o conteúdo do branch atual a partir da branch inserida

* git fetch + [Nome da Branch]:                     
Atualiza o repositório com o conteúdo do Github

* git pull:                                         
Importará atualizações da nuvem para o repositório local

* touch .gitignore:                                 
Criará um arquivo de texto para adicionar o nome dos arquivos que não deverão ser enviados.
Cada arquivo não enviado será escrito no arquivo de texto manualmente
