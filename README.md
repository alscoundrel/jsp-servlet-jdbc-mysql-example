# jsp-servlet-jdbc-mysql-example
 Java, Servlet and Mysql

The tutorial in
https://www.javaguides.net/2019/03/jsp-servlet-jdbc-mysql-crud-example-tutorial.html

this com.mysql.jdbc.Driver is deprecated (descontinuado) is changed to com.mysql.cj.jdbc.Driver


# Aconselho a criação de um novo projeto:
1º “Dynamic web project” (com web.xml) uso do JDK 12;\n
2º Passarem os ficheiros para as pastas correspondentes (src, WebContent, WebContent->WEB-INF->lib);\n\n

# No mysql criar uma base de dados “demo”, código na pasta sql->demo.sql
CREATE DATABASE demo;\n
USE demo;\n\n
create table users (\n
 id  int(3) NOT NULL AUTO_INCREMENT,\n
 name varchar(120) NOT NULL,\n
 email varchar(220) NOT NULL,\n
 country varchar(120),\n
 PRIMARY KEY (id)\n
);\n
\n
# Adicionar na configuração do Mysql (my.ini), na zona de [mysqld] isto default_time_zone='+00:00'

Ao correr o projeto der erro (pode ser por não associar as dependências):\n
1º Acrescente a dependência “catalina.jar” ao projecto.\n
Clicar com o botão direito do rato no projeto, selecionar properties->Java Build Path->Libraries->Classpath->Add External JARs
Se continuar com erros, adicione estas dependências:\n
•	jsp-api-xxx.jar;\n
•	servlet-api-xxx.jar;\n
•	mysql-connector-java-xxx.jar;\n
•	jstl-xxx.jar;\n
•	protobuf-java-xxx.jar (opcional).\n
\n
