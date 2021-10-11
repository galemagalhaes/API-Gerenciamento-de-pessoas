
<h1>Entrega do Projeto</h1>
Este projeto foi realizado como parte do Bootcamp "GFT Java & AWS Developer". 

Inicialmente foi feita a configuração do ambiente de desenvolvimento utilizando a ferramenta SDKMan!, cuja função é facilitar o uso de diferentes versões do Java.
Após a configuração foram passados conceitos sobre o padrão de arquitetura REST e explicada a diferença entre REST e RESTful. Esse último se refere ao nível de maturidade
seguindo o padrão. Esses níveis vão de 0 a 3 (portanto são 4 níveis) no modelo de maturidade Richardson.

O próximo passo foi criar o projeto inicial, para isso foi usado o Spring Initializr. Para este projeto foram usadas as dependências:
* Spring Boot DevTools;
* Lombok;
* Spring Web;
* Spring Data JPA;
* Spring Boot Actuator;
* H2 Data Base.

Em seguida foi feita a configuração do Intellij, com a inclusão do JDK 11 na estrutura do projeto (Project Structure).
Depois foi feita também a configuração de execução e debug selecionando a classe principal de entrada coma a anotação @SpringBoot.
Ainda foram utilizadas e explicadas as seguintes anotações:
* @RestController - controlador acessado através de uma API REST
* @RequestMapping - caminho principal de acesso (nível 1 de maturidade Richardson)
* @GetMapping - verbo HTTP Get

Na sequência foi demonstrado como fazer deploy na nuvem com Heroko e habilitado deploy automático, pois a proposta era fazer 
as entregas do projeto por partes. O deploy feito a cada funcionalidade completa. Foi necessário fazer uma configuração
para o Heroko, pois, por padrão (à época da aula), ele detecta até Java 8, portanto, versões mais recentes necessitam da 
seguinte configuração:
* Sistem Properties --> java.runtime.version=11

A próxima etapa foi fazer a modelagem de dados.

Foi demonstrado o uso do Lombok com as seguintes anotações:
* @Data - insere automaticamente getters e setters;
* @Builder - padrão de projeto para construção;
* @AllArgsConstructor e @NoArgsConstructor - para inserir construtores;
* @Entity - para a identidade;
* @Id com @GeneratedValue - para gerar Id incremental pelo banco de dados.

O uso do Lombok deixa o código mais elegente e facilita sua manutenção, reduz o tamanho do código deixando-o mais limpo.
Outras anotações do Lombok podem ser acessadas no link de documentação na sessão de links no final deste documento.



Durante seu desenvolvimento foram usadas ferramentas como o SDKMan, Maven, entre outras, que tive dificuldade em configurar na minha máquina.
Razão pela qual estou entregando o projeto original ao invés de uma réplica codada por mim.
No momento planejo formatar minha máquina, pois essa não é a primeira vez que tenho esse tipo de problema,
e quero em seguida refazer as instalações necessárias e o projeto por inteiro. No entanto,
como tenho prazo para finalizar o curso, optei por usar essa estratégia para poder seguir em frente
com o Bootcamp.

A seguir estão as especificações originais do projeto.


<h2>Digital Innovation: Expert class - Desenvolvendo um sistema de gerenciamento de pessoas em API REST com Spring Boot</h2>

Nesta live coding vamos desenvolver um pequeno sistema para o gerenciamento de pessoas de uma empresa através de uma API REST, criada com o Spring Boot.

Durante a sessão, serão desenvolvidos e abordados os seguintes tópicos:

* Setup inicial de projeto com o Spring Boot Initialzr 
* Criação de modelo de dados para o mapeamento de entidades em bancos de dados
* Desenvolvimento de operações de gerenciamento de usuários (Cadastro, leitura, atualização e remoção de pessoas de um sistema).
* Relação de cada uma das operações acima com o padrão arquitetural REST, e a explicação de cada um dos conceitos REST envolvidos durante o desenvolvimento do projeto.
* Desenvolvimento de testes unitários para validação das funcionalidades
* Implantação do sistema na nuvem através do Heroku

Para executar o projeto no terminal, digite o seguinte comando:

```shell script
mvn spring-boot:run 
```

Após executar o comando acima, basta apenas abrir o seguinte endereço e visualizar a execução do projeto:

```
http://localhost:8080/api/v1/people
```


São necessários os seguintes pré-requisitos para a execução do projeto desenvolvido durante a aula:

* Java 11 ou versões superiores.
* Maven 3.6.3 ou versões superiores.
* Intellj IDEA Community Edition ou sua IDE favorita.
* Controle de versão GIT instalado na sua máquina.
* Conta no GitHub para o armazenamento do seu projeto na nuvem.
* Conta no Heroku para o deploy do projeto na nuvem
* Muita vontade de aprender e compartilhar conhecimento :)

Abaixo, seguem links bem bacanas, sobre tópicos mencionados durante a aula:

* [SDKMan! para gerenciamento e instalação do Java e Maven](https://sdkman.io/)
* [Referência do Intellij IDEA Community, para download](https://www.jetbrains.com/idea/download)
* [Palheta de atalhos de comandos do Intellij](https://resources.jetbrains.com/storage/products/intellij-idea/docs/IntelliJIDEA_ReferenceCard.pdf)
* [Site oficial do Spring](https://spring.io/)
* [Site oficial do Spring Initialzr, para setup do projeto](https://start.spring.io/)
* [Site oficial do Heroku](https://www.heroku.com/)
* [Site oficial do GIT](https://git-scm.com/)
* [Site oficial do GitHub](http://github.com/)
* [Documentação oficial do Lombok](https://projectlombok.org/)
* [Documentação oficial do Map Struct](https://mapstruct.org/)
* [Referência para o padrão arquitetural REST](https://restfulapi.net/)

[Neste link](https://drive.google.com/file/d/1crVPOVl6ok2HeYjh3fjQuGQn2lDZVHrn/view?usp=sharing), seguem os slides apresentados como o roteiro utilizado para o desenvolvimento do projeto da nossa sessão.



