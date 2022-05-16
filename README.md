BASE URL:  
```JSON 
"https://psique-capstonem3.herokuapp.com/"
```

EndPoints

Cadastro:

POST /users

ex:
```JSON
{
    "email": "teste@teste.com",
    "password": "123456",
    "type": "staff" 
}
```


Login:

POST /login

ex:
```JSON
{
    "email": "teste@teste.com",
    "password": "123456"
}
```

response:
```JSON
{
	"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6InNlcmdpb0BtYWlsLmNvbSIsImlsdsdgsfTExMSwiZXhwIjoxNjUxNzg4NzExLCJzdWIiOiIyIn0.XpMIFM49i7yei5z6af4-ycFj5MMq7nLHZqIkLW5189E",
	"user": {
		"email": "teste@teste.com",
		"id": 2
	}
}
```


GET /patients

GET /staff

Necessário estar logado (Bearer token) para ver os pacientes e a equipe


POST /patients

Somente o usuário pode criar e alterar. O "userId" é o id do usuário que está criando. Necessário autenticação.

ex:
   ```JSON
   {
      "name": "Sérgio Othoniel",
      "userId": "2",
      "CPF": "11881641",
      "age": "32",      
      "appointments": [],
      "id": 1
  }
```


POST /staff

Somente o usuário pode criar e alterar. O "userId" é o id do usuário que está criando. Necessário autenticação.

ex:
```JSON
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
      "description": "Especialista em psicologia froudiana, infantil, pós-traumático, atendo há mais de 15 anos pacientes em um consultório em Campinas - SP.",
      "appointments": [],
      "CRM": "12224993439",
      "id": 1
    }
```


POST /appointments
GET  /appointments



