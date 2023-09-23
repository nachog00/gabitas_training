# Comandos

Primero que nada, vamos a abrir la terminal. Para eso, en la barra de menu, vamos a `Terminal` -> `New Terminal`, o usamos la terminal de windows. Si usas la de vscode, te va a aparecer en la parte de abajo de la pantalla y ya va a estar en el directorio del proyecto. Si usas la de Windows tenes que navegar hasta el directorio del proyecto.

## Instalar dependencias

Nuestro proyecto precisa de algunas dependencias (librerias) para funcionar. Para instalarlas, vamos a usar el comando `npm install`. Este comando va a leer el archivo `package.json`, y va a instalar todas las dependencias que esten ahi.

```bash
npm install
```

Una vez que termina, vamos a tener una carpeta nueva, llamada `node_modules`. Esta carpeta tiene todas las dependencias que instalamos. Como dijimos antes, no esta en el repositorio, pero si en tu pc.

## Correr el proyecto

Para correr el proyecto, vamos a usar el comando `npm run dev`. Este comando va a leer el archivo `package.json`, y va a ejecutar el comando que esta en la seccion `scripts` con el nombre `dev`.

```bash
npm run dev
```

Este comando va a iniciar un servidor local, es decir, que podemos entrar a la pagina web desde nuestra pc. Para eso, cuando le das ejecutar al comando te va a salir un mensaje asi:

```bash
  > gabita-training@0.0.0 dev
  > vite

  vite v2.6.4 dev server running at:

  > Local: http://localhost:3000/
  > Network: use `--host` to expose

  ready in 1.03s.
```

Vamos a copiar la url que dice `Local`, y la vamos a pegar en el navegador. Vamos a ver la pagina web, y vamos a poder ver los cambios que hacemos en tiempo real.

Cuando terminamos de usar el servidor, podemos apretar `ctrl + c` en la terminal para cerrarlo, o simplemente cerrar la terminal.

## Compilar el proyecto

Esto lo vamos a usar cuando queramos subir el proyecto a un hosting.

Para compilar el proyecto, vamos a usar el comando `npm run build`. Este comando va a leer el archivo `package.json`, y va a ejecutar el comando que esta en la seccion `scripts` con el nombre `build`.

```bash
npm run build
```

Este comando va a generar una carpeta nueva, llamada `dist`. Esta carpeta tiene todos los archivos que necesita el navegador para mostrar la pagina web. Esta carpeta no la vamos a editar nunca, porque la genera `vite` automaticamente. Es lo que vamos a terminar subiendo en algun momento al hosting.



