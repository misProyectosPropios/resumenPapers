De lookup lo único que tengo es que había

+ El Dispatch Table Search (**DTC**)
+ Global Lookup Cache (**GLC**) (mejoras de DTC)
+ Inline cache (**lc**)
+ **Polymorphic inline cache**
	
Estaticamente tipada:
+ **VTBL**
	
**VTBL**: cada clase guarda a donde llamar.

+ Problema: al agregar un mensaje, cambian todas las direcciones de a donde llama cada una, por lo que hay que compilarlo todo de nuevo (lento)

+ **Dispatch table search**
```
Busco si la clase en donde estoy sabe responder al mensaje y si es así, listo
Sino, voy al padre.
Si llegué a la clase final, entonces voy a buscar "Message Not Understood"
```

	
+ Para el **global Lookup cache**
	+ Tenemos una cache de 512 elementos.
	+ Se verifica si el mensaje fue conseguido o sino, hacemos DTC 
	
Verificar
Para el Inline cache, en cada lugar donde se envía mensaje tenemos una cache que guarda hasta a donde se llamó.

PLC: 
	Guardamos mas de un elemento, en este caso 6