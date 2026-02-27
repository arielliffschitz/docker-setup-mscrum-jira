Instrucciones 
Uso con imágenes Docker Hub
Requerido: Docker Desktop y Postman.
1-Descargar desde GitHub el repositorio https://github.com/arielliffschitz/docker-setup-mscrum-jira y colocar en la misma carpeta docker-compose.yml y mysql-data.7z; 
descomprimir mysql-data para que la carpeta quede junto al compose. Se puede bajar también el Collection para postman.
2-Editar docker-compose.yml(no olvidar!) : reemplazar la línea IP_ADDR=http://<your-local-ip>:8085 por la IP local propia, por ejemplo IP_ADDR=http://192.168.1.225:8085.
3-Ejecutar: En la carpeta que contiene docker-compose.yml, abrir terminal y ejecutar  docker compose create
4-Arrancar:
  a-Iniciar contenedores: primero mysql y eureka-server.
  b-Verificar Eureka en http://localhost:8761
  c-Iniciar todos los microservicios excepto gateway; confirmar registro en Eureka.
  d-Iniciar gateway y esperar a que se registre.

5-Prueba inicial ( sin autenticación): GET http://localhost:8090/mscrumjira/task.
Esperado: lista de task
6-Autenticación y flujo: https://docs.google.com/document/d/1KDAECAmoGt9KdEl6zFSWx-yUWjdf-Ur7fQB6gbo_TQU/edit?tab=t.0
