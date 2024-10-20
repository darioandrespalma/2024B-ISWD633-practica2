# Redes
Las redes son un componente fundamental que permite la comunicación entre contenedores, así como la comunicación de los contenedores con el mundo exterior. 
![Imagen](img/redes.PNG)
- Bridge: Esta es la red por defecto en Docker. Permite la comunicación entre contenedores en el mismo host. Cada contenedor conectado a la red bridge tiene una IP propia en la subred de la red bridge.
    -  Brige por default: Cuando se ejecuta un contenedor, Docker crea automáticamente una red de tipo bridge por default. Esta red se utiliza para permitir la comunicación entre contenedores en el mismo host. Cada contenedor conectado a esta red obtiene su propia dirección IP en la subred de la red bridge.
    - Bridge creada por nosotros: Un usuario también puede crear sus propias redes de tipo bridge en Docker. Esto puede ser útil para organizar y segmentar los contenedores de una aplicación de manera más controlada. Al crear una red bridge personalizada, se puede especificar un rango de direcciones IP y otras configuraciones de red específicas. Los contenedores conectados a esta red utilizarán las direcciones IP de la subred definida por el usuario.
- Host: Con esta red, los contenedores comparten la red del host en lugar de tener su propia interfaz de red. Esto puede mejorar el rendimiento de red, pero los contenedores pueden entrar en conflicto con los puertos del host si intentan utilizar los mismos puertos.
- None: Con esta red, se deshabilita la configuración de red. Los contenedores que usan esta red tienen su propia red de bucle invertido y no pueden comunicarse con otros contenedores a menos que se conecten explícitamente a una red.

### Crear una red de tipo bridge

Primero, vamos a crear las redes personalizadas que se indican en el esquema. Para cada red, podemos usar el siguiente comando.

```
docker network create red1 -d bridge
```

![Imagen](img/PrimeroRed.png)

```
docker network create red2 -d bridge
```

![Imagen](img/SegundaRed.png)

```
docker network create red3 -d bridge
```

![Imagen](img/TerceraRed.png)

### Crear un contenedor vinculado a una red

```
docker run -d --name <nombre contenedor> --network <nombre red> <nombre imagen>
```

Aplicamos este comando para crear los contenedores vinculados a las redes.

Crear el primer contenedor y vincularlo a la red red1:

```
docker run -d --name contenedor1 --network red1 nginx:alpine
```

![Imagen](img/CrearContenedorRed1.png)

Crear el segundo contenedor y vincularlo a la red red2:

```
docker run -d --name contenedor2 --network red1 nginx:alpine
```

![Imagen](img/CrearContenedorRed2.png)

Crear el tercer contenedor y vincularlo a la red red3:

```
docker run -d --name contenedor3 --network red1 nginx:alpine
```

![Imagen](img/CrearContenedorRed3.png)

### Para saber a qué red está conectado un contenedor

```
docker inspect <nombre contenedor>
```
ó
```
docker network inspect <nombre red> 
```

  
* Inspeccionar la red: Para verificar qué contenedores están conectados a una red, usa:

```
docker network inspect <nombre red>
```

![Imagen](img/InspeccionRed1.png)
  
* Inspeccionar un contenedor: Para ver la red a la que está conectado un contenedor:

```
docker inspect <nombre-contenedor>
```

![Imagen](img/InspeccionRed2.png)

![Imagen](img/InspeccionRed3.png)


### Vincular contenedor a una red
```
docker network connect <nombre red> <nombre contenedor>
```

### Para desvincular un contenedor de una red
```
docker network disconnect <nombre red> <nombre contenedor>
```

### Para listar las redes existentes
```
docker network ls
```

![Imagen](img/InspeccionRed.png)

### Crear los contenedores y las redes que se presentan en el esquema. Usar para todos los contenedores la imagen de nginx:alpine

![Imagen](img/esquema-ejercicio-redes.PNG)

# COLOCAR UNA CAPTURA DE LAS REDES EXISTENTES CREADAS

![Imagen](img/ListaContenedoresActivos.png)


### Para eliminar las redes creadas
```
docker network rm <nombre de la red>
```


* Eliminar la red red1:

```
docker network rm red1
```

![Imagen](img/FinalEliminacionRed1.png)

  
* Eliminar la red red2:

```
docker network rm red2
```

![Imagen](img/EliminarRed2.png)

* Eliminar la red red3:

```
docker network rm red3
```

![Imagen](img/EliminarRed2.png)

