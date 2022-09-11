# MAVEN

Es una herramienta que se usa para construir y manejar proyectos basados en JAVA con la cuale se espera que<br>
los proyectos sean más faciles de comprender y construir.

Esta herrmienta de manejo:

  1. Estandariza la forma en que se construyen proyectos en JAVA.
  2. Define claramente en que consiste el proyecto en desarrollo.
  3. Publica de manera cencilla la inofrmación del proeycto.
  4. Posibilita el comporatir archivos JAR entre proyectos.

## Intslación

1. Ir a la pagina web https://maven.apache.org/download.cgi
2. Descargar el archivo binario ZIP ( Binary zip archive )
3. Descomprimir la carpeta y gurdarla en C:/ ( opcional ) cambiar el nombre a maven ( opcional pero facilita el escribir el path )
4. Ajustar en variables del sistema -> variable name MAVEN_HOME -> value C:\maven -> OK ( para esto se cambio por un nombre facíl )
5. Ajustar en variables del sistema la variable -> path -> editar -> new -> %MAVEN_HOME%\bin -> OK -> reiniciar PC.
6. Comprobar la instalación de maven en la CMD con el comando -> mvn --version ->Enter.
La instalación es exitosa si la CMD arroja el siguiente resultado :
```cmd
Apache Maven 3.8.6 (84538c9988a25aec085021c365c560670ad80f63)
Maven home: C:\maven
Java version: 1.8.0_191, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk1.8.0_191\jre
Default locale: es_ES, platform encoding: Cp1252
OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
```

