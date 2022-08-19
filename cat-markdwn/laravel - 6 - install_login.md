# INSTALACIÓN 
## CON LOG IN Y REGISTRO


## INSTALCIÓN - VÍA CONMPOSER 

```javascript

/* Comando para instalar laravel*/
composer create-project --prefer-dist laravel/laravel name_app "6.*"


/* Entrar a la carpeta del proyecto*/
/* Comando para instalar los modulos de login y register*/
composer  require laravel/ui

/* Agregar a configuarción básica*/
php artisan ui bootstrap
php artisan ui vue
php artisan ui react

/* Para agrgar las vista de login y register */
php arisan ui bootstrap --auth 
php arisan ui vue --auth 
php arisan ui react --auth 

/* Instalamos los paquetes NPM*/
npm install


/* Se arranca el compilador Webpack (webpack.mix.js) */
npm run dev

```
