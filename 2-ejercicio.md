# Ejercicio
Configurar SonarQube utilizando Docker Compose, para esto necesitas dos servicios:
- Servicio: SonarQube
- Desde el host es necesario acceder a SonarQube por lo que necesitas mapear el puerto correspondiente.
- Servicio: PostgreSQL (existen otras opciones: Microsoft SQL Server, Oracle)
- Coloca un healtcheck para cada uno de los servicios.
- Los dos servicios deben pertenecer a una red de tipo bridge
- Investiga cuáles son los volúmenes necesarios para cada servicio
- Investiga cuáles son las variables de entorno para que los servicios funcionen de manera adecuada.
  
# Una vez creado tu archivo .yaml realiza la respectiva prueba 

Por defecto, el comando docker compose up -d busca automáticamente un archivo llamado compose.yaml o docker-compose.yaml. Como el archivo tiene un nombre diferente, se debe indicar a Docker qué archivo usar con la bandera -f (que significa "file" o archivo).

```
docker compose -f composeD.yaml up -d
```

# COMPLETAR CON UNA CAPTURA DE PANTALLA LUEGO DE EJECUTAR EL ARCHIVO

<img width="1722" height="845" alt="image" src="https://github.com/user-attachments/assets/fab20a48-ed9e-4040-9f07-7fe199e174e9" />


# ACCEDER A LOCALHOST:9000 para ingresar a SonarQube

<img width="1906" height="1021" alt="image" src="https://github.com/user-attachments/assets/f10dd9fd-cfe5-45b7-ac55-a63e88929d73" />

