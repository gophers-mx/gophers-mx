---
title: 'Como Agregar Un Recurso'
date: 2021-04-05T19:38:49-05:00
draft: false
author: 'Jorge Acero'
twitter: 'https://twitter.com/imjulianeral'
github: 'https://github.com/imjulianeral'
cover_image: '/img/blog/como-agregar-un-recurso/cover.png'
description: 'Como contribuir a la comunidad agregando un nuevo recurso'
tags: ['tag']
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

## Añade tu recurso

Para añadir tu recurso tienes que ejecutar el siguiente comando en tu terminal:

```bash
hugo new recursos/nombre-recurso.md
```

Este comando creará un arhivo markdown en el directorio `content/recursos/nombre-recurso.md`, por favor abre el archivo; verás una serie de propiedades que debes llenar **todas son obligatorias**.

La imagen del recuros debes de ponerla dentro del directorio: `static/img/recursos/nombre-recurso.jpg` y cuando termines de llenar todas las propiedades asegurate de cambiar `draft` a `false` **de otra manera no aparecerá en producción**.

```toml
---
title: "Resource Name"
draft: true
cover_image: /img/resources/title.png
description: "brief summary"
categories: ['category']
link: 'https://resourcewebsite.com'
---
```

## Consideraciones.

- Por favor usa [tinypng](https://tinypng.com/) para reducir el tamaño de la imagen.
- Puedes añadir cuantas categorias quieras pero debe de ser solo una palabra y en minúscula.
- Por favor verifica cuales categorias ya existen para evitar duplicados.

## Fin.

Eso fue todo lo que ocupas para añadir recursos, gracias por contribuir con la comunidad. 😊
