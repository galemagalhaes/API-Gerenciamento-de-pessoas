# API-Gerenciamento-de-pessoas
#
Este projeto foi realizado como parte do Bootcamp "GFT Java & AWS Developer".
As etapas desse projeto serão descritas em seguida:
#

***Configuração do ambiente*** de desenvolvimento utilizando a ferramenta SDKMan!, cuja função é facilitar o uso de diferentes versões do Java.
#

***Conceitos sobre o padrão de arquitetura REST*** e explicada a diferença entre REST e RESTful. Esse último se refere ao nível de maturidade seguindo o padrão. Esses níveis vão de 0 a 3 (portanto são 4 níveis) no modelo de maturidade Richardson.

#
***Criação o projeto inicial*** usando o Spring Initializr. Para este projeto foram usadas as dependências:

Spring Boot DevTools;
* Lombok;
* Spring Web;
* Spring Data JPA;
* Spring Boot Actuator;
* H2 Data Base.


#
***Configuração do Intellij*** com a inclusão do JDK 11 na estrutura do projeto (Project Structure) e a configuração de execução e debug selecionando a classe principal de entrada coma a anotação @SpringBoot. Ainda foram utilizadas e explicadas as seguintes anotações:

<ins>*@RestController*</ins> - controlador acessado através de uma API REST

<ins>*@RequestMapping*</ins> - caminho principal de acesso (nível 1 de maturidade Richardson)

<ins>*@GetMapping*</ins> - verbo HTTP Get

#
***Modelagem de dados*** tabela Person e Phone e seus relacionamentos.

#
***Uso do Lombok*** com as seguintes anotações:

<ins>*@Data*</ins> - insere automaticamente getters e setters;

<ins>*@Builder*</ins> - padrão de projeto para construção;

<ins>*@AllArgsConstructor*</ins> e <ins>*@NoArgsConstructor*</ins> - para inserir construtores;

<ins>*@Entity*</ins> - para a identidade;

<ins>*@Id*</ins> com <ins>*@GeneratedValue*</ins> - para gerar Id incremental pelo banco de dados.


O uso do Lombok deixa o código mais elegente e facilita sua manutenção, reduz o tamanho do código deixando-o mais limpo. Outras anotações do Lombok podem ser acessadas no link de documentação na sessão de links no final deste documento.

#
***Mapeamento da aplicação*** com uma criação básica.

#
***Deploy na nuvem com Heroko*** e habilitado deploy automático, pois a proposta era fazer as entregas do projeto por partes. O deploy feito a cada funcionalidade completa. Foi necessário fazer uma configuração para o Heroko, pois, por padrão (à época da aula), ele detecta até Java 8, portanto, versões mais recentes necessitam da seguinte configuração:

*Sistem Properties ==> java.runtime.version=11*

#
***Refatoração do código*** com a criação de DTOs - Objetos para transição de dados com o objetivo de fazer validações na camada de controle por meio de anotações, incluindo CPF no formato brasileiro. Uso da lib Map Struct para conversão de formato string para formato date por uma única interface DTO Entity.

#
***Criação de exceptions***

#
***Melhoramento do código*** que não pode ser chamada de refatoração, pois para isso seria necessário fazer testes unitários usando lambda do Java. Esse melhoramento inclui renomear variáveis para maior clareza do código.

#
***Implementação do Delete e Put*** lembrando que Put é para atualização completa, para uma atualização parcial seria usado o verbo HTTP Patch, que não foi abordado no curso.

#
***Dicas sobre processos seletivos*** e a relevância da documentação do código e a importância do arquivo README.

#
***Um pouco sobre testes*** com a implementação de testes unitários na classe createPerson e explicação sobre como deve ser aplicada a cobertura por testes:

* Regras de negócio essenciais que não possam ser quebradas durante uma refatoração ou manutenção do código;
* Bugs.

Ou seja, algumas partes do código não tem a necessidade de teste, esses devem ser feitos nas partes mais relevantes para a aplicação, o negócio ou o cliente.

#
***Indicação de materiais para estudo***, incluindo testes, além de outros verbos HTTP, annotations, referências e atalhos.

Durante o desenvolvimento foram usadas ferramentas como o SDKMan, Maven, entre outras, que tive dificuldade em configurar na minha máquina, razão pela qual estou entregando o projeto original ao invés de uma réplica codada por mim. No momento busco soluções para esse problema, pois essa não é a primeira vez que isso ocorre. No entanto, como tenho prazo para finalizar o curso, optei por usar essa estratégia para poder seguir em frente com o Bootcamp.
