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

## Windows 10 (mover a instalación de la terminal)

Si tienes Windows 10 vamos a instalar (un mini) Ubuntu dentro de tu Windows 10. Para ello:

1. Desde el menú inicio de tu Windows busca y abre **Microsoft Store**.
1. En el buscador del store busca **Ubuntu**.
1. Instala **Ubuntu 18.04 LTS**.
1. Verás que en tu menú inicio se habrá añadido un programa llamado **Ubuntu 18.04 LTS**.
1. Al instalar te pedirá que añadas una nueva contraseña. **Esta contraseña es la que utilizaremos siempre para la terminal.** No la pierdas!!

Una vez terminado debes:

1. Desde el menú inicio de tu Windows busca y abre **Activar o desactivar las características de Windows**.
1. Activa la opción **Subsistema de Windows para Linux**. Acepta y reinicia.

Después de haber hecho estas dos cosas tu Windows contará con una **terminal** que funciona igual que si estuvieras trabajando en Linux.

## Ubuntu 18 (linux)

Si quieres trabajar en Ubuntu y no lo tienes instalado a continuación te explicamos cómo hacerlo. Hay dos opciones:

- Instalar Ubuntu borrando todo lo que hay en el ordenador (recomendada): esta opción es obligatoria para equipos viejos que no tienen recursos para tener a la vez Windows y Linux.
- Instalar Ubuntu junto a Windows: crearemos una partición del disco duro del ordenador para instalar Ubuntu y luego poder arrancar el ordenador desde el SO que elijamos. Esta opción es más compleja y depende del ordenador concreto que tengáis que pueda hacerse o no.

> **IMPORNTANTE:** Antes de proceder a la instalación es muy importante **hacer una copia de seguridad de los datos** que estén en el ordenador y que no queramos perder.

Usaremos la distribución de Ubuntu 18.04, que podemos descargar una ISO desde http://releases.ubuntu.com/18.04/ y grabaremos en un CD o pendrive. El día de la sesión de bienvenida os ayudaremos a instalarlo y llevaremos pendrives preparados con esta versión. Seguiremos los pasos de instalación para instalar y configurar el sistema.

Si queremos mantener Windows, tendremos que hacer una partición:

- Hacer partición e instalar Ubuntu siguiendo este tutorial (mínimo de 30GB): https://www.tecmint.com/install-ubuntu-alongside-with-windows/

> NOTA: Al elegir instalar ubuntu, seleccionamos la opción de "opciones adicionales" para elegir en qué partición hacerlo. Una vez seleccionada la partición donde instalar Ubuntu, elegir que el gestor de arranque (bootloader) se instale en el disco duro principal en un desplegable abajo de la pantalla.

> NOTA: En Adalab los profesores trabajamos con UBUNTU 18. Si quieres usar otra distribución de Linux, no podemos garantizar que sabremos resolver todos los problemas relacionados con el sistema operativo.

#### Posibles problemas en la instalación de Ubuntu

- En equipos de la marca MSI, [suele haber problemas con los drivers de teclado / ratón en la instalación, de la tarjeta gráfico y/o de la conexión WiFi](https://gist.github.com/mari-linhares/cef4cb3440408e44963d1447a7db5ae0).
- En algunos Asus, no funciona la conexión Wifi, y [hay que instalar los drivers](https://askubuntu.com/questions/990378/wi-fi-not-working-on-lenovo-thinkpad-e570-realtek-rtl8821ce) que podéis pasar en un pendrive o con una conexión a Internet a través de vuestro móvil.
- También encontramos otras incompatibilidades de hardware (ordenador) con Ubuntu, [como esta que nos ha sucedido](https://askubuntu.com/questions/38780/how-do-i-set-nomodeset-after-ive-already-installed-ubuntu).

## Mac

Si utilizas Mac no necesitas instalar nada ya que el sistema operativo ya cuenta con una terminal adecuada para programar.