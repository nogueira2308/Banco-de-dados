# Banco-de-dados
Criei um código cadastrando clientes direto no terminal do Xampp utilizando Mysql
Criando um banco de dados direto no terminal

mysql -u root -p

show databases; /* Permite que você visualize o banco de dados*/

create database 33ti;

use 33ti;

create table clientes
(id bigint auto_increment primary key,
nome varchar(100) not null, /* o not null indica que esse campo não pode estar vazio */
email varchar(100) unique, /* o unique indica que não pode ser cadastrado o mesmo email*/
data nascimento date, /* o formato date é o mesmo que a do USA Ano- MÊs- Dia*/
saldo decimal(10,2));

show tables; /* Permite que você visualize a tabela*/

describe clientes; /*descreve o conteúdo que você criou na tabela*/

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Maria Oliveira',
'mariaoliveir@exemple.com',
'1990-07-20',
3000.75);

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Joao Silva',
'joaosilva@exemple.com',
'1985-01-12',
10250.30);

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Lucas Verdade',
'lucasverdade@exemple.com',
'1992-08-25',
9250.90);

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Vladimir Boavista',
'vladimirboavista@exemple.com',
'1987-01-06',
5204.75);

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Isolete Paiva',
'isoletepaiva@exemple.com',
'1995-02-20',
1000.30);

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Veronica Assun',
'veronicaassun@exemple.com',
'1996-04-16',
6359.15);


insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Junior Tudobem',
'Juniortudobem@exemple.com',
'1996-03-03',
4000.58);

insert into clientes(
nome,email,data_nascimento,saldo)
values(
'Erico Verissimo',
'ericiverissimo@exemple.com',
'2000-09-09',
7856.54);

select * from clientes; /* mostra o que foi inserido na tabela/*

update clientes /* Alterando dados*/
set saldo = saldo + 250.00
where email = 'maria@gmail.com';

select * from clientes;

select nome,email,data_nascimento,saldo from clientes order by nome asc /* Organiza os nomes em ordem crescente */

delet from clientes where id = 5; /*deleta o id 5 na tabela*/








