Primero debemos descargar git para luego instalarlo en nuestra pc.
recordar tildas la opcion de :"git bash here" y seleccionar la opcion de use cisual stufio as a git degault editor.
Podemos abrir el git bash o una consola o una terminal desde vs.
para abrir la termina desde vsc tenemos que abrir el root en el IDE, luego tocamos sobre el boton "terminal" y luego tocamos sobre el select que esta al lado del "+" y seleccionamos la opcion "git bash". Al tocarlo, se nos abre el bash en la terminal.
Paso seguido necesitamos configurar nuestro usuario por unica vez con los siguientes comandos:
got config --global user.name "nombreUsuario"
git config --global user.mail emailsuyo@gmail.com
Luego de esto podemos corroborar si la configuracion quedo impactada con los siguientes comandos:
git config user.name
git config user.email
------------------------------
Luego de tener todo configurado e instalado necesito pararme sobre mi root y decirle: "che root, vamos a trabajar con git" (Como hago esto?)
Para hacer esto necesitamos estar posicionado sobre mi root y usar el comando (por primera y unica vez):
git init
Luego de ejecutar el git init ya estamos parados sobre el estado"working directory" que es donde generamos todas las lineas de codigo
Cuando completo mi tarea, paso todo lo trabajado del "working directory" -> "staging area" Como hago esto? Para hacerlo necesitamos el comando: 
git add . (comando por lote)
git add nombreArchivo (manual archivo o directorio)
Luego de pasar todo el "STAGING AREA" instantaneamente pasamos todo el "repository" con el comando:
git commit -m "comentario breve y descriptivo de lo que se estuvo trabajando"
Al terminar de commitear, se nos genera una version nueva y nos posiciona en el "working directory" automaticamente.

Como controlo los estados de mis archivos/directorios? con el siguiente comando:
git status
git log --oneline: para ver los commit
git log : para ver directamente a que hora lo hizo y quien lo hizo
Con git checkout podemos ir a la rama que queramos
Con git merge podemos unir lo que estaba en una rama, y seguir parado sobre el master
Las ramas nos sirven para generar una copie fiel de nuestro proyecto. Esto nos permite modificar las git banch NombreRama
Para corroborar las ramas que tenemos creadas usamos el comando:
git branch -l
para movernos entre las ramas usamos el comando:
git checkout nombreRama
Es importante que cuando nos movemos a una rama y trabajamos sobre la misma, hagamos el pasaje de estado que ya conocemos (working directory -> staging area -> repo)
A partir de entender que el codigo generado  en nuestra rama es el correcto voy a necesitar agregar esta rama a ;mi master, como hacemos el agregado de nuestra rama al master? Antes de ejecutar el comando es necesario estar posicionado sobre el master, para ahi eejcutar el siguiente comando: 
git merge NombreRama
Luego de mergear, podemos eliminar la rama con el siguiente comando:
git branch -d nombreRama
sss
ya en la pantalla de crear repositroio tengo que completarlo con un nombre unico e irrepetible, dejar tildad la opcion public ty dejar todo como esta
apartir de ahora puedo usar el comando que crea el tubo entre las dos partes
git remote add origin https://
este paso se ejecuta una sola vez y luego tengo que usar el comando :
git push -u origin master
para pasar toda la oinfo de mi llocal por el tubo a git hub