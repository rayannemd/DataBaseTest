<h1> DataBaseTest </h1>

This is a repository for my database test. If you want to interact with it, open the PostgreSQL on your computer and run the following codes.

<h2> Creating the database </h2>

```
create database bdescola 
```

<h2> Creating the tables </h2>

```
create table tb_aluno( 

codigo_aluno integer primary key, 

nome_aluno varchar(60) not null, 

ano_nascimento int, 

email varchar(60), 

sexo varchar not null 

)  
```

```
create table tb_curso( 

codigo_curso integer primary key, 

nome_curso varchar(60) not null 

) 
```

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

```
insert into tb_aluno (codigo_aluno, nome_aluno, ano_nascimento, email, sexo) 

values (3, 'João Pedro', '1979', 'joao@provasql.com.br', 'M') 
```

```
insert into tb_curso (codigo_curso, nome_curso) 

values (1, ‘MEDICINA’) 
```

```
insert into tb_matricula (codigo_curso, codigo_aluno)  

values (1, 1) 
```

<h4> Note: You have to change the values according to what document requires. </h4>


