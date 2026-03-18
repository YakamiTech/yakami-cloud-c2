# 📘 Manual de Workflow - Cloud C2

Diferente do hardware, a nuvem sofre ataques da internet 24 horas por dia. Nossa governança aqui precisa focar em estabilidade e segurança.

## 🚨 Regras Vitais
1. **Zero Segredos no Código:** Nunca faça commit de ficheiros `.env`, senhas de banco de dados, chaves SSH do Azure ou Private Keys de carteiras Web3 (Polygon). Se vazar, o repositório está comprometido. Use o `.gitignore` com rigor.
2. **Feature Branches:** Nenhuma alteração de fluxo do Node-RED vai direto para a branch `main`.
   - `git checkout -b feature/integracao-polygon`
   - `git checkout -b fix/porta-mqtt`

## 🔄 Homologação
Antes de alterar um tópico MQTT no Node-RED, valide com a equipe de Firmware (repositório `yakami-ecostation`) se eles já atualizaram o código em C++ nas placas físicas. Um erro de sincronia entre estes repositórios causa a perda instantânea dos dados da missão.
