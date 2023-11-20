# to-do-list-docker
Este proyecto construye las imágenes de Docker especificadas en el archivo docker-compose.yml. El cual realiza este proceso basándose en las instrucciones 
proporcionadas en los respectivos Dockerfile de cada servicio.

También se puede iniciar los servicios, pero da un error cuando se arranca el proyecto en el port 3000: 
"backend_1 | Error: ENOENT: no such file or directory, stat '/frontend/build/index.html'" 

He intentado varias opciones para solucionar este error y terminar de dockerizar el proyecto, pero no he podido solucionarlo todavía.
