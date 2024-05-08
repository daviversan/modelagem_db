# Modelagem do banco de dados
## SQL Designer
<img src="modelagem_db.png">

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
&nbsp;&nbsp;&nbsp;&nbsp; Tabela destinada ao cadastro do usuário, caso ainda não tenha uma conta. É associada à tabela users através de uma conexão id_users, referenciando um usuário para cada cadastro.

### sign_in
