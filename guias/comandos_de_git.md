
En esta guía **estamos recopilando todo lo que enseñamos en los tres módulos** del curso sobre Git y GitHub. No es necesario conocer ni dominar Git antes de empezar el curso de Adalab, os lo iremos enseñando poco a poco. Mucha de esta información y de estos vídeos están también en algunas de las lecciones de los módulos 1 y 2.

Git es una herramienta que **se aprende con el uso y la práctica**.

Está guía está dividida en tres partes: principales comandos de Git, vídeos y Git stash.

# Principales comandos de Git

## git *command* --help

Obtener ayuda sobre un comando:

```bash
git clone --help
```

```bash
git commit --help
```

## git clone

Clonar un repo en nuestro ordenador desde un repo remoto:

```bash
git clone url-de-repo-en-github
```

## git add

Añadir todos los ficheros modificados al próximo commit:

```bash
git add -A
```

Añadir algunos ficheros modificados al próximo commit:

```bash
git add nombre-de-fichero
```

```bash
git add nombre-de-una-carpeta/*
```

## git commit

```bash
git commit -m "Add footer styles"
```

## git push

Subir uno o varios commits al repositorio remoto:

```bash
git push
```

Subir los últimos commits al remoto después de crear una rama:

```bash
git pull -u origin nombre-de-rama
```

## git pull

Bajar los últimos commits desde el repositorio remoto:

```bash
git pull
```

## git status

Ver el estado de nuestro repo local:

```bash
git status
```

## git fetch

Sincroniza la información (de commits, ramas...) desde el repo remoto al local, sin hacer ningún cambio en nuestro código ni en nuestro historial local de commits, lo podemos hacer siempre que queramos:

```bash
git fetch
```

## git branch

Listar las ramas locales:

```bash
git branch
```

Listar las ramas remotas:

```bash
git branch -r
```

Crear una rama (sin movernos a ella):

```bash
git branch nombre-de-la-nueva-rama
```

## git checkout

Movernos desde la rama actual a otra rama:

```bash
git checkout nombre-de-otra-rama
```

Crear y movernos a una rama en un solo comando:

```bash
git checkout -b nombre-de-la-nueva-rama
```

## git merge

Mover el código desde la rama de origen hacia la rama en la que estoy:

```bash
git merge nombre-de-rama-origen
```

## git log

Ver el listado de commits realizados:

```bash
git log
```

Para salir de `git log` y volver a la terminal hay que pulsar `q`.

## git init

Crea un repositorio desde cero en nuestro ordenador:

```bash
git init
```

## git add remote

Enlaza un repositorio de nuestro ordenadro con un repositorio remoto:

```bash
git remote add origin url-del-repositorio-que-me-da-github
```

# Vídeos de Git

## Crear un repositorio

[Vídeo](https://www.youtube.com/watch?v=MGf3K6qxptg) sobre cómo crear y clonar un repositorio:

{% embed url="https://www.youtube.com/watch?v=MGf3K6qxptg" %}

## Añadir cambios a un repositorio

[Vídeo](https://www.youtube.com/watch?v=QQOHttHNtY0) sobre cómo añadir commits a un repositorio con los comandos `add`, `commit`, `push` y `pull`:

{% embed url="https://www.youtube.com/watch?v=QQOHttHNtY0" %}

## Merges blandos y duros

[Vídeo](https://www.youtube.com/watch?v=jDOVhbgc8Ec) sobre cómo trabajar dos personas en paralelo en un repositorio y cómo solucionar merges blandos (cuando ambas personas tocan diferentes líneas de código) y merges duros (cuando ambas personas tocan la misma línea):

{% embed url="https://www.youtube.com/watch?v=jDOVhbgc8Ec" %}

## Trabajar con varias ramas

[Vídeo](https://www.youtube.com/watch?v=MnaRLneoiSo) sobre cómo trabajar con varias ramas, movernos entre ramas, publicarlas y mergear una rama en otra:

{% embed url="https://www.youtube.com/watch?v=MnaRLneoiSo" %}

## Flujo de ramas

[Vídeo](https://www.youtube.com/watch?v=t-GbqNDrJ4A) sobre qué ramas debemos usar y cómo y cuándo debemos mover el código entre las diferentes ramas para mantener la mejor calidad de código:

{% embed url="https://www.youtube.com/watch?v=t-GbqNDrJ4A" %}

# Git stash

Git stash es una herramienta muy útil pero un poco avanzada. No la explicamos durante el curso, pero os la explicamos aquí para que cuando estéis muy aburridas podáis aprender algo nuevo :)

## ¿Qué es?

Git nos permite guardar el código modificado y no commiteado a una especie de cajón temporal, al que llamaremos **stash** y recuperarlo más tarde.

## ¿Para qué sirve?

* Imagina que estás trabajando en la rama A y has hecho cambios en el código. Te quieres cambiar a la rama B pero todavía no quieres commitear los cambios actuales a la rama A.
* O estás trabajando en la rama A y quieres subir los cambios actuales a la rama B. Haces un checkout y Git te dice que no te puedes cambiar de rama porque hay cambios en tu código y no quiere sobre escribirlos ni borrarlos.
* O tienes un montón de cambios sin commitear y haces `git pull` y Git te da error porque si te bajas los commits de tus compañeras se machacan tus cambios.

**Solución:** guardamos el código en un stash, los cambios desaparecen de nuestra rama, es decir, se queda limpia, y ahora sí te puedes cambiar a la rama que quieras. Más tarde puedes recuperar tu código desde ese stash.

> **Nota:** puedes tener tantos stash como quieras.

## ¿Cómo funciona?

Una vez que tenemos cambios en nuestra rama, por ejemplo máster, que queramos guardar en un stash hacemos:

```bash
git stash push -m "Description of the code I am saving"
```

Ahora mi rama está limpia y me puedo cambiar a la rama que quiera.

**Más tarde en la rama que sea**, quiero recuperar el código. Para ver el listado de stash que tengo en este repo, hago:

```bash
git stash list
```

Y me aparece el listado de todos los stash, como por ejemplo:

```bash
stash@{0}: On master: Description of the code I am saving
stash@{1}: On header: Work in progress: header
```

Para recuperar el stash 0, es decir, para coger el código y ponerlo en nuestra rama, haremos:

```bash
git stash pop stash@{0}
```
Y en nuestra rama aparecerán los cambios como si los acabaramos de escribir ahora mismo, es decir, sin commitear.

## Borrar los stash

En el momento que queramos borrar los stash que hemos ido creando, haremos...

```bash
git stash list
```

... para saber el índice del stash que queremos borrar. Aquí vamos a borrar el stash 0.

```bash
git stash drop stash@{0}
```

## Importante

Todo estos movimientos de código para allá y para acá se hacen sin hacer commit, ni push, por lo que esto solo sucede en nuestro local. Nunca sube a remoto. Para que suba a remoto tenemos que crear un commit y hacer un push como siempre.
