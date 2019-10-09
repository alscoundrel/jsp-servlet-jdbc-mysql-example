# jsp-servlet-jdbc-mysql-example
 Java, Servlet and Mysql

The tutorial in
https://www.javaguides.net/2019/03/jsp-servlet-jdbc-mysql-crud-example-tutorial.html

this com.mysql.jdbc.Driver is deprecated (descontinuado) is changed to com.mysql.cj.jdbc.Driver


# Aconselho a criação de um novo projeto:
1º “Dynamic web project” (com web.xml) uso do JDK 12;<br>
2º Passarem os ficheiros para as pastas correspondentes (src, WebContent, WebContent->WEB-INF->lib);

# No mysql criar uma base de dados “demo”, código na pasta sql->demo.sql
CREATE DATABASE demo;<br>
USE demo;<br>
<br>
create table users (<br>
 id  int(3) NOT NULL AUTO_INCREMENT,<br>
 name varchar(120) NOT NULL,<br>
 email varchar(220) NOT NULL,<br>
 country varchar(120),<br>
 PRIMARY KEY (id)<br>
);<br>

# Adicionar na configuração do Mysql (my.ini), na zona de [mysqld] isto default_time_zone='+00:00'
<br>
Ao correr o projeto der erro (pode ser por não associar as dependências):<br>
1º Acrescente a dependência “catalina.jar” ao projecto.<br>
Clicar com o botão direito do rato no projeto, selecionar properties->Java Build Path->Libraries->Classpath->Add External JARs<br>
Se continuar com erros, adicione estas dependências:<br>
•	jsp-api-xxx.jar;<br>
•	servlet-api-xxx.jar;<br>
•	mysql-connector-java-xxx.jar;<br>
•	jstl-xxx.jar;<br>
•	protobuf-java-xxx.jar (opcional).<br>
