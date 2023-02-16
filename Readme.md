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


