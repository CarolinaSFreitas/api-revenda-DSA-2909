# api-revenda-DSA-2909

Aula 10 de Desenvolvimento de Serviços e APIs - ASSOCIAÇÕES - **N-N** - 29/09

# 🚗 Revenda

*Conferir o arquivo do Berçario* 

#### Documentação do Sequelize sobre associações: 
+ https://sequelize.org/docs/v6/core-concepts/assocs/

### Lembrando que:

**Pra iniciar**:
1. `` npm init -y ``
2. `` npm i express sequelize mysql2 cors ``
3. `` npm i --save-dev nodemon ``
4. `` npx nodemon app ``
5. No VS, criar um "app.js" como o arquivo do repo
6. ⚠️ Alterar o "package.json", adicionando a linha `` "type": "module", `` após a linha de "main": "index.js","

**Banco de Dados**:
1. Criar a pasta "database" com um arquivo chamado "conecta.js" e lá dentro inserir:

```
import { Sequelize } from "sequelize";

export const sequelize = new Sequelize('aula', 'aluno', 'senacrs', {
    host: 'localhost',
    dialect: 'mysql', /* one of 'mysql' | 'postgres' | 'sqlite' | 'mariadb' | 'mssql' | 'db2' | 'snowflake' | 'oracle' */
    port: 3306 
  });
  
````

**No Insomnia**:
1. URL: http://localhost:3000/aula
2. Criar uma pasta pro projeto
3. **CRUD**: Criar as HTTP Requests básicas (GET (listagem), POST (criação do registro no banco), PUT (alterações no registro), DEL (exclusão do registro))

----

## ⚠️ Atenção: Em 'app.js'

Deve-se criar primeiro a tabela que é dona da chave estrangeira. *Conferir o arquivo do Berçario* 

## 🔑 Chave Estrangeira - Para fazer o Relacionamento N-N (muitos pra muitos)

1. Após criar as tabelas em Models (tabelas: carros, etc), fora da definição dos campos deve-se indicar na tabela que vai receber a chave estrangeira (cliente):

*Conferir o arquivo do Berçario* 

## 🕹️ Controllers e Routes 🛣️

1. Tem que criar um controller para cada na pasta controllers, o **xController**, **yController** e **zController**.

2. Em 'routes.js', deve-se criar rotas para cada controller, *Conferir o arquivo do Berçario*. 
