# jsp-servlet-jdbc-mysql-example
 Java, Servlet and Mysql

The tutorial in
https://www.javaguides.net/2019/03/jsp-servlet-jdbc-mysql-crud-example-tutorial.html

this com.mysql.jdbc.Driver is deprecated (descontinuado) is changed to com.mysql.cj.jdbc.Driver


# Aconselho a criação de um novo projeto:
1º “Dynamic web project” (com web.xml) uso do JDK 12;
2º Passarem os ficheiros para as pastas correspondentes (src, WebContent, WebContent->WEB-INF->lib);

# No mysql criar uma base de dados “demo”, código na pasta sql->demo.sql
CREATE DATABASE demo;
USE demo;

create table users (
 id  int(3) NOT NULL AUTO_INCREMENT,
 name varchar(120) NOT NULL,
 email varchar(220) NOT NULL,
 country varchar(120),
 PRIMARY KEY (id)
);

# Adicionar na configuração do Mysql (my.ini), na zona de [mysqld] isto default_time_zone='+00:00'

Ao correr o projeto der erro (pode ser por não associar as dependências):
1º Acrescente a dependência “catalina.jar” ao projecto.
Clicar com o botão direito do rato no projeto, selecionar properties->Java Build Path->Libraries->Classpath->Add External JARs
Se continuar com erros, adicione estas dependências:
•	jsp-api-xxx.jar;
•	servlet-api-xxx.jar;
•	mysql-connector-java-xxx.jar;
•	jstl-xxx.jar;
•	protobuf-java-xxx.jar (opcional).
