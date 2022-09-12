# CONFIGUARACIÓN MySQL

Es para correr en local, puerto 3306, user root sin pasword y conlas configuración de TimeZone


```javascript
#GENERAL
server.port=8080

spring.datasource.url=jdbc:mysql://localhost:3306/spring?useUnicode=true&useJDBCCompliantTimezoneShift=true&useLegacyDatetimeCode=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=
spring.datasource.driver-class-name=com.mysql.jdbc.Driver
spring.jpa.database-platform = org.hibernate.dialect.MySQL5Dialect
spring.jpa.generate-ddl=true
spring.jpa.hibernate.ddl-auto = update
```
