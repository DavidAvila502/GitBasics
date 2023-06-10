# Bases de git

En este documento, encontrarás una guía rápida que abarca los comandos básicos y esenciales para utilizar Git y GitHub. Esta guía te ayudará a comenzar con el control de versiones y la colaboración en tus proyectos.

## Contenido

---

1. [Creación de repositorio local](#Creación-de-repositorio-local)
2. [Creación de una rama principal](#Creación-de-una-rama-principal)
3. [Agregar un origen a nuestro repositorio local](#Agregar-un-origen-a-nuestro-repositorio-local)
4. [Agregar elementos a nuestro repositorio local](#Agregar-elementos-a-nuestro-repositorio-local)
5. [Preparar repositorio local para empujar los cambios (commit)](#Preparar-repositorio-local-para-empujar-los-cambios)
6. [Empujar cambios al repositorio remoto (push)](#Empujar-cambios-al-repositorio-remoto)

## Creación de repositorio local

---

Para crear un repositorio local, necesitas ejecutar el comando `git init`. Este comando se utiliza para inicializar un repositorio de Git en la ruta actual. Asegúrate de dirigirte a la carpeta raíz de tu proyecto antes de ejecutarlo. Aquí tienes los pasos a seguir:

1. Abre una terminal o línea de comandos.

2. Navega a la carpeta raíz de tu proyecto utilizando el comando "cd" seguido de la ruta de la carpeta. Por ejemplo:

```bash
cd /ruta/de/la/carpeta/proyecto
```

3. Una vez que estés en la carpeta raíz de tu proyecto, ejecuta el siguiente comando:

```bash
git init
```

## Creación de una rama principal

---

GitHub utiliza ramas para almacenar proyectos. En este sistema de ramificación, hay una rama principal y también pueden existir ramas secundarias. En este caso, ejecutaremos el siguiente comando para crear localmente nuestra rama principal llamada "main":

```bash
git branch -M main
```

## Agregar un origen a nuestro repositorio local

---

Una vez que hayas creado un repositorio en GitHub y desees subir tu proyecto, que inicialmente está en tu repositorio local, necesitarás vincularlo con el repositorio remoto en GitHub. Esto te permitirá comenzar a subir tu proyecto y sus versiones posteriores al repositorio remoto. Para lograr esto, debes utilizar el comando `git remote add origin` seguido de la URL del repositorio remoto. Aquí tienes los pasos a seguir:

1. Copia la URL del repositorio remoto en GitHub. Puedes encontrarla en la página del repositorio en GitHub.

2. Abre una terminal o línea de comandos y navega hasta la carpeta raíz de tu proyecto.

3. Ejecuta el siguiente comando para vincular tu repositorio local con el repositorio remoto en GitHub:

```bash
git remote add origin <URL_del_repositorio_remoto>
```

Asegúrate de reemplazar `<URL_del_repositorio_remoto>` con la URL que copiaste en el paso anterior.

4. Verifica que la vinculación se haya realizado correctamente ejecutando el siguiente comando:

```bash
git remote -v
```

## Agregar elementos a nuestro repositorio local

---

Una vez que hayas ejecutado los pasos anteriores y tengas tu repositorio local configurado con la rama principal y el origen remoto en GitHub, puedes agregar los archivos a tu repositorio local utilizando el comando `git add`. Este comando te permite seleccionar los archivos que deseas incluir en el próximo commit. A continuación, te explico cómo usarlo:

1. Asegúrate de estar ubicado en la carpeta raíz de tu proyecto en la terminal o línea de comandos.

2. Utiliza el siguiente comando para agregar archivos específicos al área de preparación (staging):

```bash
git add archivo1 archivo2 ...
```

Reemplaza "archivo1", "archivo2", etc., con los nombres de los archivos que deseas agregar. Puedes especificar múltiples archivos separados por un espacio.

3. Si deseas agregar todos los archivos modificados en la carpeta actual y sus subcarpetas, puedes utilizar el siguiente comando:

```bash
git add .
```

Esto agregará todos los archivos modificados al área de preparación, este es el comando más habitual para agregar todo automaticamente.

4. Verifica el estado de los archivos agregados utilizando el comando "git status". Deberías ver los archivos que has agregado resaltados en verde.

## Preparar repositorio local para empujar los cambios

---

Despues de agregar los archivos al repositorio local utilizando el comando `git add`, es necesario realizar un commit para preparar los cambios y luego poder enviarlos al repositorio remoto. El commit es una acción que crea un punto de control en la historia del proyecto y registra los cambios realizados.

1. Asegúrate de estar ubicado en la carpeta raíz de tu proyecto en la terminal o línea de comandos.

2. Ejecuta el siguiente comando para realizar un commit con los cambios agregados:

```bash
git commit -m "Mensaje descriptivo"
```

Reemplaza "Mensaje descriptivo" con un texto breve y descriptivo que explique los cambios realizados en el commit. Este mensaje es útil para comprender rápidamente qué modificaciones se han realizado en el proyecto.

3. Una vez que ejecutes el comando, Git creará un commit con los cambios preparados. Esto guarda los cambios en tu repositorio local.

Es importante tener en cuenta que los commits son independientes y se pueden realizar múltiples commits antes de enviar los cambios al repositorio remoto. Cada commit representa un estado específico del proyecto en un momento dado.

Después de realizar el commit, puedes utilizar el comando "git push" para enviar tus cambios al repositorio remoto, como mencionamos anteriormente.

## Empujar cambios al repositorio remoto

---

Para subir tus cambios y tu proyecto al repositorio remoto en GitHub, puedes utilizar el comando `git push -u origin`. Este comando enviará tus archivos locales al repositorio remoto que has configurado previamente como `origin`. La opción "-u" establece la rama de seguimiento predeterminada para futuros empujes, lo que facilita los empujes posteriores. A continuación, te explico cómo utilizarlo:

1. Asegúrate de estar ubicado en la carpeta raíz de tu proyecto en la terminal o línea de comandos.

2. Ejecuta el siguiente comando para empujar tus cambios al repositorio remoto:

```bash
git push -u origin <nombre_rama>
```

Por ejemplo el caso de haber nombrado tu rama principal como `main` el comando será:

```bash
git push -u origin main
```

Reemplaza <nombre_rama> por el nombre de la rama en la que deseas realizar el empuje. Si estás utilizando la rama principal, reemplaza <nombre_rama> por `main`.

3. Git solicitará tus credenciales de GitHub (nombre de usuario y contraseña o token de acceso personal) para autenticar el empuje.

4. Una vez autenticado, los archivos locales serán empujados al repositorio remoto en GitHub. Esto puede tardar unos momentos dependiendo del tamaño de tu proyecto y la velocidad de tu conexión a internet.

Después de ejecutar el comando `git push -u origin` por primera vez, en futuros empujes podrás utilizar simplemente "git push" sin necesidad de especificar la rama, ya que Git recordará la configuración de seguimiento predeterminada.

Recuerda que es importante tener en cuenta las políticas de colaboración establecidas en tu proyecto y asegurarte de no sobrescribir el trabajo de otros colaboradores al realizar los empujes.
