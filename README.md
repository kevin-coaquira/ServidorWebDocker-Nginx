# ServidorWebDocker-Nginx

Ejecutamos el siguiente comando <code>docker run --rm -d -p 8080:80 --name web nginx</code> en PowerShell  
![paso1](https://user-images.githubusercontent.com/91737963/168915418-cf11545c-d0bc-4cc9-a0ea-1812548ca147.png)  
Abrimos localhost:8080 y se ve que todo funciona correctamente, ya que se ve que nginx muestra por defecto su página  
![paso2](https://user-images.githubusercontent.com/91737963/168915552-3c6cd97a-94e2-40bb-90d3-b4c3460e3ce4.png)  
Acontinuación detenemos el contenedor con el cmd <code>docker stop web</code> en este caso yo le llame <code>docker-nginx</code>  
![paso3](https://user-images.githubusercontent.com/91737963/168916091-a4dd9220-01ed-4b1e-ab23-fb47888d184b.png)  
creamos nuestro propio html  
![image](https://user-images.githubusercontent.com/91737963/168915938-8bdb566d-123a-40c0-981e-ed4835bcd934.png)  
Una vez creado el html ejecutamos el siguiente cmd <code>docker run --rm -d -p 8080:80 --name web -v ~/Documentos/nginx/site-content:/usr/share/nginx/html nginx</code>, que este debe estar creado un directorio llamado **Nginx** y dentro de este otro directorio llamado **site-content** que dentro estara el html, en mi caso el siguiente::  
![image](https://user-images.githubusercontent.com/91737963/168916670-793a72b1-70b8-4eba-a855-8876575dbeb0.png)  
Una vez que se haya ejecutado vamos al localhost:8080 y vemos que todo salio bien  
![paso4](https://user-images.githubusercontent.com/91737963/168916185-e3b698b7-26cd-43b3-849f-e7152f2ce66e.png)
