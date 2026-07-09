 # 7.8 Arquitetura de Software

O Sistema de Gestão de Sala de Aula Online utiliza uma Arquitetura Híbrida, que combina o padrão Em Camadas (para as operações estruturais e transacionais) com o modelo Publish-Subscribe / Orientado a Eventos (para a camada de comunicação e atualizações em tempo real).

#  Justificativa Técnica

1. Camadas para o Core da Aplicação: Os fluxos tradicionais de dados do sistema — como gerenciamento de turmas, matrículas de estudantes, envio de arquivos e controle de perfis — são isolados em camadas distintas (Apresentação, Aplicação, Domínio e Infraestrutura). Essa separação de conceitos simplifica a manutenção do código, viabiliza testes automatizados isolados e facilita o desenvolvimento paralelo da equipe por meio das branchs do Git.
2. Publish-Subscribe para Notificações e Reatividade: Um dos principais requisitos não-funcionais do sistema é a entrega instantânea de informações (como postagens no mural, mensagens e lançamento de notas). Centralizar essa demanda em requisições HTTP tradicionais geraria gargalos no banco de dados devido ao excesso de requisições síncronas paralelas. O padrão Pub/Sub soluciona isso de forma assíncrona: a camada de aplicação publica um evento específico (ex: AtividadePostadaEvent) e o intermediador de mensagens encarrega-se de atualizar os clientes conectados (estudantes assinantes daquela turma) instantaneamente.

---

 # 7.10 Decisões Arquiteturais

A tabela abaixo descreve as três principais decisões arquiteturais tomadas para o projeto, correlacionando o problema de negócio às escolhas técnicas implementadas.

| Decisão Arquitetural | Contexto / Problema | Solução Adotada | Justificativa / Impacto Técnico |
| :--- | :--- | :--- | :--- |
| **Estilo Arquitetural Híbrido** | Necessidade de isolar regras de negócio complexas do MVP sem perder performance em notificações massivas. | Fusão de Arquitetura em Camadas com Mensageria baseada em eventos (Pub/Sub). | Permite velocidade na entrega do escopo principal (Camadas) combinado com uma estrutura escalável para interações em tempo real. |
| **Mecanismo de Autenticação** | Controle de acesso estrito baseado em papéis (Professores vs. Alunos) com rotas protegidas na API. | Autenticação Stateless com tokens JWT (JSON Web Tokens). | Elimina a necessidade de manter estados de sessão na memória do servidor, garantindo segurança na validação de permissões diretamente no cliente. |
| **Estratégia de Notificações** | Risco de degradação da performance do banco de dados por requisições redundantes de checagem de novas mensagens. | Protocolo WebSockets integrado a um broker de mensageria assíncrona (Redis/RabbitMQ). | Permite a persistência de conexões leves e bi-direcionais para empurrar atualizações na tela do usuário sem sobrecarregar a infraestrutura transacional. |
