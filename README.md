# Prova prática de sql

##
# Criação das tabelas:
## TB_ALUNO:
````sql
create table tb_aluno(
   cod_aluno int primary key,
	nome_aluno varchar(50) NOT NULL,
	ano_nascimento date,
	e_mail varchar(60),
	sexo varchar NOT NULL
);
````
## TB_CURSO:
````sql
create table tb_curso (
   cod_curso int primary key,
	nome_curso varchar (60) NOT NULL
);
````
## TB_MATRICULAS:
````sql
create table tb_matriculas (
   cod_curso int references tb_curso (cod_curso),
	cod_aluno int references tb_aluno (cod_aluno)
);
````

# Inserção dos dados nas tabelas:
## INSERT TB_ALUNO:
````sql
insert into tb_aluno (cod_aluno, nome_aluno, ano_nasc, e_mail, sexo)
values (1, 'Josiel Jardim', 1974, 'josiel@provaSQL.com.br', 'M');
insert into tb_aluno (cod_aluno,nome_aluno,ano_nasc,e_mail,sexo)
values(2, 'Ana Maria', 1980, 'ana@provaSQL.com.br', 'F');
insert into tb_aluno (cod_aluno, nome_aluno, ano_nasc, e_mail, sexo)
values(3, 'João Pedro', 1979, 'joao@provaSQL.com.br', 'M');
````
## INSERT TB_CURSO:
````sql
insert into tb_curso (cod_curso, nome_curso)
values(1,'Medicina');
insert into tb_curso (cod_curso, nome_curso)
values(2,'Arquitetura');
insert into tb_curso (cod_curso, nome_curso)
values(3,'Filosofia');
insert into tb_curso (cod_curso, nome_curso)
values(4, 'Informatica');
insert into tb_curso (cod_curso, nome_curso)
values(5,'Jornalismo');
````
## INSERT TB_MATRICULA:
````sql
insert into tb_matriculas (cod_curso, cod_aluno)
values(1,1);
insert into tb_matriculas (cod_curso, cod_aluno)
values(1,2);
insert into tb_matriculas (cod_curso, cod_aluno)
values(2,3);
insert into tb_matriculas (cod_curso, cod_aluno)
values(5,3);
````

## Questões práticas:
## Questão 01
Faça um comando SQL para matricular o aluno “Pedro César” no curso de Informática. Os dados devem ser inseridos na tabela TB_MATRÍCULA.
## Resolução
![quest1](https://user-images.githubusercontent.com/102304929/206206785-84a4aef8-9174-4c37-8668-9fc1be6d5072.png)

## Questão 02
Escreva um comando SQL que retorne os nomes dos alunos e do(s) cursos em que estão matriculados. Os dados deverão estar ordenados pelo nome do curso.
## Resolução
![quest2](https://user-images.githubusercontent.com/102304929/206207596-d8f4771f-f152-4a14-9086-87440d462bf8.png)

## Questão 03
Crie um comando SQL que retorne o e-mail de todos os alunos maiores de idade.
## Resolução
![quest3](https://user-images.githubusercontent.com/102304929/206208160-d9ad8e04-2364-4cb2-89d3-7716702a257a.png)

## Questão 04
Desenvolva um comando SQL que mostre o total de alunos.
## Resolução
![quest4](https://user-images.githubusercontent.com/102304929/206209376-e275773c-049f-42d4-8bdc-dc0377d703cf.png)

## Questão 05
Escreva um comando SQL para listar o total de alunos matriculador em cada curso.
## Resolução
![quest5](https://user-images.githubusercontent.com/102304929/206209962-683d5abd-cf6e-4bc3-bd5f-b087971d357a.png)

## Questão 06
Desenvolva um comando SQL que retorne o nome de todos os alunos maiores que 18 anos.
## Resolução
![image](https://user-images.githubusercontent.com/102304929/206316643-82f60ed0-5b2a-4fb2-8066-29d9454cc194.png)

## Questão 07
Faça um comando SQL que retorne o nome de todas as mulheres.
## Resolução
![quest7](https://user-images.githubusercontent.com/102304929/206317026-7cc8ac67-0b72-4196-840a-4829bec5fe50.png)

## Questão 08
Faça um comando SQL que retorne o nome de todas as mulheres matriculadas no curso de Medicina.
## Resolução
![quest8](https://user-images.githubusercontent.com/102304929/206317410-3fc79cdc-9fc3-4162-9ddf-c7f3e324e57a.png)

## Questão 09
Faça um comando SQL que retorne os nomes dos cursos ordenados por ordem alfabética.
## Resolução
![quest9](https://user-images.githubusercontent.com/102304929/206317689-96cf126c-ea65-4f4e-a0e2-f7b6ed4c38dd.png)

## Questão 10
Crie o enunciado de uma consulta SQL que utilize “junção” (com resposta).
## Resolução
![quest10](https://user-images.githubusercontent.com/102304929/206323842-8c95ec9a-a938-4482-89f0-c612daffbc91.png)

## Questões teóricas:

## Questão 1:
### Defina: SQL.
#### R: SQL significa Standard Query Language, literalmente a linguagem padrão para realizar queries.

## Questão 2:
### Faça um relacionamento cronológico sobre SQL.
#### R: A linguagem SQL surgiu em meados da década de 70, sendo resultado de um estudo de E. F. Codd, membro do laboratório de pesquisa da IBM em San Jose, Califórnia. Este estudo tinha foco em desenvolver uma linguagem que adapta-se ao modelo relacional. O primeiro sistema de BD baseado em SQL tornou-se comercial no final dos anos 70 juntamente com outros sistema de BD’s relacionais. O sucesso da linguagem SQL foi tão grande que obrigou o ANSI (American National Standarts Institute), a padronizar as implementações da linguagem, assim, nos dias de hoje, a maior parte de BD’s seguem criteriosamente esta padronização, podendo ter algumas variações, mais mesmo assim não afetando na padronização global da linguagem tornando assim a portabilidade mais fácil, se seguida de forma adequada pelo DBA. Em 1982, foi lançada a primeira versão padronizada da linguagem SQL, que vieram ganhando melhorias de acordo com sua evolução e tornando-se assim, a mais poderosa ferramenta para definição e manipulação de BD’s e hoje utilizada em grande parte dos BD existente, tais como MySQL, SQLServer, Firebird dentre outros.

## Questão 3:
### Liste as principais características de SQL.
#### R: SQL é uma linguagem padrão para trabalhar com bancos de dados relacionais. Ela é uma linguagem declarativa e que não necessita de profundos conhecimentos de programação para que alguém possa começar a escrever queries. A linguagem SQL é utilizada de maneira relativamente parecida entre os principais bancos de dados relacionais do mercado: Oracle, MySQL, MariaDB, PostgreSQL, Microsoft SQL Server, entre muitos outros. Cada um tem suas características, sendo o MySQL e o PostgreSQL extremamente populares por possuírem versões gratuitas e de código aberto.

## Questão 4:
### Descreva a sintaxe do comando SQL: SELECT. Quais cláusulas são obrigatórias e quais são opcionais?
#### R: O comando SELECT é utilizado para extrair os dados das tabelas de um banco de dados. Ele pode extrair dados de uma ou mais tabelas ao mesmo tempo, executando desde simples consultas até comandos mais complexos, fazendo buscas, junções, filtros comparativos, ordenações e diversos outros itens.

## Questão 5:
### Qual a importância da linguagem SQL no desenvolvimento de softwares atualmente? Justifique.
#### R: O SQL Server, criado pela Microsoft, é muito conhecido e utilizado no mercado. A linguagem usada nessa ferramenta é o T-SQL, e oferece recursos avançados e diferenciados para facilitar a atualização de dados e o armazenamento das informações de forma segura e confiável. O SQL Server atua com sistemas integrados de criptografia, permitindo que a visualização ou alteração das informações sejam feitas apenas pelas pessoas responsáveis, o que garante ainda mais segurança e tranquilidade para os usuários e empresários. É uma alternativa comumente utilizada em lojas online, instituições governamentais, bancos e indústrias dos mais diversos portes.
