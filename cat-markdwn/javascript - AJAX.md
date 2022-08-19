# AJAX - JAVASCRIPT

AJAX significa Asyncronous JavaScript XML

se utilliza para hacer paginas dinámicas.
es asíncrono y se utiliza para refrescar datos en ciertas partes de la pagína sin tener que refrescar todo el Documento HTML


```javascript

function javascript_ajax(){

var xmlhttp = new XMLHttpRequest();

xmlhttp.onreadystatechange = function(){
  
  if(xmlhttp.readyState == 4 && xmlhttp.status == 200){
      
      /*acciones aincronas a ejecutar*/
      
      var respuesta = xmlhttp.responseText;
      console.log(respuesta);
    
  }

}// end onready..

xmlhttp.open("GET", "https://api.coindesk.com/v1/bpi/currentprice.json",true);
xmlhttp.send();

}


```
