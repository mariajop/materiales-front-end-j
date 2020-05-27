
En esta guía estamos recopilando todo lo que enseñamos en los tres módulos del curso sobre Git y GitHub.

Está guía está dividida en tres partes:

- Principales comandos de Git.
- Vídeos sobre Git.
- Git stash.

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

Sincroniza la información (de commits, ramas...) entre el repo remoto y el local, sin hacer ningún cambio en nuestro código ni en nuestro historial local de commits, lo podemos hacer siempre que queramos:

```bash
git fetch
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

### Añadir cambios a un repositorio

[Vídeo](https://www.youtube.com/watch?v=QQOHttHNtY0) sobre cómo añadir commits a un repositorio con los comandos `add`, `commit`, `push` y `pull`:

{% embed url="https://www.youtube.com/watch?v=QQOHttHNtY0" %}

### Merges blandos y duros

[Vídeo](https://www.youtube.com/watch?v=jDOVhbgc8Ec) sobre cómo trabajar dos personas en paralelo en un repositorio y cómo solucionar merges blandos (cuando ambas personas tocan diferentes líneas de código) y merges duros (cuando ambas personas tocan la misma línea):

{% embed url="https://www.youtube.com/watch?v=jDOVhbgc8Ec" %}

# git stash

Git stash es una herramienta muy útil pero un poco avanzada. No la explicamos durante el curso, pero os la explicamos aquí para que cuando estéis muy aburridas podáis aprender algo nuevo :)

## ¿Qué es git stash?

Git nos permite guardar el código modificado y no commiteado a una especie de cajón temporal, al que llamaremos **stash** y recuperarlo más tarde.

## ¿Para qué sirve?

* Imagina que estás trabajando en la rama A y has hecho cambios en el código. Te quieres cambiar a la rama B pero todavía no quieres commitear los cambios actuales a la rama A.
* O estás trabajando en la rama A y quieres subir los cambios actuales a la rama B. Haces un checkout y Git te dice que no te puedes cambiar de rama porque hay cambios en tu código y no quiere sobre escribirlos ni borrarlos.

**Solución:** guardamos el código en un stash, los cambios desaparecen de nuestra rama, es decir, se queda limpia, y ahora sí te puedes cambiar a la rama que quieras. Más tarde puedes recuperar tu código desde ese stash.

> Nota: puedes tener tantos stash como quieras.

## ¿Cómo funciona?

Una vez que tenemos cambios en nuestra rama, por ejemplo máster, que queramos guardar en un stash hacemos:

```bash
git stash push -m "Description of the code I am saving"
```

Ahora mi rama está limpia y me puedo cambiar a la rama que quiera.

Más tarde en la rama que sea, quiero recuperar el código. Para ver el listado de stash que tengo en este repo, hago:

```bash
git stash list
```

Y me aparece el listado de todo s los stash, como por ejemplo:

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

Todo estos movimientos de código para allá y para acá se hacen sin hacer commit, ni push, por lo que esto solo sucede en nuestro local. Nunca sube a remoto.