# Ya estamos en VSCode

Ahora que ya importaste el repositorio a VSCode, vas a encontrar que hay un monton de carpetas y archivos, no te asustes, es normal, es el proyecto de la pagina web que vamos a hacer.

## Que es todo esto?

### Introduccion

Este proyecto esta hecho con [vite](https://vitejs.dev/), que es un programa que toma todos los archivos que estan en la carpeta y los convierte en un solo archivo que el navegador puede entender.
Por ejemplo, cuando en tu `index.html` queres aplicar estilos, pones:

```html
<link rel="stylesheet" href="./styles/style.css">
```
Esto lo que hace es decirle al navegador que tiene que buscar el archivo `style.css` en la carpeta `styles`, y aplicar esos estilos a la pagina web.

Vos vas a ir agregando archivos a las carpetas, y vite se va a encargar de que todo funcione.


### Archivos

* `index.html`
  Es el archivo principal, es el que se va a abrir cuando entres a la pagina web
* `readme.md`
  Este es el archivo que lees cuando entras al repositorio en github, es el que tiene toda la informacion del proyecto , pero realmente no afecta en nada a la pagina. Solo es una documentacion.
  Es un archivo de texto, pero con formato especial, se llama markdown, por eso la extension `.md`. Si queres saber mas sobre markdown, podes leer [este articulo](https://www.markdownguide.org/basic-syntax/)
Cuando haces click en los links del readme, te lleva a otros archivos, como este, que estan en la carpeta `docs`.
* `package.json`
  Este archivo tiene informacion sobre el proyecto, como el nombre, la version, y las dependencias. Las dependencias son otros proyectos que este proyecto necesita para funcionar. Por ejemplo, este proyecto usa `vite` para tomar todos los archivos, y convertirlos en un solo archivo que se pueda usar en la pagina web. Si queres saber mas sobre `vite`, podes leer [este articulo](https://vitejs.dev/guide/).
* `package-lock.json`
  Este archivo es generado automaticamente por `npm`, que es un programa que viene con `nodejs`, que es un programa que te permite correr javascript en tu compu. Este archivo no lo vamos a tocar, pero es importante que este ahi.
* `.gitignore`
  Este es un archivo que le dice a `git` que archivos no tiene que tener en cuenta. Por ejemplo, `node_modules` es una carpeta que se crea cuando ejecutas `npm install`. Es una copia en tu pc de las librerias que precisa nuestro proyecto para funcionar. Como es una copia, no es necesario que este en el repositorio, porque se puede volver a crear cuando se necesite. Por eso, esta en el `.gitignore`.
  Las librerias son projectos de otra gente que nos sirven en el nuestro. Pero estas librerias, los autores ya las tienen en sus repositorios, por eso no es necesario que esten en el nuestro. Solamente registramos en `package.json` que librerias necesitamos, y `npm` se encarga de descargarlas y ponerlas en `node_modules`.
  Cuando decimos que no estan en nuestro projecto, esto quiere decir que si vas a github, y entras a la carpeta `node_modules`, no vas a encontrar nada. Pero si entras a la carpeta `node_modules` en tu pc, vas a encontrar todas las librerias que necesitamos descargadas, para poder usarlas en nuestro proyecto.

### Carpetas

  * `docs`
    Esta carpeta tiene todos los archivos que se usan en el readme. Por ejemplo, el archivo `ya_estamos_en_vscode.md` es el que estas leyendo ahora. Cuando haces click en el link del readme, te lleva a este archivo.
  * `node_modules`
    Esta carpeta tiene todas las librerias que necesitamos para que el proyecto funcione. Como dijimos antes, no esta en el repositorio, pero si en tu pc.
  * `public`
    En esta carpeta ponemos todos los archivos que queremos que esten disponibles en la pagina web. Por ejemplo, si queres poner una imagen, la pones en esta carpeta, y despues en el `index.html` pones:
    ```html
    <img src="./imagen.png">
    ```
    Y el navegador va a buscar la imagen en la carpeta `public`, y la va a mostrar en la pagina web.
  * `styles`
    En esta carpeta ponemos todos los archivos de estilos. Por ejemplo, si queres poner un color de fondo, pones en `styles/style.css`:
    ```css
    body {
      background-color: red;
    }
    ```
    Y el navegador va a buscar el archivo `style.css` en la carpeta `styles`, y va a aplicar esos estilos a la pagina web.
    Podes tenes mas de un archivo css, esto es util para separar los estilos de distintas partes de la pagina. En realidad podrian estar todos en uno solo, pero es mas facil de mantener si estan separados.
    Por ejemplo, si tengo una pagina que tiene un menu, y un contenido, puedo tener un archivo `menu.css` y un archivo `contenido.css`, y en el `index.html` pongo:
    ```html
    <link rel="stylesheet" href="./styles/menu.css">
    <link rel="stylesheet" href="./styles/contenido.css">
    ```
    Y el navegador va a buscar los archivos en la carpeta `styles`, y va a aplicar esos estilos a la pagina web.
  * `dist`
    Esta carpeta puede que no la veas al principio. Es una carpeta que la genera `vite` cuando le mandamos el comando `build`. Basicamente, todo lo que hacemos en el proyecto, lo hacemos repartido en muchos archivos y carpetas. Cuando hacemos un `build`, `vite` se encarga de tomar todos esos archivos y carpetas, y convertirlos en un solo archivo que el navegador pueda entender. Esta carpeta no la vamos a editar nunca, porque la genera `vite` automaticamente. Es lo que vamos a terminar subiendo en algun momento al hosting.