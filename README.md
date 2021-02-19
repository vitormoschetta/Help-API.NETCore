# Help-API.NETCore

### Recebimento de parâmetros nos _requests_


#### [FromBody] 
Lida com parâmetros que vem no corpo da requisição.

POST, PUT, DELETE 

Geralmente definidos um objeto que recebe o valor de cada propriedade mapeada nele que seja comum à propriedade do corpo da requisição.


<br>

#### [FromRoute] 
Lida com parâmetros de rota, que vêm antes de "?"

<br>

####FromQuery] 
Lida com parâmetros de consulta, que vêm depois de "?"

Ex: "orders/123?ShowHistory=true"então 
	
   "123" é seu parâmetro de rota.  
   "showHistory" é seu parâmetro de consulta.
	
 
> Obs: com [FromQuery] é possível definir um objeto e preenchê-lo a partir dos parâmetros contidos na url do request.

<br>

#### [FromHeader] 
Lida com os parâmetros contidos no "head" da requisição.

Tanto podemos definir um objeto para receber os parâmetros mapeados no header que sejam equivalentes, quanto podemos receber um único parâmetro
do head, neste caso da seguinte forma:

  	[FromHeader(Name = "ApiToken")] string apiToken
	
	  Aqui mapeamos para a string "apiToken" o valor do parametro 		  "ApiToken" contido no "header" da requisição.
