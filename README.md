# Plataforma-Monitoramento-Dispositivos-IoT

## Descrição

Este projeto é uma aplicação web full-stack desenvolvida para integrar dispositivos IoT em uma plataforma colaborativa. O objetivo é fornecer uma ferramenta para monitoramento e coleta de dados em tempo real, auxiliando na tomada de decisões no setor agrário, com foco na volumetria de chuva.

### Community IoT Device (CIoTD) 1.0.0

**OAS 3.0**

A CIoTD é uma plataforma colaborativa para compartilhamento de acesso a dados de dispositivos IoT. Através dela, colaboradores podem cadastrar seus dispositivos, permitindo que qualquer pessoa possa coletar os dados desses dispositivos e utilizá-los em suas aplicações.

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
- **Frontend:** Angular + Material

## Como Executar o Projeto

1. Clone o repositório:
   ```sh
   git clone https://github.com/felipesntr/IoT-Device-Monitoring-Platform
   ```
2. Navegue até o diretório do projeto:
   ```sh
   cd IoT-Device-Monitoring-Platform
   ```

## Detalhes de implentação

Para registrar novos dispositivos, implementei um controller da API que utiliza o padrão Command, enviando o Command de registro de um dispositivo que, por fim, é recebido pelo "Handler" específico desse Command.

A decisão de utilizar esse padrão para todos os Commands e Queries se deve à facilidade de implementação com o Mediatr, ao desacoplamento das lógicas de negócios, tornando o Controller extremamente simples, além da reusabilidade e manutenabilidade. Além disso, como pode ser visto no projeto de testes, os testes são bem simples de se implementar, pois os Commands, Queries e Handlers podem ser testados isoladamente.

Escolhi manter algumas validações dentro do próprio Command, como no exemplo do RegistrarDevice, pois no futuro posso utilizar Fluent Validations sem causar impactos no Handler.

A utilização de DTOs se dá pela facilidade de uso nas requisições e por não expor totalmente os Commands. No futuro, podemos cadastrar contextos específicos em cada Command sem a necessidade de o usuário fornecer via API Request.

## Contato

Para mais informações, entre em contato através de felipr.sntr@gmail.com .
