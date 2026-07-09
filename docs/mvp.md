Funcionalidade Essenciais:
  FE1 - Autenticação: Login para os estudantes, professores, coordenadores, administradores.
  FE2 - Gestão da Turma: Permite que o administrador crie as novas turmas e vincule a elas os alunos e professores. Além de poder arquivar uma turma ou alterá-la (adicionar ou retirar estudantes/professores.
  FE3 - Publicação das atividades: Permite que o professor poste novas atividades em turmas que ele é o professor e quue estejam ativas. Permissão apenas para o professor.
  FE4 - Envio de Trabalhos com Prazo de Entrega: Permite ao estudante anexar um arquivo na atividade desde que esteja dentro do seu prazo de entrega, bloqueando novos envios ou alterações após a data de vencimento da atividade.
  FE5 - Lançamento e Consulta de Notas: Permite ao professor atribuir notas aos envios de atividade dos alunos e garante que o estudante visualize apenas o seu desempenho de forma organizada.
  FE6 - Gerenciamento do Sistema: Permite que o Administrador gerencie os usuários, permissões de acesso e configurações do sistema. O Administrador mesmo tendo acesso a quase todo o sistema, não possui autorização para alteração/postagem de notas e atividades.

Funcionalidades Futuras:
  FF1 - Sistema de Mensagens Interno: Troca de mensagens entre professores e alunos e o histórico da conversa.
  FF2 - Painel do Coordenador: Tela de monitoramento e acompanhamento das turmas para o coordenador. Sem a possibilidde de alteração de informações.
  FF3 - Configuração de Notificação das Atividades: Opção do aluno ativar/desativar o recebimento de mensagens automáticas sobre as atividades.
  FF4 (Funcionalidade Inovadora) - Mapa de Aprendizagem da Turma: Visão Geral do desempenho da turma disponível para os professores e o coordenador, permite a identificação de conteúdos que a turma apresenta maior dificuldade, auxiliando professores na tomada de decisões pedagógicas e snedo um acréscimo no Painel do Coordenador.

Justificativa da Priorização:
  Justificativa das Funcionalidades Essenciais:
    FE1 e FE6 - Necessário para que o sistema funcione corretamente, pois cada tipo de usuário possui um bloqueio ou permissão dentro do sistema que deve ser respeitada para que o fluxo correto funcione. Ex: um aluno não deve ter o poder de alterar a sua nota.
    FE2 - Necessário para que os alunos e professores vejam apenas as turmas que os interessam.
    FE3, FE4 e FE5 - Necessário para que seja seguido o fluxo padrão em relação à postagens de atividades para os alunos, o envio da atividade pelos alunos e o recebimento da nota.
    FE2, FE4 e FE6 - Regras necessárias para a segurança e integridade de dados acadêmicos.
  Justificativa das Funcionalidades Futuras:
    FF1 - Chat em tempo real possuem alta complexidade de desenvolvimento (histórico, notificações...). O contato de início pode ser feito via e-mail/whatsapp, sem que isto afete que o sistema funcione corretamente.
    FF2 - Devido ao seu objetivo ser a visualização de informações, sem que haja alteração ou criação, pode ser adiado. Primeiro deve ser focado em o processo acontecer corretamente (criação de turmas, postagens de atividades...) para após criar uma maneira de visualizar todas esses dados. Além de ser possível contornar a falta da visualização com relatórios feitos direto do banco de dados.
    FF3 - Seria necessário a criação/alteração da tela de configuração disponível para o aluno, além do  sistema sempre precisar verificar com esta esta configuração para que seja ou não enviada a notificação. O sistema funciona corretamente sem esta customização.
    FF4 - Seria necessário a criação de telas e relatórios específicos para esta funcionalidade. Os professores e coordenadores enquanto a funcionalidade não estiver implementada poderão visualizar as notas dos alunos e entregas de atividades e tirarem suas conclusôes a partir delas. O processo necessário para o ensino pedagógico ocorrerá mesmo sem a funcionalidade, com ela sendo apenas uma facilitadora do processo.
