# Prime-Request_Compliance

Se busca consultar la Api de cheack compliance de Prime infrastructure para recuperar la información de aquellos equipos que estan fuera de compliance. 
Lo que necesitamos es contar cuantos son los equipos que se encuentrane en esta situación y enviar dicha información en juntos a los equipos agregando 
su Ip, nombre, etc. Para hacer el envio de la información se opto por agregarla a una archivo csv para su posterior procesamiento.

La solicitud de creación de esta api por parte del cliente era consultar aquellos equipos que se encontraban fuera del compliancias y enviar el numero de equipos
fuera de compliancias junto a su información via email, ademas se solicito enviar un email por cada job audit, por lo cual se hace una iteración del programa 
leyendo y enviando la correspondiente información en emails separados. 

El script cuenta con verificación en caso de error de conexión al servidor y en caso de que los jobs lleguen vacios, en estos casos se envia un email notificando 
el tipo de falla, el cual tambien se realiza de forma independiente por cada job audit.
