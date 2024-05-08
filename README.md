# Modelagem do banco de dados
## SQL Designer
<img src="new_modelagem.png">

## Entidades 
### Users
&nbsp;&nbsp;&nbsp;&nbsp; Entidade central do modelo, em que todas as conexões são efetuadas. Contém os seguintes atributos:
- ``` id: ``` Código de identificação único para cada usuário
- ```name: ```Nome criado pelo usuário para ser identificado na plataforma
- ```age:``` Idade do usuário
- ```email:``` Email fornecido pelo usuário para efetuar a autenticação da conta e através do qual a comunicação com a plataforma será estabelecida
- ```admin:``` Opção de administrador para usuários cadastrados com essa responsabilidade
- ```pesqusador:``` Opção de conta para usuários não administradores

### sign_up
&nbsp;&nbsp;&nbsp;&nbsp; Tabela destinada ao cadastro do usuário, caso ainda não tenha uma conta. É associada à tabela users através de uma conexão ```id_users```, referenciando um usuário para cada cadastro.

### sign_in
&nbsp;&nbsp;&nbsp;&nbsp; A tabela sign_in é destinada aos usuários que já possuem cadastro e pretendem acessar sua conta. Compartilha os atributos ```name```, ```age``` e ```password```. Possui conexões com a tabela ```users```, ```sign_up``` e ```address```.

### address
&nbsp;&nbsp;&nbsp;&nbsp; A tabela ```address``` referecia um endereço por usuário, sendo definido no momento de cadastro, portanto a conexão com a tabela ```sign_up```. Seus dados são automaticamente ativados no momento de sign_in

### forms
&nbsp;&nbsp;&nbsp;&nbsp; A tabela ```forms``` representa o formulário da aplicação web que será preenchido pelo usuário. É composta pelos seguintes atributos:
- question: Referencia as perguntas do formulário
- anwser: Referencia as respostas para as perguntas do formulário
- had_dogs: Representa a opção selecionada por usuários que já tiveram um cachorro
- will_have_dogs: Representa a opção selecionada por usuários que pretendem ter um cachorro
- have_dogs:  Representa a opção selecionada por usuários que possuem um cachorro

&nbsp;&nbsp;&nbsp;&nbsp; Essa tabela faz uma conexão única com os users, recebendo id_users e id_dogs para efetuar a conexão dos dados.

### dogs
&nbsp;&nbsp;&nbsp;&nbsp; Essa tabela referencia os cachorros que serão adicionados ao banco de dados. É composta pelos seguintes atributos:
- id
- name
- breed
- age
- 
