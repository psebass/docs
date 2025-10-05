# Dockerfile

## Referencias rápidas

### Dockerfile
¿Qué es un dockerfile?  
Un Dockerfile está compuesto por una secuencia de instrucciones que le dicen a  
Docker cómo construir una imagen de contenedor. Las partes principales de un   
Dockerfile son instrucciones como FROM para la imagen base, RUN para ejecutar   
comandos durante la construcción, COPY y ADD para añadir archivos, WORKDIR   
para definir el directorio de trabajo, ENV para variables de entorno, EXPOSE
para puertos y CMD para el comando por defecto al iniciar.  

### Instrucciones comunes generales
```dockerfile
FROM <imagen>
: Especifica la imagen de base para la compilación de la nueva imagen. 

RUN <comando>
: Ejecuta comandos durante el proceso de construcción de la imagen,
como instalar software o dependencias. 

COPY <ruta-local> <ruta-imagen>
: Copia archivos y directorios desde el sistema host a la imagen del contenedor. 
ADD <fuente> <destino>
: Similar a COPY, pero también puede manejar archivos comprimidos y URLs. 

WORKDIR <ruta>
: Establece el directorio de trabajo (la ruta donde se ejecutarán comandos posteriores)
dentro de la imagen. 

ENV <nombre>=<valor>
: Define variables de entorno que serán utilizadas por la aplicación dentro del contenedor. 

EXPOSE <puerto>
: Informa a Docker que el contenedor escuchará en los puertos especificados. 

CMD ["ejecutable", "param1", "param2"]
: Define el comando por defecto que se ejecutará cuando se inicie un contenedor a partir 
de esta imagen. 

USER <usuario>
: Establece el usuario que ejecutará las instrucciones posteriores. 

ARG <nombre>=<valor>
: Define variables que son accesibles durante el proceso de construcción de la imagen. 

VOLUME <punto-montaje>
: Crea un punto de montaje en el contenedor que puede contener dato
```

### Ciclo resumido
![Ciclo](/public/ciclo_simple.jpg)


## Dockerfile SPA

### Ejemplo

![DockSPA](/public/dockerfile-SPA.jpeg)

## Dockerfile Flask

### Ejemplo

![DockFlask](/public/sec%20conf%20dockerfile%20SPA.jpeg)
