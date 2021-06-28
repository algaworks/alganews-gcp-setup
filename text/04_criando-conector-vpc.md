## Criando um conector VPC

Para que a nossa aplicação consiga se conectar ao banco de dados, é necessário criar um conector VPC para a rede.

Ative o serviço de *VPC Access* e *Network* utilizando os comandos:

```
gcloud services enable servicenetworking.googleapis.com
gcloud services enable vpcaccess.googleapis.com
```

Depois, crie um conector com o comando:

```
gcloud compute networks vpc-access connectors create vpc-connector-us-central1 ^
       --network default --region us-central1 --range 10.10.0.0/28 
```
**Importante**: O acento circunflexo (\^) é o caractere de *escape* no prompt de comandos do Windows, utilizado para inserir um comando em mais de uma linha. Use o caractere de *escape* correspondente ao seu sistema operacional ou terminal ou digite tudo em uma única linha.


#### Referências

 - [Google Cloud Docs - Configurando VPC Access](https://cloud.google.com/vpc/docs/configure-serverless-vpc-access)

