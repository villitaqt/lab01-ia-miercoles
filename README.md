# lab01-ia-miercoles
 
## TAREA:
- Desplegar dos web, WEB 1 y WEB 2
- los puertos configurados de manera externa deben ser 4000 y 4001
- Gestionar carpetas
- Hacer uso de Gitflow/Conventional commits 

## GUIA DE DESPLIEGUE

Requisitos:
- Docker Engine instalado.
- Git instalado.


### Construcción de Imágenes
```
docker build -t image-web01 src/web01
docker build -t image-web02 src/web02 
```

### Despliegue de Contenedores
**Web01 (Puerto 4000):**

``` 
docker run --name cont-web-01 -p 4000:80 image-web01
```
**Web02 (Puerto 4001):**

```
docker run --name cont-web-02 -p 4001:80 image-web02
```

### Detener e iniciar
```
docker stop cont-web-01 cont-web-02  # Detener
docker start cont-web-01 cont-web-02 # Iniciar
```