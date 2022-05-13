BASE URL: https://psique-capstonem3.herokuapp.com/

EndPoints

Cadastro:

POST /users

ex:
{
    "email": "teste@teste.com",
    "password": "123456"
}


Login:

POST /login

ex:
{
    "email": "teste@teste.com",
    "password": "123456"
}

response:
{
	"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InNlcmdpb0BtYWlsLmNvbSIsImlsdsdgsfTExMSwiZXhwIjoxNjUxNzg4NzExLCJzdWIiOiIyIn0.XpMIFM49i7yei5z6af4-ycFj5MMq7nLHZqIkLW5189E",
	"user": {
		"email": "teste@teste.com",
		"id": 2
	}
}


GET /patients

GET /staff

Necessário estar logado (Bearer token) para ver os pacientes e a equipe


POST /patients

Somente o usuário pode criar e alterar. O "userId" é o id do usuário que está criando. Necessário autenticação.

ex:
   {
      "name": "Sérgio Othoniel",
      "userId": "2",
      "age": "32",
      "email": "sergio@mail.com",
      "appointments": [],
      "id": 1
}


POST /staff

Somente o usuário pode criar e alterar. O "userId" é o id do usuário que está criando. Necessário autenticação.

ex:
{
      "name": "Hannibal Lecter",
      "userId": "3",
      "age": "59",
      "email": "hannibal@mail.com",
      "specializations": [
        "Psicologia Infantil",
        "Tratamento pós-traumático",
        "Canibalismo"
      ],
      "description": [
        "Especialista em psicologia froudiana, infantil, pós-traumático, atendo há mais de 15 anos pacientes em um consultório em Campinas - SP."
      ],
      "appointments": [],
      "documents": "12224993439 CRM",
      "id": 1
    }


POST /appointments
GET  /appointments



