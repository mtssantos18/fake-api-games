# Adicionar seus jogos favoritos e seu computador;

Essa API foi desenvolvida para que você possa adicionar seus jogos favoritos, e as especificações do seu computador.

_Url Base para API :_ https://fake-api-mtssantos18.herokuapp.com/

# Endpoints

# Usuário

## Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.

### Body:

{ <br/>
"email": "insira um email", <br/>
"password": "sua senha" <br/>
"age": "idade", <br/>
"name": "nome" <br/>
}

## Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Body:

{ <br/>
"email": "insira um email", <br/>
"password": "sua senha" <br/>
}

# Games

GET /games

Você pode visualizar os jogos postados pelos usuários.

Não precisa de body, porém necessita estar logado com um usuário para ter acesso as informações de jogos.

POST /games

Para postar um novo jogo insira a classificação do seu jogo, nome e seu nível de habilidade no jogo: <br/>
**OBS**: não esquece de insirir o userId, referente ao seu cadastro;

### Body:

{ <br/>
"type": "classificação", <br/>
"name": "nome do jogo", <br/>
"skillLevel": "nível de habilidade", <br/>
"userId": 1 <br/>
}

# Computer

GET /computer

Você pode visualizar os computares listados na API.

Não precisa de body, e não precisa de autenticação para visualizar os computadores postados;

POST /computer

Para postar as especifciações do seu computador, faça um post com as seguintes informações: <br/>
**OBS**: não esquece de insirir o userId, referente ao seu cadastro;

### Body:

{ <br/>
"processor" : "processador", <br/>
"motherboard": "placa mãe", <br/>
"ram": "memória ram", <br/>
"storage": "espaço de armazenamento", <br/>
"gpu" : "placa de vídeo", <br/>
"userId": "1" <br/>
}
