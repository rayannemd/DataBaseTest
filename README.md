<h1> DataBase Test </h1>

This is a repository for my database test. If you want to interact with it, open the PostgreSQL on your computer and run the following codes.

<h2> Creating the database </h2>

```
create database bdescola 
```

<h2> Creating the tables </h2>

Creating the table 'tb_aluno'
```
create table tb_aluno( 

codigo_aluno integer primary key, 

nome_aluno varchar(60) not null, 

ano_nascimento int, 

email varchar(60), 

sexo varchar not null 

)  
```
Creating the table 'tb_curso'
```
create table tb_curso( 

codigo_curso integer primary key, 

nome_curso varchar(60) not null 

) 
```
Creating the table 'tb_matricula'
```
create table tb_matricula( 

codigo_curso integer references tb_curso (codigo_curso), 

codigo_aluno integer references tb_aluno (codigo_aluno) 

) 

alter table  

add constraint fk_codigo_curso foreign  key (codigo_curso) references tb_curso(codigo_curso) 

add constraint fk_codigo_aluno foreign  key (codigo_aluno) references tb_aluno(codigo_aluno) 
```

<h2> Inserting the data </h2>
<h4> Note: You have to change the values according to what the document requires. </h4>

Inserting the data of the table 'tb_aluno'
```
insert into tb_aluno (codigo_aluno, nome_aluno, ano_nascimento, email, sexo) 

values (3, 'João Pedro', '1979', 'joao@provasql.com.br', 'M') 
```
Inserting the data of the table 'tb_curso'
```
insert into tb_curso (codigo_curso, nome_curso) 

values (1, ‘MEDICINA’) 
```
Inserting the data of the table 'tb_matricula
```
insert into tb_matricula (codigo_curso, codigo_aluno)  

values (1, 1) 
```

<h1> Pratice Questions </h1>





