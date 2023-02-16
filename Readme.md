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

