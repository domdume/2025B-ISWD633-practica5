# MI APRENDIZAJE
Anteriormente ejecutábamos cada contenedor uno por uno y los conectábamos manualmente. Con Docker Compose, solo debo escribir "instrucciones" en un solo archivo y este se encarga de todo. El archivo .yaml es como el plano de una casa, le digo qué servicios quiero (MySQL, WordPress), qué volúmenes usar ( - mysql-vol), y qué redes ( - net-wp). En lugar de utilizar 4 o 5 comandos ahora se puede utilizar docker compose up-d. Los contenedores pueden llamarse por su nombre de servicio (WordPress pudo encontrar a la base de datos solo llamándola mysql-service), sin necesidad de IPs. Aprendí a usar depends_on y healthcheck. Esto le dice a WordPress: "No intentes arrancar hasta que estés seguro de que la base de datos (mysql-service) está saludable y lista para recibir informaicón". Esto evita muchísimos errores de conexión.

## Problemas solucionados 
Problema: Cuando ejectué docker compose up -d, el comando falló porque el puerto 8080 (que se quería usar para WordPress) ya estaba siendo usado por otro contenedor que se había creado en una práctica anterior (el mysql).

Solución: Se indentificó el contenedor "fantasma" que estaba ocupando el puerto y se lo detuvo (docker stop mi-servidor-web). Como alternativa, también se aprendió que se puede simplemente editar el archivo compose.yaml y cambiar el puerto a uno que estuviera libre, como 8081:80.
