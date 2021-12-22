# APUNTES SASS
Debemos tener instalado Node.js y NPM para saber si esta instalado se escribe en el terminal

- node --version

## INSTALANDO SASS
- npm install sass --save-dev `Un camino Instalando en el proyecto`
- npm install -g sass `Otro camino Instalando de forma global en el computodor o sea de forma global`

## CREAMOS UN PROYECTO CON SASS

- Creo Directorio, mkdir `02-iniciando-sass`
- Me posiciono dentro de, `02-iniciando-sass, escribo cd 02-iniciando-sass/`
- Escribo en la terminal o Gitbash(Window) `touch` para crear archivos `touch index.html`
- Escribo en la terminal o Gitbash(Window)  `mkdir` para crear la carpeta `assets`
- Me posiciono dentro de la carpeta, `assets, escribo cd assets/`
- Escribo en la terminal o Gitbash(Window)  `mkdir` para crear la carpeta `sass`
- Me posiciono dentro de la carpeta, `sass, escribo cd sass/`
- Escribo en la terminal o Gitbash(Window) `touch` para crear el archivo en formato sass `main.scss`
- Para iniciar la compilacion sass --watch styles.scss:styles.css
- Para terminar la compilación `Ctrl-C`

## TEMAS A VER:
- Crear variables
- Organizar Parciales (Patron 7-1) (Organizar mi proyecto)
- Nesting
- Referencia al bloque padre
- Uso de extends


## PARA CREAR VARIABLES EN SASS
```scss

    $primary-color:'red';
    $secondary-color:'orange';
    $tipografy-xx-large:'60px';

```
## ORGANIZAR PARCIALES (Patron 7-1) (Organizar mi proyecto)
```scss

    @import 'variables';

```