![Adalab](https://beta.adalab.es/resources/images/adalab-logo-155x61-bg-white.png)

# ❄️ We ❤︎ Components: Evaluación Final-masopego

Como parte de la evaluación final del Módulo I (HTML y CSS), se nos propone maquetar la _home_ de la página ficticia "Anonymous Proxy".

Durante las 12 horas que duraba el ejercio, se nos plantea resolver varios puntos:

- Usar **Sass**.
- Usar **flexbox** y **CSS Grid**.
- Usar **media queries**.
- Resolver algunas **interacciones** usando transiciones.
  -Emplear **Gulp** para automatizar tareas.

## Módulo 1

- Incorporar un botón de hamburguesa en la esquina superior izquierda y mantenerse fijo al realizar scroll.
- Enlazar el menú hamburguesa con la página de Adalab.

## Módulo 2

El objetivo de esta sección es dar la bienvenida al usuario a la página y captar su atención desde el primer momento. Entre los retos que nos encontramos tenemos:

- Establecer una imagen de fondo que ocupe toda la ventana del navegador.
  Maquetarlo completamente en flexbox.

Además de resolver los retos, incorporamos una animación a la cabecera: "Snow". Cogiendo de base una imagen de puntos blancos y fondo transparente en png, la posicionamos encima de la imagen de fondo del header. Para realizar el efecto de la transición, usamos su background-position. Para aumentar el efecto, jugamos con el background-size, la opacidad y el desenfoque.

```
&__snow {
  position: absolute;
  top: 0px;
  bottom: 0px;
  right: 0px;
  left: 0px;
  background-image: url(http://www.freepngimg.com/download/winter_snow/4-2-white-snow-png.png);
  animation-name: snow-city;
  animation-duration: 40s;
  animation-timing-function: linear;
  animation-iteration-count: infinite; }`

@keyframes snow-city {
  from {
    opacity: 0.5;
    filter: blur(0.1xp);
    background-size: 300px;
    background-position: 0 -2000px;
  }

  to {
    opacity: 0.7;
    filter: blur(0.5px);
    background-size: 550px;
    background-position: 0 -1000px;
  }
}
```

Para realizar esta animación, nos hemos inspirado en la página de Movistar+ Series. [Aquí](https://lazona.movistarplus.es/), un ejemplo.

## Módulo 2

Se trata de la primera sección del _main_. Los retos que encontramos fueron:

- Maquetarlo para que mantuviera en todos los dispositivos alineación a la izquierda.

Como parte de las mejoras indispensables, tenemos que insertar una transición en el botón "Go". Nos decantamos por cambiar el _background-color_, _box-shadow_, _border_, _color_.

```
&:hover {
    color: $color-primary;
    background-color: $color-dark;
    box-shadow: 0 1px 2px 0 $color-dark;
    border: 2px solid $color-dark;
}
```

## Módulo 3

En esta sección, se presentan los siguientes retos:

- Maquetar los 3 elementos del listado con CSS Grid en todos los tamaños de pantalla.

Además de cumplir con este requisito, incluimos en la maquetación con CSS Grid el título de la sección y el botón de "More reasons".

Como parte de las mejoras indispensables, tenemos que insertar una transición en el botón "Go". Nos decantamos por cambiar el _background-color_, _box-shadow_, _border_.

```
&:hover {
  background-color: $color-dark;
  box-shadow: 0 1px 2px 0 $color-dark;
  border: 2px solid $color-dark;
}
```

## Módulo 4

En esta sección, se presentan los siguientes retos:

- Maquetar el footer usando flexbox.
- Todos los elementos de la columna "Articles" y "Twitter" tienen que ser enlaces a la página de Adalab.

Además de realizar estas cuestiones, añadimos una animación al botón de footer para que se mantenga siempre flotando, como si diera saltos. Para favorecer una animación fluida, le añadimos cuatro posiciones:

```
&__scroll {
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  transform: translate(0, -25px);
  animation-name: button-move;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}


@keyframes button-move {
  0% { transform: translate(0, -30px); }
  50% { transform: translate(0, -25px); }
  50% { transform: translate(0, -25px); }
  100% { transform: translate(0, -30px); }
}
```

También, incluimos una pequeña animación a los enlaces para que cambien de color suavemente cuando se hace _hover_:

```
& a {
  padding: 2px;
  transition: color ease 0.5s;
  &:hover { color: $color-bright; }
}
```
