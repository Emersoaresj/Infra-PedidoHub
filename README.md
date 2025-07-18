# Infra-PedidoHub

Repositório de infraestrutura para orquestração dos microsserviços do sistema **PedidoHub** utilizando Docker Compose.

## 📦 Estrutura esperada

Coloque este repositório e todos os microsserviços lado a lado em uma mesma pasta, por exemplo:

/alguma-pasta/

   ├─ cliente-service/

   ├─ produto-service/

   ├─ estoque-service/

   ├─ pedido-service/

   ├─ pagamento-service/

   ├─ pedido-receiver/

   └─ Infra-PedidoHub/

## 🚀 Como rodar

1. **Clone todos os repositórios dos microsserviços e o Infra-PedidoHub**
2. **Copie o arquivo `.env.example` para `.env`** e preencha as variáveis conforme necessário.
3. No diretório `Infra-PedidoHub`, execute:

   ```bash
   docker compose up --build

4. Todos os serviços serão iniciados juntos, prontos para integração e testes.


## ⚙️ Serviços orquestrados
PostgreSQL (banco de dados)

Kafka e Zookeeper (mensageria)

cliente-service

produto-service

estoque-service

pedido-service

pagamento-service

pedido-receiver (consumer)

Cada microsserviço sobe em sua própria porta, conforme especificado no docker-compose.yml.

 Variáveis de ambiente
O arquivo .env contém as variáveis utilizadas no docker-compose.yml, como dados de conexão do banco e configurações dos serviços.
Nunca versionar o .env com dados sensíveis!
Forneça um .env.example para facilitar a configuração.

## 🛠️ Dicas
Para acessar os bancos de dados, utilize a porta 5432.

Os microsserviços expõem APIs REST em suas respectivas portas (8081 a 8086).

Kafka expõe a porta 9092.

## 🧪 Testes
Após subir todos os serviços, utilize ferramentas como Postman ou Swagger UI (se disponível nos micros) para testar os endpoints.

## 📚 Documentação
Para informações sobre cada microsserviço (endpoints, exemplos etc), consulte o README de cada repositório individual.
