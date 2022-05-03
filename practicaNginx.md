![20220430_13h06m49s_grim](https://user-images.githubusercontent.com/91564852/166104724-9c1445c6-9ec7-49b1-95d5-aefe827d00d7.png)

Haremos esta práctica de dos maneras. Primero serviremos dos webs distintas vía Nginx usando puertos distintos en localhost, y después las serviremos empleando nombres de dominio.

- Instalando nginx en Ubuntu 22.04.

```
sudo apt install nginx
```

- Configurando el local host: vamos hacia la carpeta de archivos de configuración donde aparecerán los sitios disponibles para nuestro servidor:

![20220430_13h12m34s_grim](https://user-images.githubusercontent.com/91564852/166104759-7e6c7adf-c656-4738-95c2-d4812836db1d.png)

- Creamos sendos archivos de configuración, apuntando hacia los puertos 81 y 82:

```bash
sudo vim ejemplo1
```

![20220430_13h25m35s_grim](https://user-images.githubusercontent.com/91564852/166104766-7345461f-172a-4d50-8712-a13f5ba1839a.png)


```bash
sudo vim ejemplo2
```

![20220430_13h27m03s_grim](https://user-images.githubusercontent.com/91564852/166104777-01c16b37-8aa5-4b86-b1e5-3603bb5ff0dd.png)

- Creamos los enlaces simbólicos en la carpeta `sites-available` que apuntan a los archivos de configuración recién creados:

![20220430_13h32m40s_grim](https://user-images.githubusercontent.com/91564852/166104790-c8f2582b-e68f-4337-8e62-a1d6b61b11bf.png)

- A continuación vamos a crear los directorios a los que apunta el root de nuestros archivos de configuración:

![20220430_13h36m05s_grim](https://user-images.githubusercontent.com/91564852/166104798-f0059c29-3173-4dde-8cdd-60bf772343a2.png)

- Una vez hemos descargado los archivos web de prueba, vamos a renombrarlos y moverlos a la carpeta correcta:

![20220430_13h50m01s_grim](https://user-images.githubusercontent.com/91564852/166104806-7e4fbca5-9e1f-4312-b7c0-34b7dfbcf583.png)

- Reiniciamos el servidor:

![20220430_13h50m56s_grim](https://user-images.githubusercontent.com/91564852/166104809-08af884d-2a5f-46b7-8f4f-4ab6199ef74b.png)

- Comprobamos que nuestro sitio está disponible vía el puerto 81 del localhost:

![20220430_13h56m17s_grim](https://user-images.githubusercontent.com/91564852/166104837-ee53eb41-4a09-46ef-af08-8136956a5d60.png)

- Y lo mismo para el puerto 82:

![20220430_13h57m39s_grim](https://user-images.githubusercontent.com/91564852/166104845-2c191d4f-3d6a-4143-9d0a-10f1ec5fe346.png)

Con todo lo cual, ya tenemos ambas páginas web de ejemplo funcionando a través de nuestro servidor nginx en localhost.

- En la siguiente captura podemos ver la configuración necesaria para servir las páginas web a través de subdominios distintos que comparten puerto:

![20220503_19h14m19s_grim](https://user-images.githubusercontent.com/91564852/166505223-ce53cf63-8cd1-4f1f-9e8a-db1e7521b2df.png)

Nótese que para este procedimiento hemos debido de modificar el archivo `/etc/hosts`.


- Accedemos a las páginas de ejemplo escribiendo la ruta que hemos indicado:

![20220503_19h14m36s_grim](https://user-images.githubusercontent.com/91564852/166505380-131e0aca-af71-421d-9be3-0f310689c4ef.png)
![20220503_19h15m24s_grim](https://user-images.githubusercontent.com/91564852/166505411-017187f6-6231-4214-91d1-b7461fa11e41.png)


