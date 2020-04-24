# Instalación de ordenadores para el curso de Adalab

## Requerimientos mínimos del ordenador

En el curso de programación front-end de Adalab necesitaremos usar un ordenador. Para poder realizar el curso de forma fluida, el ordenador debería tener estas características (no es obligatorio que las tenga, pero para que tengáis una orientación):

- Al menos 8GB de RAM (con 4GB irá algo más lento pero también se puede).
- Procesador i5 o similar con velocidad superior a 1GHz.
- Disco duro: recomendamos desde 128GB; si es SSD va a ir más fluido que si es HDD pero se puede tener más capacidad por menos precio.
- Tarjeta gráfica y pantalla: cualquiera pueden ir bien, aunque recomendamos pantalla de 15’ o como mínimo 13’ para poder programar junto a una compañera (con pantallas más pequeñas es posible pero se hace más complicado).

Para poder realizar el curso el sistema operativo (SO) del ordenador debe ser uno de los siguientes:

- **Windows 10**
- **Ubuntu 18**
- **Mac**

## Instalación del sistema operativo

### Ubuntu 18 (linux)

Si quieres trabajar en Ubuntu y no lo tienes instalado a continuación te explicamos cómo hacerlo. Hay dos opciones:

- Instalar Ubuntu borrando todo lo que hay en el ordenador (recomendada): esta opción es obligatoria para equipos viejos que no tienen recursos para tener a la vez Windows y Linux.
- Instalar Ubuntu junto a Windows: crearemos una partición del disco duro del ordenador para instalar Ubuntu y luego poder arrancar el ordenador desde el SO que elijamos. Esta opción es más compleja y depende del ordenador concreto que tengáis que pueda hacerse o no.

> NOTA: Antes de proceder a la instalación es muy importante **hacer una copia de seguridad de los datos** que estén en el ordenador y que no queramos perder.

Usaremos la distribución de Ubuntu 18.04, que podemos descargar una ISO desde http://releases.ubuntu.com/18.04/ y grabaremos en un CD o pendrive. El día de la sesión de bienvenida os ayudaremos a instalarlo y llevaremos pendrives preparados con esta versión. Seguiremos los pasos de instalación para instalar y configurar el sistema.

Si queremos mantener Windows, tendremos que hacer una partición:

- Hacer partición e instalar Ubuntu siguiendo este tutorial (mínimo de 30GB): https://www.tecmint.com/install-ubuntu-alongside-with-windows/

> NOTA: Al elegir instalar ubuntu, seleccionamos la opción de "opciones adicionales" para elegir en qué partición hacerlo. Una vez seleccionada la partición donde instalar Ubuntu, elegir que el gestor de arranque (bootloader) se instale en el disco duro principal en un desplegable abajo de la pantalla.

> NOTA: En Adalab los profesores trabajamos con UBUNTU 18. Si quieres usar otra distribución de Linux, no podemos garantizar que sabremos resolver todos los problemas relacionados con el sistema operativo.

#### Problemas en la instalación de Ubuntu

- En equipos de la marca MSI, [suele haber problemas con los drivers de teclado / ratón en la instalación, de la tarjeta gráfico y/o de la conexión WiFi](https://gist.github.com/mari-linhares/cef4cb3440408e44963d1447a7db5ae0).
- En algunos Asus, no funciona la conexión Wifi, y [hay que instalar los drivers](https://askubuntu.com/questions/990378/wi-fi-not-working-on-lenovo-thinkpad-e570-realtek-rtl8821ce) que podéis pasar en un pendrive o con una conexión a Internet a través de vuestro móvil.
- También encontramos otras incompatibilidades de hardware (ordenador) con Ubuntu, [como esta que nos ha sucedido](https://askubuntu.com/questions/38780/how-do-i-set-nomodeset-after-ive-already-installed-ubuntu).

### Windows 10

Si tienes Windows 10 vamos a instalar (un mini) Ubuntu dentro de tu Windows 10. Para ello:

1. Desde el menú inicio de tu Windows busca y abre **Microsoft Store**.
1. En el buscador del store busca **Ubuntu**.
1. Instala **Ubuntu 18.04 LTS**.
1. Verás que en tu menú inicio se habrá añadido un programa llamado **Ubuntu 18.04 LTS**.
1. Al instalar te pedirá que añadas una nueva contraseña. Esta contraseña es que utilizaremos siempre para la consola de Ubuntu. No la pierdas!!

Una vez terminado debes:

1. Desde el menú inicio de tu Windows busca y abre **Activar o desactivar las características de Windows**.
1. Activa la opción **Subsistema de Windows para Linux**. Acepta y reinicia.

Después de haber hecho estas dos cosas tu Windows contará con una consola (o terminal que es lo mismo) que funciona igual que si estuvieras trabajando en Linux.

Por último:

1. Instala VS Code (más abajo explicamos cómo hacerlo).
1. Abre la configuración de VS Code pulsando en el icono de la tuerca (esquina inferior izquierda) y a continuación **Settings**.
1. Busca la opción **Terminal > External: Windows exec**.
1. Añade el texto **C:\windows\System32\cmd.exe**.
1. Abre una terminal puslando en el menú superior > **Terminal** > **New terminal**: una nueva terminal se abrirá en la parte inferior de VS Code.
1. En dicha parte inferior hay un desplegable, ábrelo y pulsa en **Select default shell**.
1. Selecciona la opción **WSL Bash**.

Si tienes problemas para realizar alguno de estos pasos te ayudaremos durante la sesión de bienvenida del curso.

## Instalación de los programas

Una vez preparado el sistema operativo, instalaremos los siguientes programas para el curso:

- **Node:** es un programa que nos permite ejecutar JavaScript en nuestro ordenador y lo vamos a usar para que nos ayude a programar y a automatizar tareas.
- **Git:** es un repositorio de código para organizar, almacenar y compartir nuestros proyectos. Algo así como el Drive o el Dropbox de los programadores.
- **Zoom:** es para hacer video llamadas.
- **VS Code:** es el editor de código de moda.
- **Slack:** es un WhatsApp orientado a empresas.

> NOTA: En los siguientes pasos vamos a escribir `sudo` en la terminal. Siempre que escribimos `sudo` la terminal nos pedirá una contraseña, esto es porque vamos a instalar cosas en **modo Administrador**. En Ubuntu y Mac es la contraseña del usuario. En Windows es la contraseña que pusimos al instalar el mini Ubuntu.

### Node JS desde Ubuntu

Ejecuta las siguientes líneas en la terminal de una en una:

```bash
sudo apt install curl
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt install nodejs
```

### Node JS desde Windows 10

1. Desde el menú inicio abre Ubuntu.
1. Y sigue los pasos del apartado anterior: Node JS desde Ubuntu.

### Node JS desde Mac

Ejecuta la siguiente línea en la terminal:

```bash
sudo brew install node@12
```

### Node JS: comprobando si lo hemos instalado bien

Una vez terminada la instalación de Node JS desde cualquiera de los 3 sistemas operativos debemos comprobar que todo ha ido bien. Para ello ejecutaremos en la terminal la siguiente línea:

```bash
node --version
```

Y la terminal debe mostrar la versión de Node JS instalada, algo como `v12.16.0`. **Es importante que empiece por v12.** Si por el contrario la terminal muestra el mensaje `No se ha encontrado la orden «node»...` es que algo hemos hecho mal. Vuelve a repetir todos los pasos y si no te funciona consulta a tu profesor.

### Git desde Ubuntu

Ejecuta las siguientes líneas en la terminal de una en una:

```bash
sudo apt update
sudo add-apt-repository ppa:git-core/ppa
sudo apt install git
```

### Git desde Windows

1. Desde el menú inicio abre Ubuntu.
1. Y sigue los pasos del apartado anterior: Git desde Ubuntu.
1. Y también descarga e instala [Git para Windows](https://git-scm.com/download/win).

### Git desde Mac

Descarga e instala Git desde [esta página](https://git-scm.com/download/mac).

### Git: comprobando si lo hemos instalado bien

También debemos comprobar que Git se ha instalado correctamente la versión 2.x escribiendo en la terminal la siguiente línea:

```bash
git --version
```

Y la terminal debe mostrar la versión de Git instalada, algo como `git version 2.17.1`. Si por el contrario la terminal muestra el mensaje `No se ha encontrado la orden git...` es que algo hemos hecho mal. Vuelve a repetir todos los pasos y si no te funciona consulta a tu profesor.

### Zoom desde Ubuntu

- Accede al instalador de aplicaciones desde el menú
- Buscar Zoom e instálalo.

### Zoom desde Windows

- Descarga e instala [Zoom](https://zoom.us/support/download).

### Zoom desde Mac

- Descarga e instala [Zoom](https://zoom.us/support/download).

### Otros programas

Necesitamos instalar VS Code, Chrome y Slack. Desde Windows y Mac podemos instalar estos programas accediendo a las siguientes páginas:

- VS Code (https://code.visualstudio.com/)
- Chrome (https://www.google.com/chrome/)
- Slack (https://slack.com/)

Desde Ubuntu, la forma más cómoda es acceder al instalador de aplicaciones desde el menú, y ahí buscar cada programa e instalarlo.

## Creación de cuentas

### Cuenta de Zoom

- Crea una cuenta en [Zoom](https://zoom.us/signup).
- Usa el mismo email de Gmail que has proporcionado a Adalab.
- No uses el botón de **Iniciar sesión con Google**.

Inicia sesión en la aplicación de Zoom:

- Abre la aplicación de Zoom de tu ordenador.
- Mete tu email y contraseña en el formulario de la izquierda.
- No uses el botón **Ingresar con Google**.

### Cuenta de GitHub

- Crea una cuenta en [GitHub](https://github.com/).
- Usa el mismo email de Gmail que has proporcionado a Adalab.
- A la hora de elegir tu nombre de usuaria ten en cuenta que será parte de vuestro futuro perfil profesional.

### Cuenta de Trello

- Crea una cuenta en [Trello](https://trello.com/).
- Usa el mismo email de Gmail que has proporcionado a Adalab.
- A la hora de elegir tu nombre de usuaria ten en cuenta que será parte de vuestro futuro perfil profesional.

> **Nota:** Si tienes algún problema durante la instalación o la creación de cuentas, no te preocupes, díselo a tu profesora el primer día de clase.