---
title: 'Como Crear Un Post'
date: 2021-03-23T00:39:09-06:00
draft: false
author: 'Jorge Acero'
twitter: 'https://twitter.com/imjulianeral'
github: 'https://github.com/imjulianeral'
cover_image: '/img/blog/como-crear-un-post/cover.png'
description: 'Como contribuir a la comunidad creando tu propio post.'
tags: ['tutoriales', 'gophersmx']
---

¡Hola! Que bueno que quieras aportar a la comunidad con tu conocimiento, a continuación veras lo facil que es contribuir ❤️.

## Instalación de Hugo

![Hugo Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/a/af/Logo_of_Hugo_the_static_website_generator.svg/1024px-Logo_of_Hugo_the_static_website_generator.svg.png 'Hugo Logo')

Lo primero que ocupas que instalar es Hugo, Hugo es el generador de sitios estáticos que ocupamos para nuestra página.

### Instalación en Arch Linux

```bash
sudo pacman -Syu hugo
```

### Instalación en Debian & Ubuntu:

```bash
sudo apt-get install hugo
```

### Instalación en Fedora:

```bash
sudo dnf install hugo
```

### Instalación en Windows (Chocolatey):

```bash
choco install hugo -confirm
```

### Instalación en macOS (Homebrew):

```bash
brew install hugo
```

## Clona el repositorio de github.

Después de instalar Hugo puedes proceder a clonar el repositorio.

```bash
git clone https://github.com/gophers-mx/gophers-mx.github.io.git
```

## Crea tu rama.

Dentro del repositorio debes de crear tu propia rama.

```bash
git checkout -b blog/post-name
```

## Crea tu post.

Ahora puedes crear el archivo de markdown donde podrás escribir tu post.

```bash
hugo new blog/post-name.md
```

El archivo será creado dentro del directorio `content/blog/post-name.md`, ahora abre el archivo y verás algunos valores.

```toml
---
title: "Post Name"
date: 2021-03-30T20:55:43-06:00
draft: true
author: "Your name"
twitter: "https://twitter.com/username"
github: "https://github.com/username"
original_post: "https://blog.yoursite.com/post"
cover_image: '/img/blog/post-name/cover-image.jpg'
description: "post's brief summary"
tags: ['tag']
---
```

Todas las propiedades son obligatorias, excepto `original_post`; esa la puedes remover. Para entender mejor como llenar cada propiedad ocupas comprender de que se trata cada una:

### Author

Tu nombre.

### Draft.

De ser `true` **no se mostrará en producción, por favor cambialo a `false` cuando termines de escribir tu post**.

### Twitter

Tu cuenta de twitter.

### Github

Tu cuenta de Github.

### Original Post (Opcional)

Esta propiedad es completamente opcional ya que hace referencia al link del post original que escribiste en tu propio blog u otra plataforma.

### Cover Image

Es la miniatura del post, el tamaño recomendado es **1200x620px**. Debes de guardar esta imagen dentro del directorio `static/img/blog/post-name/cover.png`. De preferencia usa [tinypng](https://tinypng.com/) para reducir el peso tus imágenes.

### Description

Un resumen del post.

### Tags

Puedes añadir tags a tu post para categorizarlo, por favor verifica cuales tags ya existen para no repetirlos y cuando crees un tag por favor que solo sea una palabra y en minúsculas.

## Escribiendo el post.

Para escribir el post el único conocimiento que necesitas es la [sintaxis de markdown](https://www.markdownguide.org/basic-syntax/), pero si quieres optimizar algunas cosas para Hugo, puedes checar su [documentación](https://www.markdownguide.org/basic-syntax/).

Ahora para empezar a ver tu post dentro de el proyecto ocupas escribir el siguiente comando en tu terminal:

```bash
hugo serve -D
```

La bandera `-D` significa que va a mostrar los posts que tengan la propiedad `draft: true`, recuerda que tienes que cambiar el valor a `false` cuando termines de escribir tu post, **de otra manera no aparecerá en producción**.

Finalmente despues de terminar de escribir tu post, ejecuta en tu terminal:

```bash
hugo
```

Si el log no muestra ningún error, puedes proceder a crear tu pull request.

## Fin.

Eso ha sido todo, gracias por contribuir con la comunidad. 😊
