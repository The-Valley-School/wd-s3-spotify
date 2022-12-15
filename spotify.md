> [Recursos](recursos/assets.zip)

¡El siguiente reto al que os enfrentáis es a Spotify! ¿Qué tal suena eso? 

La idea, montar la funcionalidad de un reproductor de música (vamos a omitir el uso de la etiqueta audio para que nos nos volvamos locos trabajando en equipo)

![spotify](recursos/spotify1.png)
![spotify2](recursos/spotify2.png)

TIPS:

- Tendremos 2 formatos dependiendo del tamaño de pantalla:
    - Resoluciones menores a 768px tendrán el formato vertical
        - ancho máximo de la tarjeta 400px ;
    - Resoluciones mayores el formato horizontal
        - ancho máximo de la tarjeta 700px (40%px carátula, 60% reproductor);
- Nomenclatura BEM
- SCSS
- Gradiente del fondo: linear-gradient(to bottom right, #72FFB6, #10D164);
- Sombra de la tarjeta:  1px 1px 5px 1px rgba(0, 0, 0, 0.2);
- Color de la barra de progreso: #efefef;
- Otros colores: white, black, lightgray
- Todos los iconos están sacados de font-awesome y tienen una pequeña transición (hay que meter esta extensión en los span :) )


```
%player-action{
  transition: 300ms;
  &:hover{
    opacity: 0.7;
    cursor: pointer;
  }
}
```


- El listado de canciones es el siguiente:


```
const list = [
    {
        id: 0,
        author: "C.Tangana",
        title: "Me Maten",
        cover: "tangana_cover.png",
        duration: 10
    },
    {
        id: 1,
        author: "Rosalía",
        title: "Despechá",
        cover: "rosalia_cover.png",
        duration: 5
    },
    {
        id: 2,
        author: "Shakira",
        title: "Te felicito",
        cover: "shakira_cover.png",
        duration: 8
    },
    {
        id: 3,
        author: "Quevedo",
        title: "Quédate",
        cover: "quevedo_cover.png",
        duration: 12
    },
    {
        id: 4,
        author: "Bad Bunny",
        title: "Tití me preguntó",
        cover: "bad_cover.png",
        duration: 20
    }
];
```


- Os dejamos también la función que pasa los segundos a minutos para poder mostrarlos:


```
// Pasa los segundos a minutos
const getMinutes = (s) => {
    const minutes = (Math.floor(s / 60) < 10) ? '0' + Math.floor(s / 60) : Math.floor(s / 60);
    const seconds = (Math.floor(s % 60) < 10) ? '0' + Math.floor(s % 60) : Math.floor(s % 60);
    return minutes + ':' + seconds;
}
```


¡A por ello!