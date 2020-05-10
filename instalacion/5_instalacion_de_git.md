# Instalación y uso de Git / GitHub

## Introducción

### Qué es Git

### Qué es GitHub

### Crear una cuenta en GitHub

## Git desde Ubuntu

### Instalación

Ejecuta las siguientes líneas en la terminal de una en una:

```bash
sudo apt update
sudo add-apt-repository ppa:git-core/ppa
sudo apt install git
```

### Configuración

## Git desde Windows

### Instalación

1. Desde el menú inicio abre Ubuntu.
1. Y sigue los pasos del apartado anterior: Git desde Ubuntu.
1. Y también descarga e instala [Git para Windows](https://git-scm.com/download/win).

### Configuración

## Git desde Mac

### Instalación

Descarga e instala Git desde [esta página](https://git-scm.com/download/mac).

### Configuración

## Comprobar si lo hemos instalado bien

También debemos comprobar que Git se ha instalado correctamente la versión 2.x escribiendo en la terminal la siguiente línea:

```bash
git --version
```

Y la terminal debe mostrar la versión de Git instalada, algo como `git version 2.17.1`. Si por el contrario la terminal muestra el mensaje `No se ha encontrado la orden git...` es que algo hemos hecho mal. Vuelve a repetir todos los pasos y si no te funciona consulta a tu profesor.

## Crear nuestro primer repositorio para los ejercicios

### Explicar la estructura de carpetas que vamos a usar