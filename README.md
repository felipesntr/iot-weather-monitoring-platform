# iot-weather-monitoring-platform

## Descrição

Este projeto é uma aplicação web full-stack desenvolvida para integrar dispositivos IoT em uma plataforma colaborativa. O objetivo é fornecer uma ferramenta para monitoramento e coleta de dados em tempo real, auxiliando na tomada de decisões no setor agrário, com foco na volumetria de chuva.

## Funcionalidades

- **Autenticação de Usuários:** Permite que os usuários se autentiquem para configurar e acessar dados de monitoramento.
- **Seleção de Dispositivos:** Exibe todos os dispositivos cadastrados na plataforma, permitindo que os usuários selecionem e configurem aqueles que desejam monitorar.
- **Configuração de Comandos:** Para cada dispositivo selecionado, os usuários podem indicar quais comandos disponibilizados pelo dispositivo devem ser utilizados.
- **Dashboard de Monitoramento:** Lista todos os dispositivos selecionados e apresenta as respostas para cada um dos comandos configurados.
- **Coleta de Dados via Telnet:** Realiza o acesso aos dados do dispositivo utilizando o protocolo Telnet, enviando comandos e coletando as respostas.
- **Otimização de Requisições:** Implementa métodos para otimizar as requisições e reduzir os tempos de resposta.

## Tecnologias Utilizadas

- **Backend:** C#, .NET
- **Banco de Dados:** SQLite
- **Autenticação:** JWT
- **Protocolo de Comunicação:** Telnet

## Como Executar o Projeto

1. Clone o repositório:
   ```sh
   git clone https://github.com/felipesntr/iot-weather-monitoring-platform
   ```
2. Navegue até o diretório do projeto:
   ```sh
   cd iot-weather-monitoring-platform
   ```

## Contribuições
Contribuições são bem-vindas! Por favor, envie um pull request ou abra uma issue para discutir suas ideias.

## Contato
Para mais informações, entre em contato através de felipr.sntr@gmail.com .