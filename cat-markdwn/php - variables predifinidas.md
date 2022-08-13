# Variables predifinidas

SON LAS VARAIBLES DE CONFIGURACIÓN, EJECUCIÓN Y DE SISTEMAS DEL PROGRAMA.

SE OBTIENEN CON EL COMANDO 

phpinfo();

|Nombre(constante)|	Valor	Descripción|
|:----------------|:-----------------|
|INFO_GENERAL	1	      |La línea de configuración, ubicación de php.ini, fecha de compilación, servidor Web, sistema y más.|
|INFO_CREDITS	2	      |Créditos de PHP. Ver también phpcredits().|
|INFO_CONFIGURATION	4	|Valores Locales y Maestros actuales de las directivas PHP. Ver también ini_get().|
|INFO_MODULES	8       |	Módulos cargados y sus respectivos parámetros Ver también get_loaded_extensions().|
|INFO_ENVIRONMENT	16	|Información de las variables de entorno. Tambien disponibles en $_ENV.|
|INFO_VARIABLES	32	  |Muestra todas las variables predefinidas de EGPCS (Environment, GET, POST, Cookie, Server).|
|INFO_LICENSE	64	    |Información de Licencia de PHP. Ver también el » FAQ de licencia.|
|INFO_ALL	-1	        |Muestra toda la información anterior|

ejemplo:

phpinfo(32) <== VAraibles de información.

|Variable|Value|
|:--|:--|
|$_SEVER["PATH"]| C:..sistem|
|$_SERVER['SYSTEMROOT'] |	C:/Windows|
|$_SERVER['COMSPEC'] |	C:\WINDOWS\system32\cmd.exe|
|$_SERVER['PATHEXT'] |	.COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC|
|$_SERVER['WINDIR'] |	C:\WINDOWS|
|$_SERVER['SYSTEMDRIVE'] |	C:|
|$_SERVER['TEMP'] |	C:/Windows/Temp|
|$_SERVER['TMP'] |	C:/Windows/Temp|
|$_SERVER['PHPRC'] |	C:/laragon/bin/php/php-8.0.21-nts-Win32-vs16-x64|
|$_SERVER['PHP_FCGI_MAX_REQUESTS'] |	0|
|$_SERVER['_FCGI_SHUTDOWN_EVENT_'] |	1204|
|$_SERVER['SCRIPT_NAME'] |	/index.php|
|$_SERVER['REQUEST_URI'] |	/|
|$_SERVER['QUERY_STRING'] |	no value|
|$_SERVER['REQUEST_METHOD'] |	GET|
|$_SERVER['SERVER_PROTOCOL'] |	HTTP/1.1|
|$_SERVER['GATEWAY_INTERFACE'] |	CGI/1.1|
|$_SERVER['REMOTE_PORT'] |	60045|
|$_SERVER['SCRIPT_FILENAME'] |	C:/laragon/www/dgmikel.github.io/index.php|
|$_SERVER['SERVER_ADMIN'] |	admin@example.com|
|$_SERVER['CONTEXT_DOCUMENT_ROOT'] |	C:/laragon/www/dgmikel.github.io|
|$_SERVER['CONTEXT_PREFIX'] |	no value|
|$_SERVER['REQUEST_SCHEME'] |	http|
|$_SERVER['DOCUMENT_ROOT'] |	C:/laragon/www/dgmikel.github.io|
|$_SERVER['REMOTE_ADDR'] |	127.0.0.1|
|$_SERVER['SERVER_PORT'] |	666|
|$_SERVER['SERVER_ADDR'] |	127.0.0.1|
|$_SERVER['SERVER_NAME'] |	dgmikel.github.io.test|
|$_SERVER['SERVER_SOFTWARE'] |	Apache/2.4.47 (Win64) OpenSSL/1.1.1k mod_fcgid/2.3.10-dev|
|$_SERVER['SERVER_SIGNATURE'] |	no value|
|$_SERVER['SystemRoot'] |	C:\WINDOWS|
|$_SERVER['HTTP_ACCEPT_ENCODING'] |	gzip, deflate|
|$_SERVER['HTTP_SEC_GPC'] |	1|
|$_SERVER['HTTP_ACCEPT'] |	text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8|
|$_SERVER['HTTP_ACCEPT_LANGUAGE'] |	es-ES;q=0.7|
|$_SERVER['HTTP_USER_AGENT'] |	Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.5112.81 Safari/537.36|
|$_SERVER['HTTP_UPGRADE_INSECURE_REQUESTS'] |	1|
|$_SERVER['HTTP_CACHE_CONTROL'] |	max-age=0|
|$_SERVER['HTTP_CONNECTION'] |	close|
|$_SERVER['HTTP_HOST'] |	dgmikel.github.io.test:666|
|$_SERVER['FCGI_ROLE'] |	RESPONDER|
|$_SERVER['PHP_SELF'] |	/index.php|
|$_SERVER['REQUEST_TIME_FLOAT'] |	1660409516.9254|
|$_SERVER['REQUEST_TIME'] |	1660409516|
