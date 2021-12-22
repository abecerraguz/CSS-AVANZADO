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
- Sass Nested
- Referencia al bloque padre &
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
    @import 'reset';
    @import 'grid';
    @import 'nav';

```

## Sass Nested
```scss

.nav{
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: $bg-black;
    color: $font-color;
    &__brand{
        width: 150px;
        height: auto;
        display: flex;
        img{
            width: 100%;
            height: auto;
        }
    }

    &__navegation{
        list-style: none;
        display: flex;
    }

    &__button{
       @extend .button;
        background:$bg-button;
        color: $font-color;
        transition: all 0.3s ease-in-out;
    }

    &__button:hover{
        @extend .button;
         background:$bg-button-active;
         color: $font-color;
     }

    &__button-background{
        @extend .button;
         background:$bg-button-active;
         color: $font-color;
     }

}

```
## REFERENCIA AL BLOQUE PADRE
El carácter especial & siempre se reemplaza por el selector padre
```scss
    #main {
    color: black;
    a {
        font-weight: bold;
        &:hover { color: red; }
    }
    }
```

Se compila en CSS:
```scss
    #main { color: black; }
    #main a { font-weight: bold; }
    #main a:hover { color: red; }
```