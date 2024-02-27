# Repositório

### Criar Repositórios:

* git init + [Nome do repositório]:                 
Inicia um repositório dentro de um diretório

* git remote add origin + [URL do repositório]:         
Vincula o repositório criado localmente com o repositório do github

* git clone + [ssh]:                                
Clona o repositório do github localmente, criando o repositório local

### Configurar Repositório:

* git config --global user.email + ["email"]:       
configurar email no repositório

* git config --global user.name + ["nome"]:              
configurar nome de usuário no repositório

### Mudança nos Repositórios:

* git status:                                       
Exibe as mudanças que não foram adicionadas ao versionamento e quais foram

* git add + [Nome do Arquivo]:                      
Adiciona 1 arquivo ao versionamento

* git add . :                                       
Adiciona todos os arquivos ao versionamento

* git reset + [Nome do Arquivo]:
Desfaz o add de um arquivo

* git reset:
Desfaz todos os add

* git commit -m ["Nome do Versionamento"]:          
Cria um novo versionamento

* git rm -r + [Nome do diretório]:                  
Excluir um diretório não vazio

* git mv + [Nome do Diretório] + [Novo Local]:           
Mover arquivo ou diretório

* git add . && git commit --amend --no-edit:
Acrescenta conteudo a um commit