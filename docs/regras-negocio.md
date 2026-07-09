RN01: Estudantes só podem visualizar as turmas que estão matriculados.
  O sistema mostrará para o estudante apenas as turmas em que ele está vinculado.
  
RN02: Estudante não pode alterar uma atividade após o encerramento do prazo de entrega.
  Quando a atividade possuir prazo de entrega, o estudante deverá postá-la e alterá-la neste período. Após a data de entrego sistema
  não permitirá novos envios ou alterações.

  Possíveis Impactos:

  User Story:

  US05 - Como estudante, quero enviar meus trabalhos para cumprir as atividades propostas pelo professor.

  Casos de Uso:

  Enviar Trabalho

  BPMN:

  Antes de registrar o envio, o sistema deve verificar se o prazo da atividade ainda está válido.

  Arquitetura:

  Necessidade de armazenar data de entrega e realizar validação de regras no processamento das atividades.

  Requisito Não Funcional:

  Integridade dos dados e confiabilidade das informações acadêmicas.

RN03: Apenas professores podem atribuir ou alterar notas e atividades.
  As notas e atividades só poderão ser registradas ou modificadas pelo professor cadastrado como o responsável pela turma.

  Possíveis Impactos:

  User Story:

  US04 - Como professor, quero publicar atividades para que os estudantes possam acessá-las.

  US04 - Como professor, quero registrar notas das avaliações para acompamahar o desempenho dos estudantes.

  Casos de Uso:

  Publicar Atividade

  Registrar Nota

  BPMN:
  
  As etapas de criação de atividades e lançamento de notas são executadas exclusivamente pelo professor.

  Arquitetura:

  Necessidade de autenticação e controle de permissões de acesso por perfil de usuário.

  Requisito Não Funcional:

  Segurança e controle de autorização.

RN04: O Sistema terá a opção de notificar os estudantes ou não sobre as novas atividades.
  O Estudante terá a opção de escolher se deseja que o sistema o notifique quando houver novas atividades postadas na turma.

RN05: Apenas usuários vinculados a uma turma podem acessar seus conteúdos.
  O sistema deve permitir que estudantes e professores acessem apenas as turmas nas quais possuem vínculo cadastrado.
  
RN06: As notas e atividades devem estar associadas à turma correspondente.
  O sistema dee garantir que atividades, entregas e notas sejam vinculadas corretamente à turma em que foram criadas,
  evitando registros em disciplinas ou turmas incorretas.
