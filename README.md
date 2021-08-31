# Corebiz AWS API

## Instalar serverless framework

```zsh
npm install -g serverless
```

MacOS/Linux

```zsh
sudo npm install -g serverless
```

## Instalar dependências

```zsh
npm install aws-sdk
npm install uuidv4
```

## Verificar versão e instalação

```zsh
serverless
serverless --version
```

## Configurar IAM credentials em AWS

1. Procurar por IAM em AWS Services
2. Entrar em Usuários
3. Adicionar novo usuário
4. User name => serverless
5. Click em acesso programático
6. Next
7. Attach policy => AdministratorAccess
8. Next
9. Criar usuário

```zsh
serverless config credentials --provider aws --key {Access Key ID} --secret {Access Secret}
```

## Criar projeto e boilerplate

```zsh
mkdir {nome_do_projeto}
cd {nome_do_projeto}
sls create -t aws-nodejs
```

## Deploy

```zsh
sls deploy
```

## Endpoints da API

POST - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads <br>
GET - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads <br>
PUT - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads/{id} <br>
DELETE - https://se3l85r4x5.execute-api.us-east-2.amazonaws.com/dev/leads/{id} <br>

## CORS
Configurado o CORS nos headers das requisições no arquivo handler.js
```js
headers: {
"Access-Control-Allow-Headers" : "Content-Type,X-Amz-Date,Authorization,X-Api-Key,X-Amz-Security-Token",
"Access-Control-Allow-Origin": "*",
"Access-Control-Allow-Methods": "OPTIONS,POST,GET,PUT,DELETE"
```
}
