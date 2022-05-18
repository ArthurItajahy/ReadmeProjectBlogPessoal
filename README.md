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
   * [Atualizações Futuras](#Atualizacoes-Futuras)
   * [Agradecimentos](#Agradecimentos)
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

### Parte-3-Teste-No-Insominia:

#### Teste de cadastro: Aqui mostramos o cadastro funcionando, após o usuário ser cadastro sua senha é criptografada e envia para o banco de dados.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/Cadastro.png) 

#### Teste de Login: Quando o Login é efetuado, observe que o token de acesso é gerado para o usuário, mas aqui usamos model virtual onde esse token não guardado no banco de dados e sim colocando em espelho do modelo do usuário. Assim fazendo o token existir apenas quando o usuário está logado.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/Login.png) 

#### Fizemos vários outros testes e depois fizemos o deploy no heroku, caso você queira fazer os seus próprios testes, acesse o link a baixo. 

<img alt="Heroku" src="https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white"/>

#### Deploy na Nuvem:https://genioindomavel.herokuapp.com

=====L O G I N=====

    usuário: root

    senha: root

=================


#### Codigo do projeto back-end:  https://github.com/ArthurItajahy/Blog


# Front-End

No front-end também usamos o padrão MVC(Model,View e Controller), primeiro tive que dividir o que seria feito pois tinha que construir muitas coisas, por isso decidi dividir o projeto em duas grandes partes. 

Dependências usadas: 

## instalação do material ui



yarn add @material-ui/core@4.12.3

yarn add @material-ui/icons@4.11.2

yarn add @mui/icons-material@5.0.5
 
yarn add @material-ui/lab@4.0.0-alpha.60

yarn add @emotion/react@11.5.0

yarn add @emotion/styled@11.3.0

yarn add @mui/material@5.0.6


## instalação do react-router-dom

yarn add react-router-dom@5.3.0

yarn add @types/react-router-dom@5.1.8
 
## instalação do axios 

yarn add axios@0.21.4

## instalação do useLocalStorage 

npm i react-use-localstorage@3.5.3

## instalação do redux

yarn add @types/redux@3.6.0 react-redux@7.2.5

## instalação do react-toastify

npm install --save react-toastify@8.0.3


### Parte-1-Criando-Tela-de-Login-e-Cadastro 

Bom, o que você vai ver abaixo já é o produto final sujeito a mudanças, o login foi construído para pegar os dados de email e senha com esses dados, o login faz a requisição para o banco de dados  e compara os dados para ver se existe algum usuário compatível, ele espera o retorno do banco de dados, caso o usuário exista ele manda o usuário para o Home com o token gerado. Se o usuário não existir ele retorna um Alerta.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/telalogin.gif)


#### Essa é a pagina de cadastro, dessa forma você pode observar que você pode colocar link da foto do seu usuario.. Insira seu nome, email e senha. Pronto seu cadastro de está feito.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/telacadastro.gif)


### Parte-2-Criando-Home-e-Perfil

#### Mostrando o home onde você podera criar a seus temas e suas postagens que estaram diretamente ligadas a seu usuario. (No futuro poderemos implementar para que outros usuario não possa apagar sua postagem)

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/telahome.gif)

#### O perfil do usuario onde ira estar sua foto. ele pode ter acesso a todas as postagens já feitas.

![Web 1](https://github.com/ArthurItajahy/ReadmeProjectBlogPessoal/blob/main/assets/forReadme/telaperfil.gif)


#### O Deploy foi efetuado no Netlify.
<img alt="Netlify" src="https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white"/>

#### Crie o seu perfil também e faça sua postagem acessando o link a baixo.

#### Deploy na nuvem: https://genioindomavel.netlify.app



#### Codigo do projeto front-end: https://github.com/ArthurItajahy/Blog_pessoal_FrontEnd


# Atualizacoes-Futuras

#### => Funcionalidade para Atualizar o Perfil.

#### => Funcionalidade para apenas o usuario que postou poder apagar.

#### => Curtidas para as postagens.

#### => Fotos para as postagens.

#### => Reconstruir o back-end em microserviço para ter mais escalabilidade e segurança.

#### => E reescrever em Kotlin para o mobile.


## Agradecimentos.




#### Bom, esse projeto não seria possível sem os ensinamentos adquiridos no bootcamp da Generation Brasil . O bootcamp foi focado em capacitar as pessoas para se tornarem Desenvolvedores Java Full Stack Junior. Ensinando todo o caminho necessário para que isso se torna-se realidade.



#### Quero agradecer a o instrutor Luis Guerreiro que me ensinou logica da programação desde o Portugol e fazendo uma transição desses conhecimentos para Java, depois introduzindo o conceito de OOP. Após esse conhecimento adquirido fomos divididos em grupos para criar um projeto em equipe para consolidar os conhecimentos na linguagem.



#### Após isso o instrutor  Rafael Queiroz, ensinou sobre bancos relacionais usando a ferramenta MySQL. Depois fui apresentado por ele ao framework Spring boot para facilitar na criação de projetos com Java. Ensinou sobre Padrões de projeto em camadas. Com conclusão criamos dessa parte subimos os projetos no Heroku.



#### No final o instrutor Yuri Oliveira apresentou o Front-End, passando pelo básico HTML, CSS e Javascript. Com os conhecimentos consolidados fomos guiados a facilitar nosso desenvolvimento e começamos a usar uma biblioteca chamada React. onde os conhecimentos foram usando para construir o Front-End desse Blog. Então subi o resultado final no Netlify.



#### Jacqueline Hernandes que teve o papel de ser nossa instrutora de Jornada, nos auxiliou muito quando estávamos perdidos e ensinou para gente como devemos nos comportar em ambiente profissional. Acredito que nenhum outro bootcamp deu tanta importância para a forma que convivemos em sociedade.



#### Agradeço a Turma 44 por serem tão incríveis. E Principalmente ao meu grupo do Projeto Integrador(PI), Aline A. Lopes, Amanda Cristine Soares de Barros, Amaury Wagner Erick Ferreira, Felipe Carvalho e Larissa. Vocês me ensinaram como liderar um grupo, saber lidar com pessoas de diferentes tipos de pensamento, conhecimento e cultura



#### E o meu ultimo agradecimento vai para Generation Brasil. O trabalho social de vocês me tornou um Desenvolverdo Java Full Stack, mais acima disso me tornou um ser humano melhor.




