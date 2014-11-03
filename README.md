docker-minecraft
================

Servidor Minecraft con Servidor Web que muestra el mapa con Overviewer.py

setup

=> creamos el fichero start a partir de start.0 rellenando con el directorio presente


buildall 

=> construye las imagenes de minecraft (servidor) y mapgenerator (overviewer.py)
   Ambas basadas en phusion/baseimage


rmcontainers

=> elimina todos los contenedores docker


start

=> inicia servidor minecraft, y servidor nginx (basado en dockerfile-nginx)
   y genera el mapa de minecraft


generamap

=> genera el mapa de nuevo


