# Freelancer

* **Track:** _Common Core_
* **Curso:** _Creando tu primer sitio web interactivo_
* **Unidad:** _Maquetado web con HTML & CSS_

***

## Objetivo

En este reto se nos pidió replicar la maquetación del template **Freelancer** de *Bootstrap*. Este debía ser el resultado final:

![Freelancer Website](docs/fullpage.png)


## Flujo de trabajo

Para cumplir con el objetivo, partí por dividir el sitio en diversas secciones, usando tanto las etiquetas `div` como los nuevos elementos semánticos de HTML5:

* `#container`: Contenedor que abarca todo el sitio.
* `nav`: Barra de navegación.
* `header`: El logo, título y descripción general de Freelancer.
* `section #portfolio`: Como el nombre lo indica, la sección en dónde se muestra el portafolio.
* `section #about`: Descripción más completa de Freelancer más el botón de descarga.
* `section #contact`: Formulario de contacto.
* `footer`: Parte inferior de la estructura web.

Cada sección a su vez contiene otras "cajas" que fueron usadas para encajar de mejor manera el contenido.

### Desafíos

* **Línea Horizontal:** Freelancer cuenta con una línea horizontal que se compone de dos líneas separadas por una estrella en medio. Se usa para subrayar las principales secciones del sitio. En mi caso, la creé haciendo varios `div` con la clase `.line`, que en CSS contenía las indicaciones correspondientes de tamaño y color. Hice la estrella usando un cáracter de *Font Awesome*.


* **Efectos de hover en `#portfolio`:** A pesar de que no se nos solicitó, quise encontrar una forma de replicar los efectos del sitio original en las imágenes de esta sección. Al principio consideré la opción de usar Javascript, pero finalmente me decanté por averiguar cómo hacerlo en CSS. En lugar de colocar las imágenes directamente en el sitio cómo había hecho en un principio, lo que hice fue crear elementos `figure` del tamaño correspondiente y como valor de `background` añadir cada una de las imágenes. Luego, dentro de cada `figure` añadí un nuevo elemento con la clase llamada `.overlay`. A `.overlay` le di un valor de opacidad de 0, el mismo tamaño que su contenedor, fondo de color verde agua con algo de transparencia (usando RGBa) y dentro de este inserté el elemento `i` con la clase correspondiente al símbolo usado en el sitio original que llama al ícono de *Font Awesome*. Al hacer *hover* sobre `.overlay` este aumenta su opacidad por completo con una breve transición. El efecto quedó bastante parecido.