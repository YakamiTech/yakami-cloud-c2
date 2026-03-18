# 🧠 Motor Lógico (Node-RED) e Ponte Web3

O Node-RED é o "maestro" da nossa nuvem. Ele escuta o MQTT, trata os dados e grava no Banco de Dados. 

## 🎯 Desafios do MVP (Fluxos de Dados)

1. **A Rota da Telemetria:** Crie um fluxo que faça *Subscribe* no tópico LoRa do veículo (Nav Explore). O Node-RED deve pegar o pacote com as coordenadas GPS, formatar a string JSON e fazer o *Insert* no InfluxDB.
2. **A Rota do Clima:** Criar um fluxo paralelo para escutar o tópico do sensor BME280 do sítio e registrar a série temporal.
3. **O Desafio do Hackathon (Integração Web3):** - Quando o Node-RED receber o webhook confirmando que um usuário escaneou o QR Code do Chalé (no Sítio), ele deverá acionar um nó de requisição HTTP (API REST).
   - Esta requisição enviará os dados (Timestamp, Local, ID do Usuário) para um Smart Contract na testnet da Polygon, registrando a entrada de forma imutável na blockchain.

**Governança:** Periodicamente, exporte os seus fluxos do Node-RED (formato `.json`) e faça um commit neste diretório. Isso é o backup oficial da inteligência do sistema.
