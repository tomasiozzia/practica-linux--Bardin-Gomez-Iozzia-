Errores encontrados - Gomez(Alumno C)

1- El docker compose no estaba instalado
- Error al ejecutar 'docker-compose up -d': El sistema mostraba 'Command 
'docker-compose' not found'
-Ese error de que no funcionaba, lo solucione instalando Docker y
Docker Compose con el comando : sudo apt install docker.io docker-compose

Pruebas con docker-compose
-Luego de haber solucionado el error anterior, volvi a correr:
 - 'docker-compose up -d' Funciono
 -'docker-compose config' Funciono
 -'docker-compose logs' Funciono
 -Con estos comandos pude levantar los 6 contenedores.

Prometheus y los targets.
-En'docker ps' se ve que el contenedor Prometheus se reinicia seguido.
- Esto coincide con lo que decia el enunciado sobre los targets: hay
una configuracion que hace que algunos aparezcan DOWN.

Entrando a Grafana desde la VM
-Ejecute lo que decia el enunciado ' http://localhost:3000' para acceder a grafana.
-Aparecio un mensaje que decia 'command 'firefox' not found'. Basicamente no lo tengo instalado.
-Claramente no pude entrar porque no tengo una virtualizacion visual.

Entrando a Grafana desde Windows.
-Entre a grafana desde mi windows, utilice la ip que aparece al utilizar el comando: hostname -l
-Utiliza la red local.
-Entre a grafana desde windows, configure Prometheus pero al ingresar la URL del enunciado,
me salto un error.
-AL tener este error, revise los logs de prometheus con el comando: 'docker-compose logs prometheus |
tail -20' me saltaba un error que decia 'yaml:line 12:could not find expected ":"'.
-Esto significa que en el archivo 'prometheus.yml' tiene un error de sintaxis en la linea 12.

Arreglando error de prometheus.yml
-Arregle el error de prometehus que era un error de sintaxis.
-Error Sintaxis: La linea que era comentario se dividia en dos, entonces la que quedaba como segunda no quedaba comentada.
-Al arreglar el error de sintaxis, pude entrar a los targets de prometheus, por ende pude hacer funcionar el URL del enunciado para entrar a targets.

