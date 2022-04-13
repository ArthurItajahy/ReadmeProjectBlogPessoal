# GÊNIO INDOMÁVEL
![GitHub](https://img.shields.io/github/license/ArthurItajahy/ReadmeProjectBlogPessoal)
# Menu
<!--ts-->
   * [Apresentação do Projeto](#Apresentacao)
       * [Motivação](#Motivacao)
       * [Tecnologia](#Tecnologias)
   * [Back-End](#Back-End)
       * [Parte 1 - Escolhendo Entidades](#Parte-1-Escolhendo-Entidades)
       * [ Parte 2 - Aplicando Spring boot](#Parte-2-Aplicando-No-Spring-Boot)
       * [ Parte 3 - Teste no insominia](#Parte-3-Teste-No-Insominia)
   * [Front-End](#Front-End)
        * [Parte 1 - Criando Tela de Login e Cadastro](#Parte-1-Criando-Tela-de-Login-e-Cadastro)
        * [Parte 2 - Criando home e Perfil](#Parte-2-Criando-Home-e-Perfil)
     <!--te-->

# Apresentacao

 ### Motivacao:
 
 ##### "Há ideia era juntar um grupo de pessoas extraordinárias e ver se eles trabalhando em equipe poderiam ser algo mais." - Nick Fury.
 
 Esse projeto foi construído com o intuito de mostrar o meu melhor, por isso coloquei tudo que eu  sabia até o momento para cria-lo. 
 Escolhi o nome gênio indomável pois queria criar uma comunidade de pessoas Gênias que estivessem prontas para ajudar o mundo por puro altruísmo.  E meu blog poderia ser capaz de dar esse pontapé inicial para que eu pudesse ir expandindo. 
 
 ### Tecnologias:
 
 Essas  tecnologias foram escolhidas pela segurança e o vasto conteúdo documentado na internet para que pudesse me dar suporte ao longo do processo, por serem tecnologias extremamente conhecidas me senti complemente confortável em usa-las. Essas tecnologias são amplamente usadas pelo mercado dessa forma o projeto estaria mais alinhado com o ambiente profissional.
        
<table>
    <tr> 
        <td><img alt="Java" src="https://img.shields.io/badge/java-%23ED8B00.svg?&style=for-the-badge&logo=java&logoColor=white"/></td>
        <td><img alt="Spring" src="https://img.shields.io/badge/spring-%236DB33F.svg?&style=for-the-badge&logo=spring&logoColor=white"/></td>
        <td><img alt="Material UI" src="https://img.shields.io/badge/Material--UI-0081CB?style=for-the-badge&logo=material-ui&logoColor=white"/></td>
        <td><img alt="MySQL" src="https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white"/></td>
        <td><img alt="React" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/></td>
        <td><img alt="HTML" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/></td>
        <td><img alt="CSS" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/></td>
        <td><img alt="TYPESCRIPT" src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white"/></td>
        </tr>
</table>  

#### Sites para deploy do projeto:

 <table>
     <tr>
             <td><img alt="Netlify" src="https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white"/></td>
        <td><img alt="Heroku" src="https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white"/></td> 
     </tr>
 </table>
 
 # BACK-END:
 
 ### Parte-1-Escolhendo-Entidades:

Essa parte foi tranquila pois como queria começar um projeto que pudesse crescer depois, optei por pelo simples e usar apenas três entidades. Postagens, Temas e Usuário. Tendo a oportunidade de expandir as coisas depois, fiz essa divisão usando MySql para que ficasse mais visual a interação das entidades.


![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/entidade.png) 

### Parte-2-Aplicando-No-Spring-Boot:


Primeiro tivemos que usar padrões de projetos como MVC(Model, View e Controller), mas fazendo algumas adaptações para o nosso projeto pois ele iria ter outras camadas de complemento que no caso seriam Model, Repository, Controller,Security e Service.

##### Model => Ira criar os modelos das nossa entidades definidas(Postagem, Usuário, Tema) ou seja também criando as ligações que as tabelas iram ter.

##### Repository => Será os filtros que iremos requisitar do banco de dados, para podermos visualizar os dados que precisamos.

##### Controller => Aqui será onde iremos reunir os Comandos HTTP (GET, POST, DELETE e PUT), o que ira nos possibilitar em fazer o famoso CRUD.

##### Service => Onde iremos colocar a nossa regra de negocio para que possamos permitir ou negar os dados que serão mandados para o banco de dados.

##### Security => Aqui é a segurança da Aplicação, onde iremos criptografar os dados sensíveis e proteger nossa aplicação usando JWT.

Após a separação das camadas instalamos as dependências necessárias.

#### Dependências usadas:

=> SpringBoot Starter data JPA

=> Spring Boot Starter-Validation

=> SpringBoot Starter Web

=> SpringBoot Starter Security

=> Commons Codec

=> MySql-ConnectorJava

=> Spring Boot DevTools

=> postgreSql

=> SpringBootStarterTest JUnit 

=> H2 Database.


Com as dependências instaladas criamos as Models, Repositorios, Services, Controller  e finalizamos colocando a Security.  Ao completar o código fiz alguns testes unitários usando JUnit e H2 database.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/TesteJUNIT.png) 


### Link do código:  https://github.com/ArthurItajahy/Blog

### Parte-3-Teste-No-Insominia:

#### Teste de cadastro: Aqui mostramos o cadastro funcionando, após o usuário ser cadastro sua senha é criptografada e envia para o banco de dados.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/Cadastro.png) 

#### Teste de Login: Quando o Login é efetuado, observe que o token de acesso é gerado para o usuário, mas aqui usamos model virtual onde esse token não guardado no banco de dados e sim colocando em espelho do modelo do usuário. Assim fazendo o token existir apenas quando o usuário está logado.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/Login.png) 

#### Fizemos vários outros testes e depois fizemos o deploy no heroku, caso você queira fazer os seus próprios testes, acesse o link a baixo. 

<img alt="Heroku" src="https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white"/>

 Link:https://genioindomavel.herokuapp.com

Para fazer o Login: 

usuário: root

senha: root





