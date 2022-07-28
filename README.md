# fullcycle-docker-desafio-nginx-node

## FullCycle - Desafio Docker: nginx - nodejs - mysql

- nginx como proxy reverso para a aplicação node.js usando mYsql para persistir os dados, sendo um container para cada.

- Ao acessar o nginx, a aplicação node será chamada que então irá salvar um nome aleatório (gerado em cada nova requisição GET) no banco de dados MySQL (nodedb), retornando todos os nomes salvos para serem listados na página.

![image](https://user-images.githubusercontent.com/31414164/181399016-ca69ee49-f2b4-4b68-9a3b-b9704c0d64da.png)


## Comandos:

- sudo docker-compose up --build -d

![image](https://user-images.githubusercontent.com/31414164/181396162-7264bedc-c8c4-4335-a101-ac204940b7fd.png)

- docker ps

![image](https://user-images.githubusercontent.com/31414164/181396206-a9e04ad1-ed44-40b2-bcd9-9f25530776dd.png)

### Para acessar os containers em execução (iterativamente acessar o bash do container em execução):
- docker exec -it container-name bash 

### Para verificar logs no container em caso de erros:
- docker logs container-name

### No caso de acessar o container MySQL, seguem comandos úteis para acessar o banco de dados no container:

- mysql -uroot -p (digitar senha em seguida "root")
- show databases;
- use nodedb;
- SELECT * FROM PEOPLE;
