# 🏗️ Infraestrutura e DevOps (Azure & Docker)

Wilson, o objetivo desta pasta é garantir a **Recuperabilidade** do sistema. Se o servidor do Azure explodir amanhã, você precisa ser capaz de reerguer a nuvem inteira da Yakami em menos de 15 minutos usando os arquivos que estão aqui.

## 🎯 Desafios do MVP (Arquitetura)

1. **Dockerização:** Não instale nada diretamente no sistema operacional (Ubuntu) do Azure. Crie um arquivo `docker-compose.yml` aqui dentro que suba os 4 contêineres do nosso sistema:
   - Eclipse Mosquitto (Broker MQTT)
   - Node-RED (Motor Lógico)
   - InfluxDB (Banco de Dados de Séries Temporais)
   - Grafana (Visualização)
2. **Segurança MQTT:** Configure o arquivo `mosquitto.conf` para exigir usuário e senha de conexão. As placas EcoStation não podem publicar dados anonimamente.
3. **Persistência de Dados:** Garanta que os volumes do Docker estejam mapeados corretamente para que os dados do banco não sejam apagados caso o contêiner reinicie.
