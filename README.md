# EJERCICIO 2: Usando Closures

Modificar el siguiente script usando closures para que se ejecute sin problemas:

```
var feature = 'closures'; 
(function () {     
	if ( typeof feature === 'undefined' ){         
		var feature = 'callbacks';         
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();
```


-En la imágen 1 se observa que hay una variable local declarada dentro de la función la cual tienen el mismo nombre que la variable global.
Cuando el interprete de javaScript revisa línea por línea, llega a un momento en donde lee la condición, la cual busca una variable, y como se sabe, si la variable local lleva el mismo nombre que la variable global, la función tomará la variable local, es decir la variable local tiene más peso que la global. Pero la variable local aún no está inicializada y el interprete la declara como "Undefined" cumpliedo la condición que siendo "True" imprimirá el mensaje 'JS coders love its callbacks'.

![codigo sin editar](http://i65.tinypic.com/b6aw60.jpg)

-En la imagén 2 se observa que al eliminar la palabra reservada var en la cuarta línea ahora no hay una variable local declarada en el contexto de la función y por tanto tomará la variable global y como ya tiene un valor de tipo "string" al pasar por la condición la igualdad es "false", por ello imprime la respuesta correcta.

![codigo editdo](http://i64.tinypic.com/2vb0vph.jpg)
