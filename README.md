# Projeto de Assistente de Chamados

Este projeto é um assistente conversacional construído com [Rasa](https://rasa.com/) que possibilita a criação e o gerenciamento de chamados de homologação de software. O bot interage com o usuário para coletar informações essenciais (como nome do software, descrição, ramal e IP da máquina) e integra-se com uma API mock para simular a criação de chamados.

## Funcionalidades

- **Coleta de Dados via Formulário:**  
  O assistente utiliza um formulário para capturar os dados necessários para homologação.

- **Integração com API Mock:**  
  Os dados coletados são enviados para um endpoint de API mock, simulando a criação de um chamado. Essa integração pode ser facilmente adaptada para sistemas reais.

- **Integração com Microsoft Teams:**  
  A arquitetura do projeto permite a futura integração com o Microsoft Teams, possibilitando notificações e acompanhamento de chamados diretamente por essa plataforma.

- **Melhoria do Modelo de NLU:**  
  O modelo de linguagem pode ser aprimorado com novos dados e ajustes nos slots, intenções e entidades para aumentar a precisão na detecção das intenções do usuário.

## Requisitos

- [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/) (para execução em containers)
- Python 3.8+ (caso opte por rodar sem Docker)
- [Rasa](https://rasa.com/) (versão 3.1 ou superior)

## Instalação e Execução

### Com Docker

1. **Clone o repositório:**

   ```bash
   git clone https://github.com/seu-usuario/nome-do-projeto.git
   cd nome-do-projeto
Construa e inicie os containers:

bash
Copiar
docker-compose up --build
Treine o modelo:

bash
Copiar
docker-compose run --rm rasa train
Inicie o shell do Rasa:

bash
Copiar
docker-compose run --rm rasa shell
Sem Docker (usando ambiente virtual)
Clone o repositório e crie o ambiente virtual:

bash
Copiar
git clone https://github.com/seu-usuario/nome-do-projeto.git
cd nome-do-projeto
python3 -m venv venv
source venv/bin/activate
Instale as dependências:

bash
Copiar
pip install -r requirements.txt
Treine o modelo:

bash
Copiar
rasa train
Inicie o shell do Rasa:

bash
Copiar
rasa shell
Possibilidade de Colaboração
Este projeto está aberto à colaboração e sugestões para aprimoramento. Algumas áreas de interesse incluem:

Incremento de Funcionalidades de Chamados:

Aprimorar o fluxo de criação de chamados, incluindo validações e notificações adicionais.
Implementar integrações com sistemas reais de gerenciamento de chamados.
Integração com Microsoft Teams:

Desenvolver módulos para enviar notificações e atualizações para canais do Teams.
Criar comandos que permitam interagir com o assistente via Teams.
Expansão da Integração com API:

Expandir a integração com a API mock para suportar funcionalidades adicionais, como atualização ou cancelamento de chamados.
Adaptar a integração para APIs de sistemas de chamados reais.
Melhoria do Modelo de NLU:

Treinar o modelo com mais dados para melhorar a compreensão das intenções do usuário.
Ajustar os slots, entidades e intenções conforme feedback dos usuários.
Como Contribuir
Fork e Clone o Repositório:
Faça um fork do projeto e clone sua cópia local.

Crie uma Branch para sua Feature ou Correção:

bash
Copiar
git checkout -b feature/nome-da-sua-feature
Implemente suas Alterações:
Faça as modificações necessárias e teste o fluxo do bot.

Envie um Pull Request:
Após concluir suas alterações, envie um pull request com uma descrição detalhada das mudanças e funcionalidades implementadas.

Discussão e Revisão:
Participaremos ativamente da revisão e discussão das alterações. Feedbacks e sugestões são muito bem-vindos!

Contato
Se tiver dúvidas ou quiser discutir ideias de melhorias, abra uma issue ou entre em contato através dos canais disponíveis no repositório.

Sinta-se à vontade para melhorar e adaptar este projeto conforme as necessidades e sugestões da comunidade. Sua colaboração é essencial para tornar este assistente ainda mais robusto e funcional!
