# Instalación de Node JS

Node JS es un lenguaje programación que nos sirve para ejecutar JavaScript en la terminal de un ordenador. En Adalab y en muchas empresas lo utilizamos también para automatizar tareas y facilitarnos la vida mientras programamos. Vamos a instalarlo.

## Node JS desde Windows 10

1. Abre VS Code.
1. Abre una terminal.
1. Y sigue los pasos del siguiente apartado: Node JS desde Ubuntu.

## Node JS desde Ubuntu

Ejecuta las siguientes líneas en la terminal de una en una:

```bash
sudo apt install curl
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt install nodejs
```

## Node JS desde Mac

Ejecuta la siguiente línea en la terminal:

```bash
sudo brew install node@12
```

## Node JS: comprobando si lo hemos instalado bien

Una vez terminada la instalación de Node JS desde cualquiera de los 3 sistemas operativos debemos comprobar que todo ha ido bien. Para ello ejecutaremos en la terminal la siguiente línea:

```bash
node --version
```

Y la terminal debe mostrar la versión de Node JS instalada, algo como `v12.16.0`. **Es importante que empiece por v12.** Si por el contrario la terminal muestra el mensaje `No se ha encontrado la orden «node»...` es que algo hemos hecho mal. Vuelve a repetir todos los pasos y si no te funciona consulta a tu profesor.
