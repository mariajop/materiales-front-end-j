# Principales comandos de Git

### git *command* --help

Obtener ayuda sobre un comando:

```bash
git clone --help
```

```bash
git commit --help
```

### git clone

Clonar un repo en nuestro ordenador desde un repo remoto:

```bash
git clone url-de-repo-en-github
```

### git add

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

### git commit

```bash
git commit -m "Add footer styles"
```

### git push

Subir uno o varios commits al repositorio remoto:

```bash
git push
```

### git pull

Bajar los últimos commits desde el repositorio remoto:

```bash
git pull
```

### git status

Ver el estado de nuestro repo local:

```bash
git status
```

### git fetch

Sincroniza la información (de commits, ramas...) entre el repo remoto y el local, sin hacer ningún cambio en nuestro código ni en nuestro historial local de commits, lo podemos hacer siempre que queramos:

```bash
git fetch
```

### git log

Ver el listado de commits realizados:

```bash
git log
```

Para salir de `git log` y volver a la terminal hay que pulsar `q`.

### git init

Crea un repositorio desde cero en nuestro ordenador:

```bash
git init
```

### git add remote

Enlaza un repositorio de nuestro ordenadro con un repositorio remoto:

```bash
git remote add origin url-del-repositorio-que-me-da-github
```