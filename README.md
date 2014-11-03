docker-minecraft
================

Servidor _Minecraft_ con Servidor Web que muestra el mapa con Overviewer.py.

setup
-----
Crea el fichero *start* a partir de *start.0* rellenando con el directorio presente (pwd).

buildall 
--------
Construye las imagenes de minecraft (servidor) y mapgenerator (overviewer.py), ambas basadas en phusion/baseimage.

stopcontainers
--------------
Detiene todos los contenedores.

rmcontainers
------------
Elimina todos los contenedores docker.

start
-----
Inicia servidor minecraft, y servidor nginx (basado en dockerfile-nginx) y genera el mapa de minecraft.

generamap
---------
Genera el mapa de nuevo.

stopcontainers
--------------

Detiene todos los contenedores docker.

*****

**Noviembre/2014**

