# ☁️ Yakami Tech - Cloud C2 (Comando e Controle)

Bem-vindo ao repositório oficial do módulo **Cloud C2**, o cérebro de processamento e visualização de dados da arquitetura híbrida ASTRA-Net (Yakami Tech).

## 🎯 Sobre este Módulo
Este repositório centraliza toda a infraestrutura "Server-Side" da nossa operação. Ele é responsável por receber os pacotes encriptados dos Gateways (EcoStations), processar a lógica de negócios, armazenar o histórico de telemetria e disponibilizar o Dashboard de Consciência Situacional.

## 🗂️ Estrutura do Diretório
Nossa nuvem é arquitetada em microsserviços. O código está dividido nas seguintes camadas:
* 📁 `/infrastructure` -> Arquivos de provisionamento da Máquina Virtual (Azure), Docker Compose, configurações do Mosquitto (MQTT) e Banco de Dados (InfluxDB).
* 📁 `/node_red_flows` -> Exportação em JSON dos fluxos lógicos do Node-RED (O motor de processamento e a ponte para a Web3).
* 📁 `/dashboards` -> Exportação em JSON dos painéis visuais criados no Grafana.

## 🛡️ Governança e Segurança Cibernética
A segurança deste repositório é vital para atender aos requisitos da norma ISO 27001 (exigência da Marinha/Defesa). Senhas, tokens de API e chaves privadas **NUNCA** devem ser commitadas em texto plano. Utilize variáveis de ambiente (`.env`).

---
*Desenvolvido na Amazônia, para o Mundo.* 🌎🚀
