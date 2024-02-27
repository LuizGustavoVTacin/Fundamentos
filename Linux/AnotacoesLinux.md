# Anotações - Linux

## Bash

#### Alterar Saída

* [Comando] > [Arquivo]:

Para alterar a saída do comando em arquivo a ser criado

1. Exemplo:

ls > Teste.txt

#### Alterar Entrada

* [Comando] < [Arquivo]:

Para alterar usar a entrada de um comando dados de outro arquivo

1. Exemplo:

./Crescente.c < Numeros.txt

#### Alterar saída e entrada simultaneamente

1. Exemplo:

./Crescente.c < Numeros.txt > NumerosOrdenados.txt

#### Encadear Comandos (Pipe)

* [Comando] | [Comando]

Designa a saída do primeiro comando na entrada do segundo programa

#### Caracteres Especiais

* \*

Simboliza qualquer número de caracteres variados

1. Exemplo ls lista*: 

Executará o comando ls para os diretórios que começam com lista

* ?

Simboliza qualquer 1 caracter

* []

Simbolizam qualquer caractere que esteja dentro de []

1. Exemplo ls lista[123]: 

Executará o comando para lista1, lista2 e lista3

* {}

Simbolizam qualquer caractere que esteja dentro de {} na ordem

1. Exemplo ls lista{1,3,2}:

Executará ls lista1, lista3 e lista 2 na ordem

## Processos e Jobs

#### ps: 

Lista os processos em execução com numero PID. Processos podem estar em foreground, background e suspenso

* [Comando] + & 

Deixará a ação sendo executada em background

1. Exemplo: ls & 

Se o comando tiver em execução e deseja-se deixá-lo em background, CTRL + X para suspendê-lo e bg para
por em background

#### jobs

Listará os comandos em background

#### fg %numero_do_job

Moverá o processo para foreground. Numero do job é listado em jobs

#### fg

Moverá o último processo em background

#### kill %numero_do_job ou kill %numero_do_PID

Matará o processo

#### Cat

* cat + [Opção] + [Arquivo]

Imprime o conteúdo do arquivo na saída

1. Opções: 

-n para numerar as linhas de saída

#### cd

* cd + [Opção] + [Caminho]

Navegação entre diretórios

1. Opções:

-L para seguir links                                
-P para seguir estrutura física

2. Exemplos:

Diretório por caminho absoluto: cd /home/luiz/Documentos/Aprendizado                                                
Diretório por caminho relativo: cd Aprendizado, quando está em Documentos                                               
Diretório anterior: cd ..                               
Diretório Home: cd                                      

#### cp

* cp + [Opções] + [Arquivo] + [Caminho]

Copia o arquivo para o diretório desejado

1. Opções:

-i: pergunta se será sobrescrito                        
-f: remove os arquivos de destino existentes                
-r: copia de forma recursiva                            

#### diff

* diff + [Opções] + [Arquivo] + [Arquivo]

Procura diferenças entre arquivos

#### display

* display + [Nome da Imagem]

Abrir imagens pelo terminal

#### du 

* du + [Opções] + [Arquivo]

Estima espaço utilizado

1. Opções

-h: anexa o rótulo de tamanho                           
-s: exibe somente o total

#### echo

* echo + [String]

Exibe uma linha de texto

1. Opções

-e: habilita interpretação de meta caracteres               
-n: não mostra novas linhas à direita

#### evince

* evince + [Arquivo PDF]

Abre o pdf para visualização

#### file

* file + [Opções] + [Arquivo]

1. Opções

-i: mostra o tipo MIME do arquivo

#### find

* find . + [Opções] + [Arquivo]

Procura arquivos pelo nome

1. Opções

-name: procura arquivos que contenham o nome                
-newer: procura arquivos que sejam mais novos               
-size: procura arquivos de tamanho especificado             
-exec: executa um comando sobre o arquivo                   

2. Exemplos

-find . -name "lista"                                   
-find . -size +30M                                      
-find . -newer lista.txt                                

#### finger

* finger

Procura por informações de usuários

1. Exemplos

-finger luiz

#### grep

* grep + [Opções] + [Arquivo]

Imprime linhas que coincidam com um padrão

1. Opções

-i: ignora maiúsculas e minúsculas

2. Exemplo

-grep "portao" lista.txt

#### groups

* groups + [Opções] + [Usuário]

Exibe grupos em que o usuário está

#### head

* head + [Opção] + [Arquivo]

Mostra a primeira parte de arquivos

1. Opções

-c: mostra os N bytes de cada arquivo
-n: mostra as primeiras N linhas

2. Exemplos

-head -c 20 lista.txt                                   
-head -n 1 lista.txt

#### id

* id + [Opção] + [Usuário]

Exibe IDs reais para grupo e usuário

#### less

* less + [Opções] + [Arquivo]

Exibe conteúdo mais sofisticado do arquivo

1. Opções

-N: mostra o número da linha

#### ln

* ln + [Opções] + [Origem] + [Destino]

Cria ligação entre arquivos

1. Opções

-i: Pergunta se pode substituir arquivo de destino existente
-f: Remove o arquivo de destino sem perguntar               
-s: Cria ligação soft

#### ls

* ls + [Opções] + [Arquivo]

Lista conteúdo

1. Opções

-a: Inclui arquivos que começam com .                   
-R: Lista diretórios encontrados recursivamente
-d: Lista nome de diretórios como arquivos              
-l: Escreve informações dos arquivos e diretórios encontrados
-r: Inverte ordem de ordenação                              
-1: Para saída em coluna simples

#### man

* man + [Comando]

Mostra o manual do comando

#### mkdir

* mkdir + [Opções] + [Diretórios]

Cria diretórios

1. Opções

-p: Cria diretório-pai de um caminho
-m: Indica o modo de permissão do diretório

2. Exemplos

mkdir -m 760 novodir

#### more

* more + [Arquivo]

Exibe conteúdo de um arquivo

#### mv

* mv + [Opção] + [Origem] + [Destino]

Move e/ou renomeia arquivos

1. Opções

-i: Questiona sobreescrever arquivo                         
-f: Apaga arquivo no destino

2. Exemplos

mv lista.txt lista2.txt (Renomeação)                    
mv Linux /home/luiz/Documentos (Movendo)

#### passwd

* passwd + [Opções] + [Login]

Modifica a senha do usuário

1. Opções

-x: Validade em dias da senha modificada

#### pkill

* pkill + [Opções]

Mata processos baseado no nome

1. Opções

- sinal: sinal numérico ou pelo nome que é enviado ao processo

#### ps 

* ps + [Opções]

Lista dos processos concorrentes

1. Opções

-a: Todos os processos do sistema
-x: Do usuário
-u: Em formato de orientação ao usuário

#### quota

* quota + [Opções]

Mostra o uso de disco e limites

1. Opções

-s: Usa unidades

#### rm 

* rm + [Opções] + [Arquivo]

Apaga arquivos e diretórios

1. Opções

-i: Questiona se cada arquivo será apagado                  
-f: Apaga sem perguntar                                 
-r: Apaga de forma recursiva

#### rmdir

* rmdir + [Opções] + [Diretório]

Remove diretórios vazios

#### Sort

* sort + [Opções] + [Arquivo]

Ordena linhas de arquivo de texto

1. Opções

-n: Compara o valor da string numérica                      
-r: Ordenação em ordem inversa                              
-u: Exclui repetições                                   

#### tail

* tail + [Opções] + [Arquivo]

Mostra a última parte do arquivo

1. Opções

-c: Mostra os N últimos bytes
-n: Mostra as últimas N linhas

#### tar

* tar + [Opções]

Gerencia compactação de arquivos

1. Opções

-c: Cria novo arquivo                                   
-x: Extrai arquivo de arquivo compactado                    
-j: Filtra o arquivo compactado através do bzip2               
-lzma: Filtra arquivo compactado através do lzma            
-z: Filtra o arquivo compactado através do gzip             
-t: Lista conteúdo do arquivo compactado                    

#### touch

* touch + [Opções] + [Arquivo]

Altera o rótulo de tempo do arquivo

1. Opções

-c: Não cria arquivos que não existam

#### wc

* wc + [Opção] + [Arquivo]

Imprime número de linhas, palavras e bytes

1. Opções

-c: Imprime número de bytes                             
-m: Número de caracteres                                   
-l: Imprime número de linhas                                
-w: Imprime número de palavras                              

#### Configurar teclado abnt2

* setxkbmap -model abnt2 -layout br

## Aplicações em Python:

* pipdate

Atualizar bibliotecas python

* pip freeze

Lista pacotes python

* pip install --upgrade + [Nome]

Atualiza manualmente

## Permissões

* ls - l: 

Exibe as permissões de arquivos ou diretórios dentro do diretório atual. O comando exibe os tipos de permissão por classe, sendo usuário, grupo e outros. 

As permissões são: r (read), w (write), x (execute) e - (sem permissão).

* man chmod:

Exibe outros tipos de permissão

* chmod + [Opção] + [Arquivo]:

Modifica a permissão de arquivo ou diretório

Tipo de Usuário | Tipo de Permissão | Mudança de Permissão
----------------|-------------------|---------------------
u (usuário) | r (read) | + (adiciona)
g (grupo) | w (write) | - (remove)
o (outros) | x (execute) |
a (todos usuários) | |

1. Exemplo de chmod u+r Teste:

Adiciona a permissão de leitura do arquivo/diretório para usuários

* ./

Executa programas com permissão habilitada
