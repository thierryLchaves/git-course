# Git Course

Este é um repositorio teste para ensinar como o git funciona

Para adicionar um arquivo a sua branch, basta Utilizar o comando git add + o nome do arquivo
Para visualizar o status que se encontra seu arquivo basta utilizar o comando git status, Ao modificar um arquivo, e deixa-lo passivel de commit, é necessário realizar novamente o comando
git add <nome do arquivo>
Ao finalizar as edições pode-se/deve ser utilizado o comando git commit -m "", e de boa prache do git que seja adicionado um comentário que contenha informações, válidas sobre o que foi 
adicionado editado e afins. Após a nova adição de um arquivo, e seu commit, é apresentado para o usuário a hash do seu commit.

Das visualizações de logs:
O comando principal para visualizar logs sobre os commit's que foram realizados é o comando <b> git log</b>
Outro comando que pode ser utilizado trata-se do comando <b> git log --decorate </b>  Ao utilizar esse comando pode-se obter mais informações de log sobre sua branch, e modificações de arquivos, tais como informações de adições, comentários sobre os commits. etc...
Outro comando que pode ser utilizado como um filtro para os comando de Git, trata-se do comando <b> git log --author="nome do autos" </b>
Outro comando que pode ser utilizado para ter uma noção sobre os arquivos,branchs trata-se do comando <b> git shotlog </b> este comando realiza a exibição global, sobre os aquivos exibindo as seguintes informações, quais foram os autores, que realizaram commit, a quantidade de commit, e quais foram os comentários. Quando é necessário visualziar informações sobre sua branch de
maneira mais "enxuta", pode-se utilizar a variavél <b> -sn </b> depois do comando do shortlog
Outra bastante importante e comumente utilizado é o comando <b> git log --graph </b> este comando irá exibir de forma "gráfica" o que está ocorrendo, com suas branchs e versões

SObre as Hashs

Para ser visualizado o que foi adicionado com um arquivo que foi modificado, deverá ser utilizado o comando <b> git show <inserir qual hash> </b>, estas informações somente serão ser obtidaspor meio das hashs.

Sobre a DIFF

Ao realizar o comando <b> git diff </b>, será exibido em tela que o as modificações do arquivo pré commit e adição do mesmo no status de envio.Informando o que foi modificado, e quais foram as modificações no arquivo que está sendo trabalhado. E de boa pratica de mercado, utilizar o git diff antes da adição, caso exitam um grande quantidade de arquivos existentes na branch, um comando que pode e dever ser utilizado é o <b> git diff --name-only </b> este comando ira mostrar somente os arquivos que foram modificados com seus respectivos nomes.

<font size = 22> <b> OBS: Em casos de edição/ commit para arquivos que já foram adicionados "git add" , pode ser utilizado o comando git commit -am "informar as modificações Boas práticas" </font></b> </br>

SObre reversão de status dos arquivos. 
Caso esteja trabalhando em um arquivo dentro de suas branchs do git, e este tenha sido editado como um todo de maneira erronea, e anteriormente a realizar a mudança de status do mesmo. 
Podera ser utilizado o comando <b> git checkout </b> este comando ira retonar o estado origial do ultimo commit.
Caso seja realizado o git add, ou seja o arquivo for levado para a área de "statement",  o comando <b> git reset HEAD "nome do arquivo" </b>, a variável HEAD que é passada após o comando 
informa que deseja-se retornar ao ponteiro de origem, ou seja remover o aquivo recém adicionado do "statment" para que o mesmo possa ser editado novamente, sem quaisquer modificações pré adição.

Em casos de já ter comitado, o arquivo e este então já tenha sido adicionado ao repositório de forma definitiva, existe um comando com 3 (três) variavéis, que pode ser adicioandas para resolução deste problema sendo eles:
<b> git reset --soft / git reset --mixed / git reset /hard </b>

exemplo do git reset --soft
Este comando irá retonar o status do seu arquivo no estágio de statment, de certa forma matando o commit que foi realizado e deixando o arquivo em questão pronto para ser commitado novamenteou retornar através do git reset HEAD, sempre que for adicionado que este comando ou outro for utilizado caso deseje apagar informação é valido utilizar o git checkout nome do arquivo

Exemplo do git reset --mixed
Este comoando irá retonar o status do seu arquivo a um estágio anterior ao de Statment, de certa forma matando de fato o foi realizado e retornando o arquivo a estágio anterior de ser adicionado a fase pré commit, neste comando não é necessário realizar o git reset HEAD  nome do arquivo 
 
Exemplo go git reset --hard
Este comomando como o nome sugere realiza o reset completo do commit, apagando por completo o commit que foi realizado bem com as modificações que foram realizadas. 

<b> em amabos os casos deve sempre adicionar a hash do commit anterior ao commit que deseja-se utilizado 
OBS: Em casos de utilizar no repositório online (GitHub), o comando git reset --hard, o git informara que uma diferença entre os commit's que foram utilizados e somente adicionará quando atraves do git push force
</b>

para realizar a conexão entre o git local com o git de nuvem é necessário seguir alguns passos, e configurações. 
O primeiro e dentro do github, realizar a adição de um novo repositório de arquivos, após tal edição deverá ser adicionado os seguintes comandos
no bash adicionar o primeiro comando este sendo 

git remote add origin git@github.com:thierryLchaves/git-course.git, onde após a barra deverá ser substituído para o nome do repositório desejado


APós isso o outro comando é
git push -u origin main </br> este comando irá realizar a seguinte informação, git push (Irá enviar para o repositório todo log de modificações aqruivos e etc, do repositório origem para o repositósio desejado. -u (Serve somente para "trakear" para não haver a necessidade de digitar tudo novamente). orgin (e para onde irá o arquivo) main de onde está vindo o arquivo

Clonando repositórios
Para realizar o trabalho de repositórios não locais, o git disponibiliza através do comando git clone, está opção, ao acessar o repositório no github, sempre sera disponibilizado o endereço do repositório tanto em <b> SSH </b> quanto em https <i> preferir por meio de SSH é mais rápido a clonagem</i>
</br>

Para realizar o clone o comando a ser inserido é 
git clone <i> git@github.com:thierryLchaves/github-course.git (neste caso pode ser adicionado o endereço SSh do repositório, cada respositório disponivél terá seu endereço ssh </i> adicionar o nove nome da pasta, e importante não está no mesmo diretório que estava trabalhando, pois isso adicionara a pasta clonada dentro da sua pasta git

Fazendo fork de um projeto
Outra funcionalidade além do git clone é o fork, o git realiza a cópia de um projeto que não é seu e faz um cópia dele para você, esse comando é importante pois o github faz um cópia de um
repositório que não é da pessoa, para a pessoa em questão no proprio github, o que poseteriormente, pode ser clonado, o git clone somente serve para respositórios que são da pessoa. 


Sobre as branch

O que é um branch ?
De forma mais rapida a ser explicada, a branch e um ponteiro movel que leva a um comit

Lembrando a cada commit realizado em arquivos, o git gera um hash sobre aquele arquivo e um snapshot daquele arquivo naquele momento. 

O que o branch e como se fosse um ponteiro, que aponto pro repostório/arquivo naquele momento daquele commit em questão 
EX:

Branch

	MAIN
	  |
	  |
	  |
	F30ab ------------------- 34ac2--------------------------98ca9
	  |                         |                              |
	  |                         |                              |
 	Sanpashot C              Snapshot B                      Snapshot A



Pode haver casos em que tenha-se mais de um branch, apontando para o mesmo commit </br>
	<b> Separando </b>
	
	MAIN
	  |
	  |
	  |
	F30ab---------------------34acs--------------------------98ca9
	  |
	  |
	  |
	Testing -> Nova branch apontando para o mesmo commit

</br>
</br>


<b> Branches em diferentes commits </b>

				MAIN
				  |
				  |
				  |
	C0-----------C1----------c2----------c3
				             |
					     |
                                             |
					  Iss53

</br> </br>
<center> <h1> Mas por que usar branches ? </h1> </center>

<h3> As vantagens de se usar branches </h3>
<font size = "15px" face="comicsans">
<ol>
<li>Poder modificar sem alterar o local principal (Master) ex:Pode trabalhar em outro local, corrigir modificar algo sem modificar o princiapal </li>
<li>Facilmente "Desligável" ex:Pode ser apagado branchs muito fácil e rápido, podendo criar vário branches sem nenhum problema </li>
<li>Múltiplas pessoas trabalhando ex:Ou pode haver um projeto com 3 branches e cada uma trabalhando na sua sem interferir o outro </li>
<li>Evita conflitos ex:Como pode haver um caso que a pessoa X esteja trabalhando em uma branch exclusiva, a quantidade de conflitos e bem menor </li>
</ol>
</font>
  
 <h4 class="heading" style="text-align: center;"> Criando um branch  </h4>
O comando que é utilizado para se criar uma nova branch é : <b> git checkout -b "aqui deve ser inserido o nome da nova branch"</b>
par visualizar em qual branch está sendo trabalhada em seu repositório basta digitar o comando git branch

<h3 class="heading" style="text-align: center;"> Movendo criando e deletando branchs </h3>
Como dito anteriormente para visualizar a lista de branchs que existem no repositório que  está sendo trabalhado, basta digitar o comando:
<b> git branch </b> quando for necessário criar uma nova branch para o projeto em questão o comando a ser utilizado deve ser o <b> git checkout "nome da branch" </b>
quando é necessário realizar o retorno a branch principal, ou mudar a branch que se está trabalhando o comando utilizado deve ser o <b> git checkout "nome da branc desejada"</b>
Em casos que é necessário apagar a branch por algum motivo, o comando a ser digitado deverá ser o <b>git branch -D "nome do branch"</b>

</br></br>
<h2 class="headgin" style="text-align:center;">Entendendo o Merge </h2>
<p>
Quando se realiza o uso de branch, com branchs externos, com branchs internos faz-se necessário realizar a união dessa branchs, tal processo é feito através dos metodos existentes, 
sendo eles <b>MERGE</b> <b>REBASE</b>
<h3 class=heading" style="text-align:center;"> Passo a Passo - Merge </h3>
</br> 
<h4>No inicio exemplo com 2 branchs</h4>

                                MAIN
                                  |
                                  |
                                  |
        C0-----------C1----------c2
                                  |
                                  |
                                  |
                                Iss53



<h4>Criando um novo branch</h4>

                                MAIN
                                  |
                                  |
                                  |
        C0-----------C1----------c2----------c3
                                             |
                                             |
                                             |
                                          Iss53


<h4> Criamos um commit pelo branch main </h4>


				MAIN	  HOTFIX
				 |	    |
				 |	    |
				 |	    |
	C0----------C1----------C2----------C4
				  \
				   \
				    \
				    C3
				     |
				     |
				     |
				   Iss53

<h4>Criamos outro commit no branch iss53</h4>

                                          Main
                                            |
                                            |
                                            |
        C0----------C1----------C2----------C4
                                  \
                                   \
                                    \
                                    C3------C5
					    |
					    |
					    |
					   iss53


<h4> Fazendo o Merge </h4>

		                                       Main
                                           		 |
	                                            	 |
                                           		 |
        C0----------C1----------C2-----C4----------------C6
                                  \                     /
                                   \                   /
                                    \                 /
                                     \               /    
                                      \             /
                                       C3----------C5
                                                   | 
                                                   |
                                                   |
						  iss53
              


Esta forma de realizar a junção de uma branch de commit, para uma forma "linear", é chamada de forma diamante.Como pode se notar na figura os commit executados torana-se uma especie de ciclo
observando a figura pode se perceber que até o commit C2 os commit do main estão lineares, porém os commits C3 e C5, estão em outra ramificação do commit iss53.Criando um vertice tal qual umtriangulo, utilizando o comando merge, sempre que for realizar um este comando o git irá criar um novo commit, juntando o branch principal com o commit que está sendo trabalhado separadamente. Por tal motivo se for analizar, o commit C6 será um resultado de c4,c5 e c4.

<table>
<tr>
<th>Prós </th>
<th>Contras</th>
<tr> 
<td>Operação não destrutiva (não irá destruir commit nenhum, não estragando o histórico) </td>
<td>E um commit extra no seu projeto(é um commit pouco efétivo, não faz diferença no commit além de juntar branchs</td>
</tr>
<tr>
<td></td>
<td>Histótico poluído (isso pode ficar complicado a visualização do histórico caso haja muitas branchs) </td>
</table>

</br></br>

<h2 class="headgin" style="text-align:center;">Entendendo o Rebase </h2></br>
<h4> Estado inicial </h4>

                                    Main
                                     |
                                     |
                                     |
        C0----------C1----------C2---C4
                                  \
                                   \
                                    \
                                     C3
                                      |
                                      |
                                      |
                                 Experiment

</br>
<h4> Durante o processo </h4>


                                               Experiment
                                        Main      |
                                         |        |
                                         |        |
                C0-------C1------C2------C4------C3'
                                          \
                                           \
                                            \
                                             \
                                              \
                                               \
                                                C3


O Rebase realiza, opera de uma maneira um pouco diferente do merge, enquanto o merge, realiza um novo commit, para juntar os novos commit relaizar em uma nova branch a branch principal. 
O rebase, ele pega o commit da branch "auxiliar", e "move" pra frente de onde ele tiver "jogando", no nosso exemplo acima, este metodo, moveria o commit C3 para frente do commit c4, torando novamente os commits lineares.Realizando uma especie de delete do commit da branch "auxiliar. Em suma o rebase, move tudo que houve em um commit separado e coloca na fila sempre. 
Esse processo é chamado de: fast forward, no nosso exemplo ele pega o commit que não estava dentro da branch principal, e o move para frente commit principal, nesse caso ele pega o commit C3 e o move para frente do commit C4, fazendo assim que tanto o commit main e o commit expience estejam na mesma linha


                                                MAIN
                                                  |
                                                  |
                                                  |
                C0-------C1------C2------C4------C3'
                                                  |
                                                  |
                                                  |
                                              Experiment



E dessa forma os commit ficam de forma linear, dos commit's o que mitiga a confusão ao visualizar os commit's.
<table>
<tr>
<th>Prós </th>
<th>Contras</th>
<tr>
<td>Evita commits extras (Neste caso como ele mantem os commits na linearidade, não existe a necessidade de um commit extra) </td>
<td>Perde a ordem cronológica(Quando é utilizado o comando rebase, o histórico fica um pouco confuso, pois como ele sempre realiza a adição do seu commit a frente, pode haver certa confusão ) </td>
</tr>
<tr>
<td>Histórico Linear(O rebase sempre irá criar um histórico linear)</td>
<td></td>
</table>

<h2> obs é aconselhado a usar o comando pool <b>git pool --rebase </b>, evitando assim realizar mudanças em branchs que não utilizaria </h2>
</br>
<h1> GIT GINORE </h1>
<p>
Este arquivo server especificamente para não trakear alguns arquivos. 
Exemplo : Digamos que temos arquivos com senhas, e elas não podem ser "subidas para algum lugar publico", porém elas precisam ser adicionadas, no ambiente"
para não subir esse tipo de coisa, e feito o arquivo gitignore e dentro deste arquivo será adicionado no respositorio, e será escrito alguns padrões que ele não utilize.
Dentro do arquivo gitignore, é possivél não somente determinar qual arquivo em especifico como também informar os tipos de extensões que não serão "subidas".
Basicamente este  arquivo serve para determinar, quais extensões e ou arquivos não serão trakeados no commit. 

Para mais informações /exemplo de utilizações de projetos e arquivos que podem ser adicionados no GITIGNORE acessar o repositório através do lik
https://github.com/github/gitignore

</p>
</br></br>
<h1> GIT STASH</h1>
<b> Esse "Comando",</b> é responsável por guardar modificações que ainda não foram commitadas, em um arquivo que pode se chamar depois quando for necessário. 
Exemplo de utilização, 
ao estar trabalhando em uma branch x, com um arquivo Y, pode ser necessário realizar a troca de branch ou algo do tipo, porém não deseja-se realizar a adição desta modicação para Statament.Neste caso pode ser utilizado o comando : <b> git stash </b> para que o arquivo com suas alterações em questão seja modificado para o estado de WIP(Woking in Progress), o que iŕa retornar o arquivo em questão 
ao estado anteiror a alteração/modificação, ao realizar as mudanças que deseja seja em outra branch ou algo do tipo deve ser utilizado o comando : <b >git stash apply </b>
</br></br> o comando: <b> git stash list </b> mostra quais são os statsh contidos na branch
</br></br> o comando: <b> git stash clear </b> realiza a limpeza de todos os stash's existentes. 

</br></br>
<h1>Criando ALIAS</h1>
EXEMPLO:
git config --global alias.s status, neste caso o que este comando fará efetivamente. 
git config --global (Este trecho do código realiza como visto anteirormente a configuração global do git), alias.s (Este trecho do código informa que será adicionado um alias, e qual será o alias)
 status (Este techo do codigo informa qual o comando será subistitudo ou apelidado)


</br></br>
<h1>Versionando com Tags</h1>
para trabalhar com tag o comando é: <b> git tag -a 1.0.0 -m "Readme finalizado"</b> neste techo do código é informaod que será adicionado uma tag, e o trecho -a servira como anotação  </br>
Para realizar a adição de deste comando é necessário realizar o comando <b> git push origin main --tags </b>
Ao digitar git tag é possivel ver quais tags estão disponivéis 

</br></br>
<h1>Git Revert</h1>

assasa
