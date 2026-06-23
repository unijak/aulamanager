# Arquitetura de Software

## Arquitetura Escolhida

Para o desenvolvimento do Aula Manager foi adotada a **Arquitetura em Camadas**, devido à sua simplicidade, organização e adequação ao contexto do projeto.

Essa arquitetura promove a separação de responsabilidades entre os diferentes componentes do sistema, facilitando a manutenção, evolução e compreensão da solução.

A estrutura proposta é composta pelas seguintes camadas:

### Camada de Apresentação

Responsável pela interação com os usuários do sistema, fornecendo as interfaces utilizadas por professores, estudantes e administradores.

Principais responsabilidades:

* Exibição das informações;
* Recebimento das ações dos usuários;
* Comunicação com a API do sistema.

### Camada de Negócio

Responsável pela implementação das regras de negócio e funcionalidades do sistema.

Principais responsabilidades:

* Gestão de turmas;
* Gestão de atividades;
* Gestão de missões de aprendizagem;
* Controle de permissões;
* Processamento das regras de negócio.

### Camada de Persistência

Responsável pelo acesso e manipulação dos dados armazenados.

Principais responsabilidades:

* Consultas ao banco de dados;
* Inserção de registros;
* Atualização de informações;
* Remoção de dados.

### Banco de Dados

Responsável pelo armazenamento permanente das informações do sistema.

Principais dados armazenados:

* Usuários;
* Turmas;
* Atividades;
* Missões de aprendizagem;
* Entregas;
* Avaliações.

---

## Justificativa da Escolha

A Arquitetura em Camadas foi escolhida por apresentar baixo nível de complexidade e atender adequadamente às necessidades do MVP proposto.

Além disso, a separação entre interface, regras de negócio e persistência facilita futuras manutenções e permite a evolução gradual da solução sem grandes impactos nos demais componentes.

Considerando o porte do projeto e os requisitos identificados, arquiteturas mais complexas, como Microserviços ou Publish-Subscribe, não se mostraram necessárias neste momento.

---

## Relação com o Modelo C4

A arquitetura definida está diretamente refletida nos diagramas C4 produzidos para o projeto.

No Nível de Contexto são apresentados os usuários e sistemas externos que interagem com o Aula Manager.

No Nível de Containers são representados os principais componentes da solução:

* Frontend Web;
* Backend API;
* Banco de Dados;
* Serviço de Notificações por E-mail.

Esses elementos implementam as responsabilidades previstas nas camadas da arquitetura adotada.

---

# Decisões Arquiteturais

## DA01 – Utilização da Arquitetura em Camadas

### Justificativa

A Arquitetura em Camadas foi escolhida por proporcionar uma clara separação de responsabilidades entre interface, regras de negócio e persistência de dados, facilitando a manutenção e evolução do sistema.

---

## DA02 – Controle de Acesso Baseado em Perfis

### Justificativa

O sistema possui diferentes tipos de usuários, cada um com responsabilidades específicas.

Foram definidos os seguintes perfis:

* Professor;
* Estudante;
* Administrador.

Essa abordagem garante que cada usuário tenha acesso apenas às funcionalidades compatíveis com sua função.

---

## DA03 – Missões de Aprendizagem como Elemento Central do Sistema

### Justificativa

As Missões de Aprendizagem representam o principal diferencial do Aula Manager.

A adoção desse conceito permite organizar conteúdos e atividades em trilhas estruturadas de aprendizagem, promovendo melhor acompanhamento do progresso dos estudantes e maior organização do processo educacional.

---

## DA04 – Utilização de Serviço de Notificações por E-mail

### Justificativa

Foi prevista a integração com um serviço de envio de e-mails para notificar usuários sobre novas atividades, missões, avaliações e atualizações relevantes.

Essa decisão melhora a comunicação entre os participantes e reduz o risco de perda de informações importantes.

