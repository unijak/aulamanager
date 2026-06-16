# Regras de Negócio

## RN01 – Apenas professores podem criar turmas

Somente usuários com perfil de professor podem criar novas turmas no sistema.

Impactos

* User Story: Criar Turma
* Caso de Uso: Criar Turma
* Necessidade de autenticação e controle de permissões


## RN02 – Apenas estudantes matriculados podem acessar uma turma

O acesso aos conteúdos, atividades e missões de uma turma será permitido apenas aos estudantes matriculados nela.

Impactos

* Caso de Uso: Ingressar em Turma
* Controle de autorização
* Segurança das informações acadêmicas


## RN03 – Apenas professores podem criar atividades

A publicação de atividades é uma responsabilidade exclusiva dos professores.

Impactos

* User Story: Criar Atividade
* Caso de Uso: Publicar Atividade
* BPMN de publicação de atividade


## RN04 – Atividades devem possuir prazo de entrega

Toda atividade cadastrada deverá conter uma data limite para envio.

Impactos

* Processo de entrega de atividades
* Controle de datas pelo sistema


## RN05 – Estudantes só podem entregar atividades dentro do prazo

Após o encerramento do prazo definido pelo professor, novas entregas não serão aceitas.

Impactos

* BPMN de entrega de atividades
* Validação de regras no backend


## RN06 – Apenas professores podem atribuir notas

Somente professores responsáveis pela turma poderão corrigir atividades e registrar notas.

Impactos

* Caso de Uso: Corrigir Atividade
* Controle de permissões


## RN07 – Uma missão deve possuir pelo menos uma atividade

Para ser publicada, uma missão de aprendizagem deverá conter ao menos uma atividade vinculada.

Impactos

* Funcionalidade de Missões
* Validação durante a criação de missões


## RN08 – O progresso da missão deve ser atualizado automaticamente

Sempre que uma atividade pertencente a uma missão for concluída, o sistema deverá atualizar automaticamente o percentual de progresso do estudante.

Impactos

* Funcionalidade de acompanhamento de progresso
* Atualização automática dos dados da missão
* Interface de acompanhamento do estudante
