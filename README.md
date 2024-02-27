# P4-HiveMQ-M9

## Introdução

Desenvolvimento de comunicação MQTT. Um broker HiveMQ foi levantado e o objetivo é se conectar e fazer uma publicação no mesmo.

### Código 1: Subscriber MQTT

Este programa é um cliente MQTT assíncrono em Go que se conecta a um broker MQTT, se inscreve em um tópico específico e recebe mensagens publicadas nesse tópico.

1. **Dependências:**
   - `github.com/eclipse/paho.mqtt.golang`: Pacote que fornece suporte MQTT para Go.
   - `github.com/joho/godotenv`: Pacote para carregar variáveis de ambiente de um arquivo `.env`.

2. **Funcionalidades Principais:**
   - Carrega as credenciais do broker MQTT e outras configurações a partir de um arquivo `.env`.
   - Define tratadores para eventos de conexão bem-sucedida e perda de conexão.
   - Conecta-se ao broker MQTT com TLS.
   - Se inscreve em um tópico MQTT especificado.
   - Exibe mensagens recebidas no console.

3. **Estrutura do Código:**
   - Declaração de tratadores de eventos de conexão (`connectHandler`) e perda de conexão (`connectLostHandler`).
   - Função `main()`:
     - Carrega as variáveis de ambiente do arquivo `.env`.
     - Configura as opções do cliente MQTT.
     - Cria um novo cliente MQTT.
     - Conecta-se ao broker MQTT e se inscreve no tópico especificado.
     - Aguarda indefinidamente por novas mensagens.

### Código 2: Publisher MQTT

Este programa é um cliente MQTT em Go que publica mensagens em um tópico específico em um broker MQTT de forma periódica.

1. **Dependências:**
   - `github.com/eclipse/paho.mqtt.golang`: Pacote que fornece suporte MQTT para Go.
   - `github.com/joho/godotenv`: Pacote para carregar variáveis de ambiente de um arquivo `.env`.

2. **Funcionalidades Principais:**
   - Carrega as credenciais do broker MQTT e outras configurações a partir de um arquivo `.env`.
   - Define tratadores para eventos de conexão bem-sucedida e perda de conexão.
   - Conecta-se ao broker MQTT com TLS.
   - Publica mensagens em um tópico MQTT especificado em intervalos regulares.
   - Exibe as mensagens publicadas no console.

3. **Estrutura do Código:**
   - Declaração de tratadores de eventos de conexão (`connectHandler`) e perda de conexão (`connectLostHandler`).
   - Função `main()`:
     - Carrega as variáveis de ambiente do arquivo `.env`.
     - Configura as opções do cliente MQTT.
     - Cria um novo cliente MQTT.
     - Conecta-se ao broker MQTT.
     - Publica mensagens periodicamente em um loop infinito.
     - Desconecta-se do broker MQTT ao finalizar o programa.

##


## Vídeo de Execução

Link: https://drive.google.com/file/d/1cKSwXpluNlZq_xeA7bYzuh0NXOhLn9Y_/view?usp=sharing