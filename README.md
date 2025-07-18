Infra-PedidoHub

Repositório de infraestrutura para orquestração dos microsserviços do sistema PedidoHub utilizando Docker Compose.

-------------------------------------------------------------
📂 Estrutura de pastas necessária
-------------------------------------------------------------
> ⚠️ **IMPORTANTE:**  
> Para rodar o PedidoHub, siga exatamente o passo a passo abaixo!  
> Estruture as pastas conforme o exemplo e execute o docker compose no diretório Infra-PedidoHub.

-------------------------------------------------------------
## 1. Crie uma pasta para o seu projeto
   Exemplo: C:\Users\SeuUsuario\Documentos\pedidohub-projeto\


-------------------------------------------------------------
## 2. Clone todos os repositórios dentro dessa pasta:
      
   
      git clone https://github.com/Emersoaresj/Cliente-Service.git   
      git clone https://github.com/Emersoaresj/Produto-Service.git   
      git clone https://github.com/Emersoaresj/Estoque-Service.git   
      git clone https://github.com/Emersoaresj/Pedido-Service.git 
      git clone https://github.com/Emersoaresj/Pagamento-Service.git 
      git clone https://github.com/Emersoaresj/Pedido-Receiver.git   
      git clone https://github.com/Emersoaresj/Infra-PedidoHub.git   

-------------------------------------------------------------
## 3. Verifique se a estrutura ficou assim:

pedidohub-projeto/   
├─ Cliente-Service/  
├─ Produto-Service/  
├─ Estoque-Service/  
├─ Pedido-Service/   
├─ Pagamento-Service/   
├─ Pedido-Receiver/  
└─ Infra-PedidoHub/
```
   ├─ docker-compose.yml    
   ├─ .env  
   └─ README.md
   ```
-------------------------------------------------------------

## 4. Acesse a pasta Infra-PedidoHub e execute:

   ```docker compose up --build```

-------------------------------------------------------------
## ⚙️ Serviços Orquestrados

- PostgreSQL (banco de dados)
- Kafka e Zookeeper (mensageria)
- cliente-service
- produto-service
- estoque-service
- pedido-service
- pagamento-service
- pedido-receiver (consumer)

Cada microsserviço sobe em sua própria porta, conforme especificado no docker-compose.yml.

-------------------------------------------------------------
## 📝 Variáveis de ambiente

O arquivo .env contém as variáveis utilizadas no docker-compose.yml, como dados de conexão do banco e configurações dos serviços.
Nunca versionar o .env com dados sensíveis!
Forneça um .env.example para facilitar a configuração.

-------------------------------------------------------------
## 🛠️ Dicas

- Para acessar o banco de dados, utilize a porta 5432.
- Os microsserviços expõem APIs REST em suas respectivas portas (8081 a 8086).
- Kafka expõe a porta 9092.

-------------------------------------------------------------
## 🧪 Testes

Após subir todos os serviços, utilize ferramentas como Postman ou Swagger UI (se disponível nos micros) para testar os endpoints.

-------------------------------------------------------------
## 📚 Documentação

Para informações sobre cada microsserviço (endpoints, exemplos etc), consulte o README de cada repositório individual.

-------------------------------------------------------------
Dúvidas ou sugestões? Abra uma issue ou entre em contato pelo GitHub!
