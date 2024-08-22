# mysql

-- BANCO DE DADOS ESCOLA

create database escola
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI; 

-- TABELA DOS ALUNOS

create table alunos (
id int not null auto_increment,
nome varchar (30) not null,
nascimento date,
turma varchar (2),
email varchar (50),
primary key(id)
)default charset = utf8mb4;

-- INSERINDO O ALUNO

insert into alunos
(id, nome, nascimento, turma, email)
values
(default, 'Miya','2006-04-21','8A','miyamatadoradeporco@gmail.com');

-- TABELA DOS PROFESSORES

create table professores (
id int not null auto_increment,
nome varchar (30) not null,
disciplina varchar (30) not null,
salario decimal (5,2),
primary key (id)
) default charset = utf8mb4;

-- INSERINDO OS PROFESSORES

insert into professores values
(default, 'Luiz','Programação','3.370'),
(default, 'Vinicius','Redes','3.370');

-- -------------------------------------------|

-- BANCO DE DADOS BIBLIOTECA

create database biblioteca
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;

-- TABELA DOS LIVROS

create table livros (
id int not null auto_increment,
titulo varchar (50),
autor varchar (30),
ano_de_publicação decimal (4,3),
disponivel boolean not null,
primary key (id)
) default charset = utf8mb4;

-- INSERINDO OS LIVROS

insert into livros values
(default, 'Chapeuzinho Vermelho','Charles Perrault','1.697',1),
(default, 'Pequeno Principe','Antoine de Saint-Exupéry','1.943',0),
(default, 'Dom Quixote','Miguel de Cervantes','1.605',0);

-- -------------------------------------------|

-- BANCO DE DADOS EMPRESA

create database empresa
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;

-- TABELA DOS FUNCIONARIOS

create table funcionarios (
id int not null auto_increment,
nome varchar (30),
salario decimal (4,3),
data_de_admição date,
primary key (id)
) default charset = utf8mb4;

-- INSERINDO O FUNCIONARIO

insert into funcionarios values
(default, 'Carlos','3.500','2026-05-30');

-- BANCO DE DADOS CINEMA

create database cinema
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;

-- TABELA DOS FILMES

create table filmes (
id int not null auto_increment,
titulo varchar (50),
diretor varchar (30),
gênero varchar (20),
duração int not null,
classificação_etaria tinyint not null,
primary key (id)
) default charset = utf8mb4;

-- INSERINDO OS FILMES	

insert into filmes values
(default, 'It a Coisa','Andy Muschietti','Terros/Misterio', '135', '18'),
(default, 'It a Coisa 2','Andy Muschietti','Terros/Misterio', '169', '18');

-- BANCO DE DADOS MUSICA

create database musica
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;

create table albuns (
id int not null auto_increment,
nome varchar (50),
artista varchar (30),
ano_de_lançamento decimal (4,3),
gênero varchar (20),
primary key (id)
) default charset = utf8mb4;

-- INSERINDO OS ALBUNS

insert into albuns values
(default, 'Chicken of Death','Massacration','2.005', 'heavy metal'),
(default, 'Good Blood Headbangers','Massacration','2.009', 'heavy metal');

--                                                                                              DESAFIO                                                                                                                              --

-- BANCO DE DADOS ANIMAÇÃO JAPONESA

create database Anime
default character set UTF8MB4
default collate UTF8MB4_GENERAL_CI;  

-- TABELA DAS OBRAS

create table obras (
id int not null auto_increment,
Titulo varchar (50),
Autor varchar (30),
Gênero varchar (20),
Plataforma varchar (30),
Data_de_Estreia date,
Editora varchar (30),
primary key(id)
) default charset = utf8mb4;

-- INSERINDO AS OBRAS

insert into obras values
(default, 'One Piece','Eiichiro Oda','Shonen','Crunchyroll, HBO Max, Netflix e Prime Video','1999-10-20', 'Shōnen Jump'),
(default, 'Fullmetal Alchemist: Brotherhood','Hiromu Arakawa','Shonen','Netflix, Prime Video e Crunchyroll','2009-04-05','Shonen Gangan'),
(default, 'Vinland Saga','Makoto Yukimura','Seinen','Crunchyroll e Netflix','2023-01-09','seinens Afternoon'),
(default, 'Dragon Ball Z','Akira Toriyama','Shonen','Prime Video','1989-04-26','Shōnen Jump');
