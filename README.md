# ¡Hola! 👋 Bienvenido a este tutorial de como usar Git

En este encargo debes utilizar `git` y su `cli` para administrar este repositorio. Pero no te preocupes, ¡te acompañaré en el proceso!

|Tiempo Promedio de Ejecución| 15 minutos |
|--|:--|
|Dificultad|Baja|
|Resultados esperados|Aprender a realizar `commits` y control de `branch`|

## Comenzemos:

### Primero que todo, necesitas generar una copia de este repositorio en tu computador

Así que sígueme el paso:

1. Descarga e instala `git` y su `cli` en tu computador desde este [link de la página oficial de git](https://git-scm.com/download/)
	- Debes buscar el que se acomode más a tu sistema operativo (Window, Linux o Mac).
	- De manera automática debieses tener en tu computador `git`. Puedes comprobar si se instaló correctamente ejecutando el comando `git --version` en cualquier momento en tu `CMD` o `Línea de comandos`
2. Copia el link desde el botón de que entrega el botón de `Code` que está la raíz del repositorio (Donde estás viendo este archivo).
	- Ejemplo: 
	![imagen](https://drive.google.com/uc?id=1z5ca9eQ2LyatxudvVYRt8HDmFvou11MW)
3. Abre tu *Línea de comandos* favorita y **clona** el repositorio en tu máquina con el comando `git clone {y aquí tu url}` (reemplazando donde está indicado con la url de tu repositorio).
4. Se te creará una carpeta con el nombre de tu repositorio en donde hayas ejecutado tu línea de comandos.

Si seguiste correctamente los pasos, ¡Felicitaciones! 🎉 Tienes tu primer repositorio clonado.

### ¡Ya clonamos!... y ahora ¿qué hacemos?

Ahora podemos entrar a esta carpeta con el comando `cd {micarpeta}` (quitando las llaves), la cual posee la configuración de tu `git` completa y podemos comenzar a ejecutar, modificar y añadir o eliminar cosas a nuestra carpeta, git se hará cargo de versionar y contorlar los cambios realizados.

1. Crea un nuevo archivo de texto en la carpeta
	- **En windows:** Botón secundario en una parte vacía de la carpeta y luego `Nuevo` > `Documento de Texto`, nombre el archivo `PruebaGit`.
	- **En Linux y Mac:** Abre la `terminal`, navega a tu carpeta de `git` y ejecuta el comando `touch PruebaGit.txt`, ésto generará un documento vacío dentro de la carpeta.
2. Realizemos nuestro primer `commit` en la carpeta correspondiente (donde descargamos nuestro repositorio y agregamos nuestro archivo), ejecutando los siguientes comandos:
	- `git add .` para agregar cualquier cambio en nuestro repositorio a "preparación".
	- `git commit -m ""` para registrar cualquier cambio que esté preparado con el mensaje que esté dentro de las comillas. En este caso, usa el mensaje `Creado archivo PruebaGit.txt`.
3. Si seguiste los pasos correctamente, tendremos nuestro `git` con su primer cambio registrado y listo para subirlo a git. Podemos seguir haciendo cambios y repitiendo el proceso de `git add . & git commit -m "mi mensaje"` o bien podemos subir nuestors cambios al servidor.
	- Para subir los cambios al servidor, simplemente ejecutamos el comando `git push origin main`, donde `origin` es nuestro servidor de git (que se configuró cuando clonamos el repositorio) y `main` es la rama/branch donde está alojada la versión de código en la que estamos trabajando.
4. Si todo funcionó bien, puede que la consola te esté pidiendo las credenciales de git en una ventana nueva o navegador. Una vez ingresadas, podrás confirmar en el repositorio que se agregó tu archivo de `PruebaGit.txt`.

### ¿Y si quiero agregar más cambios?

Para agregar más cambios, ahora ya no requerimos ejecutar el clon cada vez, si no que solo registramos los cambios y, cuando todo esté listo, lo subimos a nuestro github.

1. Abre y agrégale texto a tu archivo `PruebaGit.txt`.
2. En la consola, ejecuta:
	- `git add PruebaGit.txt` esta vez ejecutamos sólo la actualización del archivo `PruebaGit.txt`.
	- `git commit -m "cambio de contenido en archivo PruebaGit.txt"` registramos el cambio con un nombre de ello.
	- `git push origin main` subimos los cambios a la rama `main` de nuestro `origin` (servidor de github).
3. Vamos a github a ver los cambios.

Si todo está correcto, tu repositorio estará con los cambios y ahora sólo debes repetir este paso cada vez que quieras registrar los cambios.

### ¿Y las Ramas? ¿Que son?

Las ramas, o branches, son versiones paralelas de nuestro código, en otras palabras, que viven en conjunto a nuestro código `main` (rama por defecto),  y que, en algún momento, se podrían volver parte de él, o crear nuevas versiones desde ella.

Creemos un par de versiones y veamos que hacer con ellas:

1. Para crear nuestra nueva `rama` utilizaremos el comando `checkout` que también nos permite **cambiar entre ramas**.
	- Ejecutamos `git checkout -b prueba_git` donde `-b` es para inticar una nueva rama (`branch` en inglés).
	- Ésto nos dejará automáticamente una copia del código de la rama `main` en la nueva rama `pruebagit`.
2. Ahora podemos realizar cambios en esta rama y no alterar el proceso del código que ya poseemos en la rama `main` hasta que esté listo.
3. Si queremos registrar las modificaciones de esta rama nueva `pruebagit`:
	- `git add .` para agregar todos los cambios a "preparado".
	- `git commit -m "cambios en rama pruebagit"` para agregar un mensaje y empaquetar todos los cambios que están preparados.
	- `git push origin pruebagit` para subir los cambios y crear, en caso que no exista, la rama `pruebagit`.
4. Ahora tenemos dos ramas diferenciadas, `main` y `pruebagit`, donde `pruebagit` es una versión del código `main` que tiene **1 cambio extra**.

Ahora también podemos **Mezclar el código** entre ramas, para combinarlas o actualizar cambios que no poseo en mi rama de trabajo.

Para ello, utilizaremos los siguientes comandos:
- `git pull origin main` para actualizar la rama (en la que esté) desde el contenido del `main`, en otras palabras, estamos actualizando la rama `pruebagit` con lo que posea la rama `main` del servidor *github*.
- Otra forma de realizar algo similar es combinar ramas con `merge`, donde podemos ejecutarlo con `git merge [rama origen] [rama destino]`, ésto verificará si el código es combinable, y si poseemos tódas las mezclas de **bifurcaciones**.
- La última forma y la más recomendada: **Utilizar la herramienta Pull Request del agente**, la cuál se hace a través del mismo sitio web del Agente (Github en este caso).

Pull Request:
1. Ir a la sección `Pull Request` de nuestro 
![pt1PR](https://drive.google.com/uc?id=1yMU2089Rlt4P8SpQL3luK3AWV4DEmaGf)
2. Crear un nuevo `Pull Request`
![pt2PR](https://drive.google.com/uc?id=1taK9BIlJ2YQn6uoRpPOD4-Uac37IUr5r)
![pt3PR](https://drive.google.com/uc?id=1jXpCE6aKKRfPH_Clnzv65pnSN3aU7oCW)
3. Al aceptar un PR podemos realizar el MERGE de manera automática y eliminar la rama de origen (o bien mantenerla).
![pt4PR](https://drive.google.com/uc?id=1wbFXvRKjtFSrOkYm0puMahJXY1pyTPNY)
4. Si verificas la rama de destino (`main`), verás que se realizó un `commit` automático con los cambios de mezclar ambas ramas.
![pt4PR](https://drive.google.com/uc?id=1jek9jCZhr1T_txfpvoVsYKHVSVKq9U9s)

Con esto ya completamos y vimos todos los aspectos básicos de git.

¡Felicitaciones!
