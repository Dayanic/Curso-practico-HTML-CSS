# Lo que aprenderás sobre HTML y CSS
Bienvenido y bienvenida a este curso en el que pondrás en práctica todo lo aprendido en el [Curso Definitivo de HTML y CSS](https://platzi.com/cursos/html-css/). Por lo que si aún no lo has completado, te recomiendo que vayas y lo hagas. ¡Es muy completo!

Como proyecto, crearemos un clon de la página principal de Google, esa que ves cada que abres tu navegador Chrome. Para ello necesitaremos lo siguiente:

* Editor de texto
* Navegador

## ¿Qué es HTML y CSS?
Recordemos los conceptos básicos sobre los que vamos a trabajar.
**HTML** es un lenguaje de etiquetas para crear la estructura de la información de una página web.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2833%29.png)

Mientras que todas las etiquetas contenedoras (que llevan contenido) siempre llevan etiqueta de cierre, las etiquetas de contenido (que son el contenido) no siempre lo hacen.

**CSS** es un lenguaje de estilos en cascada que nos permite aplicar diseños a nuestra estructura en HTML.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2834%29.png)

Aplicamos los diseños usando reglas. Empleamos una declaración para un selector (casi siempre una etiqueta), que está compuesta por una propiedad y su valor.

**Recordatorio***: HTML y CSS no son lenguajes de programación.

### **Algunas librerías de las que puedes aprender**:
**Documentación sobre HTML, CSS y JS**:
https://developer.mozilla.org/en-US/

**Guía para entender las propiedades de CSS son ejemplos animados**:
https://cssreference.io/

**Guía completa de Flexbox**:
https://css-tricks.com/snippets/css/a-guide-to-flexbox/

**Aprende HTML con ejercicios**:
https://www.w3schools.com/html/default.asp

**Aprende sobre Flexbox jugando**:
https://flexboxfroggy.com/#es

# Análisis del proyecto Google Clone
Vamos a analizar la página principal de búsqueda de Google.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/2.jpg)
Notamos que no es la versión original porque en la URL se refleja el localhost. Sin embargo, es casi idéntica. Piensa en cómo pudo haber sido creada su estructura.

* Podríamos usar un *header* con una etiqueta nav.
* En el body crearíamos una *section* con una etiqueta *icon* o *img*.
* Un *input* para poder ingresar información en él.
* Además de un par de *button* para enviar la información.
* En el *footer* tenemos dos etiquetas *nav* que están alineadas a la izquierda y derecha, cada una con hiperenlaces dentro de sus textos.

A continuación, vamos a configurar nuestro proyecto para empezar a escribir código.

# Configuración del proyecto
Vamos a generar el *setup* del proyecto para tener muy bien organizados todos nuestros archivos, imágenes y demás.

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2837%29.png)

## **Creación de carpetas y subcarpetas**
Lo primero que necesitamos es abrir nuestro editor de texto y crear una carpeta para nuestro archivo HTML, una subcarpeta para nuestro archivo CSS y otra para las imágenes que vayamos a utilizar. Recuerda que puedes llamar tu hoja de estilos como prefieras, pero siempre debe ser clara su importancia si tienes más de una.

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2836%29.png)

## **Generación del esqueleto HTML básico**
Usamos un *shortcut* para generar todo nuestro esqueleto HTML básico y empezar a modificarlo a partir de allí. Te dejo una lista con otros atajos de teclado para *Visual Studio Code* [acá](https://carontestudio.com/blog/atajos-de-teclado-en-visual-studio-code/).

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/3.png)

**Recordemos**:

* **<!DOCTYPE html>** sirve para avisar al navegador que estamos hablando de la versión HTML5.
* **head** es una etiqueta contenedora, y no es visible para el usuario, pero es necesaria para manejar dependencias.
* **body** es una etiqueta contenedora, y contiene todo lo visual con lo que el usuario puede interactuar.
* **link** es una etiqueta de contenido que sirve para referenciar ciertos assets y por medio de esta invocaremos nuestro archivo css.

# Qué son las Chrome Dev Tools
Son un conjunto de herramientas para desarrolladores web integradas en los navegadores. Prácticamente, todos los navegadores tienen Dev Tools instaladas. Nos permite ver el comportamiento de nuestro código para depurarlo y poder implementar mejoras.

Nosotros vamos a usar **Chrome Dev Tools**, pero tú puedes usar cualquiera. La idea es visualizar los cambios en HTML y CSS en tiempo real. Hay plugins que nos permiten hacer esto en el editor de texto, pero es recomendable probar el código en el navegador antes de pasarlo a nuestro VSC.

## **¿Cómo acceder a las Dev Tools?**
Lo primero es tener abierto en el navegador el proyecto que queremos trabajar. Para ello hacemos clic derecho en una parte vacía de la página y seleccionamos la opción “**inspeccionar**”.

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2838%29.png)

Una vez abiertas las Dev Tools nos encontramos con varias pestañas y opciones. Nosotros nos centraremos en la pestaña elementos para visualizar y modificar nuestro proyecto.

Y eso es todo por ahora. Si quieres conocer más sobre las Dev Tools, te dejo la [documentación de la página oficial de Google](https://developer.chrome.com/docs/devtools/) con todas las herramientas.

# Qué es el Header y cómo hacer su maqueteado
**Header** es una [etiqueta semántica](https://platzi.com/clases/1802-accesibilidad-web/26072-que-es-el-html-semantico-y-por-que-es-importante/) que le indica al navegador que el contenido de esta etiqueta es la cabecera de la página. Todas las etiquetas semánticas advierten sobre la parte de la página en la que se encuentra ese contenido.

## **Creando el header de nuestro proyecto**
Continuemos justo donde nos quedamos en nuestro archivo *index.html*, donde ya teníamos el esqueleto básico para empezar. Vamos a crear las etiquetas una dentro de otra en el orden mostrado abajo.

1. Lo primero, por supuesto, es abrir una etiqueta **header** dentro de nuestro body para delimitar toda el encabezado.
2. **nav** nos indica que hay una barra de navegación dentro. Tenemos enlaces en nuestra barra de navegación.
3. **ul** la usamos para crear una lista desordenada para colocar dentro los ítems.
4. **li** son los ítems de una lista, sin embargo, lo que buscamos son enlaces. Para ello colocamos dentro una etiqueta ancla o **a**. En nuestro proyecto tenemos cuatro: Gmail, Imágenes, un ícono y una foto.
5. **a** es una etiqueta para agregar enlaces a un texto.

Este es el resultado final que deberías tener dentro de tu etiqueta **body** hasta ahora:

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/6%281%29.png)

En tu navegador, deberías ver algo así:

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2839%29.png)

**Nota**: No olvides que puedes instalar el Live Server desde la pestaña de Extensiones dentro de *Visual Studio Code*.

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2840%29.png)

O puedes instalarlo directamente desde la página principal [aquí](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).

¡Muy bien! Más adelante aprenderemos funciones más avanzadas y a [aplicar estilos](https://platzi.com/clases/1758-html-practico/24686-agregando-estilos-al-header/).

# Agregando estilos al Header
El resultado anterior era bastante simple. ¡Es hora de aplicar diseños a la cabecera de nuestro proyecto! Pero antes, recordemos un poco algunos conceptos que vamos a utilizar.

## **Tipos de etiquetas HTML**
Existen dos tipos de etiquetas en HTML:

**Contenedoras**
* header
* nav
* section
* div

Estas etiquetas contienen a otras y ocupan un espacio.

**De contenido**
* p
* a
* li
* h1
* img

Estas etiquetas contienen elementos visibles como texto o vídeo dentro.

Saber manejar una buena arquitectura de etiquetas contenedoras nos permite acomodar las de contenido con mucha más facilidad.

## **Tipos de display**
El display es la forma en que las etiquetas contenedoras se comportan entre ellas y posicionan su contenido. Existen tres tipos:

* **layout**: El elemento expone su contenido utilizando el diseño de flujo (diseño en bloque y en línea).
* **grid**: El elemento se comporta como un elemento de bloque y establece su contenido de acuerdo con el modelo de cuadrícula.
* **flex**: El elemento se comporta como un elemento de bloque y establece su contenido de acuerdo con el modelo de flexbox.

## **Aplicando estilos**
Le aplicamos estilos al body, al header y al nav.

### **Estilos al body**
Lo primero que haremos es abrir nuestro archivo *CSS* enlazado a nuestro *html* del proyecto y resetear los espacios dentro de la etiqueta *body*.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/7.png)

Eliminamos el margin y el padding. Cambiamos el tipo de fuente y su tamaño.

En caso de que quieras aplicar estilos a todas las etiquetas del proyecto, debes hacer anteponiendo un asterisco.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/7.1.png)

En el ejemplo se elminina el padding y margin de todas las etiquetas, sin embargo, para nuestro proyecto esto no es necesario.

## **Estilos al header**
Lo primero que tenemos que contemplar es que queremos que nuestro header ocupe el 100% del ancho de la pantalla.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/7.2.png)

Ajustamos el height para que tenga 60 pixeles de alto.

## **Estilos al nav**   
Para ser específicos (ser muy específicos está bien) aplicamos los estilos a las etiquetas nav dentro de una etiqueta header.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/7.3.png)

* Usamos **display: flex** para alterar sus dimensiones y llenar el espacio disponible.
* Usamos **justify-content: flex-end para que mande el contenido a un extremo de la página. En este caso el derecho.

# Posicionar una lista en horizontal
Ya posicionaste los elementos del header de nuestro proyecto a un extremo de la pantalla, eso está genial. Ahora los colocaremos en horizontal. ¡Vamos a abrir nuestro editor!

## **Editar una lista en HTML**
Primero, vamos a modificar el 100% de nuestra etiqueta de lista no ordenada (ul). Para ello, necesitamos agregarle un identificador a esta etiqueta. Te recomendamos leer sobre la [metodología BEM](http://getbem.com/introduction/), que es una arquitectura que te permite, entre otras cosas, colocar nombres más claros a las clases y atributos.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/8.png)

**Recuerda**: las clases son genéricas, mientras que los id, únicos. Colocamos clases a elementos que se repetirán a lo largo del código, es decir, tendrán la misma clase. Los id no se pueden repetir.

### **Estilos de la lista**
Seguimos usando la metodología BEM para ser específicos al llamar a las clases y asegurarnos que no haya otra estructura parecida. Fíjate cómo está detallado.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/8.1.png)

* Invocamos la clase como: la etiqueta *header* que contenga un nav con una clase llamada *nav-right-section*
* **width**: tiene un ancho específico para que no tenga el 100% como el header
* **height**: como ya definimos una altura a su padre (header) y no puede ser mayor, la colocamos automática, para que tome la altura de su padre
* **display**: para posicionar los elementos
* **list-style**: quitamos los bullets, ya que no los necesitamos
* **justify-content**: centramos el contenido para que no se quede únicamente a la derecha
* **align-items**: alineamos los elementos para no mantenerlos en la parte de arriba
Nos quedaría de esta manera:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2843%29.png)

### **Margin**
Ahora tenemos que separarlos con el *margin*.

Especificamos el elemento que buscamos. La etiqueta *nav* que tenga una clase llamada *nav-right-section* y que contenga una etiqueta *a*.

* **margin-right**: la despegamos un poco más del extremo de la pantalla
* **color**: usamos una cifra hexadecima de color negro
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/8.2.png)

Nos quedaría de esta manera:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2844%29.png)

## **Eliminar el subrayado**
Ahora solo nos falta eliminar el subrayado que tiene el texto. Como no lo queremos en ninguna etiqueta ancla, aplicamos los cambios a la etiqueta de manera general en la parte de arriba. La llamamos directamente.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/8.3.png)

* **text-decoration**: para quitar el subrayado.
* **cursor: pointer**: para agregar la imagen de una mano al posicionar el cursor sobre el texto.

Nos quedaría de esta manera:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2845%29.png)

¡Excelente! Nuestro encabezado se ve mucho mejor, pero aún nos falta mucho. Practica estos conceptos y revísalos cuantas veces lo necesites antes de pasar a la siguiente clase.

# Manejo de íconos e imágenes en etiquetas
Continuemos con nuestro proyecto! En esta ocasión, aprenderemos a extraer la imagen de perfil directamente de la página de Google, así como el ícono de navegación.

Ten en cuenta que para este paso vamos a usar una imagen alojada en un servidor ajeno a nosotros, por lo que se tratará de una ruta absoluta. Puedes encontrar la imagen [aquí](https://static.thenounproject.com/png/756729-200.png).

## **Estilos al ícono de navegación**
Lo primero es aplicar una clase a la etiqueta en que se encuentra nuestro ícono y eliminar el texto para que no entre en conflicto con el ícono.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/9%281%29.png)

Procedemos a aplicar los estilos en nuestro archivo CSS.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/9.1.png)

* Como puedes observar, seguimos siendo muy específicos al llamar a la clase
* Insertamos la imagen como ***background*** (fondo) con el atributo ***url***. Recuerda pegar la url entre comillas
* En casos, si la imagen insertada es muy pequeña en relación con el contenedor, se repetirá para rellenar el espacio. ***background-repeat: no-repeat*** lo evita
* ***background-position: center*** para centrar nuestro ícono
* ***background-size: contain*** ajusta la imagen al tamaño del contendor, evitando el punto antes mencionado por si es muy pequeña
* Definimos su altura y ancho en 25 píxeles

Deberíamos tener este resultado:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2847%29.png)

## **Estilos a la imagen de perfil**
Para empezar este paso, debemos obtener el enlace de nuestra imagen de perfil de Google.

Vayamos a [google.com](https://www.google.com/) y hagamos clic derecho en nuestra foto.

Clic en inspeccionar.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2848%29.png)

Vemos que la consola nos posiciona justo en la url de nuestra foto.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2849%29.png)

* Copiamos ese enlace.
* Vamos a nuestro archivo HTML y cambiamos el contenido de nuestra barra de navegación Photos e insertamos una etiqueta img en su lugar.
* Pegamos el enlace en el atributo src.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/9.2.png)

**Nota**: probablemente la URL sea demasiado larga para que la veas completa en la pantalla de tu editor. Para evitar ese molesto scroll, ve a la pestaña *View* de tu editor y activa la función * Word Warp*.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2852%29.png)

Deberías poder observar tu imagen ya incrustada en tu proyecto:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2853%29.png)

## **Detalles finales**
Como te podrás dar cuenta, faltan algunos detalles para que se parezca a la página original de Google. Vamos a nuestro archivo CSS.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/9.3.png)

* Llamamos a nuestra etiqueta **img** dentro de la clase **.nav-right-section** de la etiqueta nav
* Aplicamos un ***border-radius** del ***50%*** para que sea completamente redondo
* También aplicamos un ***margin-left*** de **10** píxeles para que no esté tan pegada al ícono de menú
Como final tu header debería tener este estilo:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2854%29.png)

Adicionalmente, te dejo una lista de sitios en los que puedes encontrar íconos para tus proyectos:

* [Google Font Icons](https://fonts.google.com/icons?selected=Material+Icons)
* [Flaticon](https://www.flaticon.es/)
* [Fontawesome](https://fontawesome.com/icons?d=gallery)
* [Iconos8](https://iconos8.es/)s

¡Perfecto! Acabamos de darles los estilos al header de nuestro proyecto. Sigamos trabajando en ello.

# Maquetado de la sección principal
Llegó la hora de aplicar los estilos al cuerpo de nuestro clon de Google. Vamos llegando a la mitad de completar este ejercicio práctico. Genial, ¿verdad?

## **Creando la estructura**
En la etiqueta *main* colocamos todo el contenido que es principal en nuestro proyecto. Puedes considerarlo como todo lo que esté por debajo del *header* y antes del *footer*. Así es, el cuerpo de la página.
Generamos tres secciones: una para el logo, otra para la barra de búsqueda y el último para los botones de “buscar” y “me siento con suerte”.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2856%29.png)

Como tenemos varias secciones, es importante que las diferenciemos con clases.
* En la primera sección añadimos una clase. En este caso **main-logo**.
* Agregamos una etiqueta **img** para el logo. Después lo agregamos, no te preocupes.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/10.png)
* En la segunda sección añadimos una clase. En este caso **main-input** (por ser el contenedor principal)
* Notamos que hay tres elementos: un ícono de lupa, un input para ingresar texto, y un botón para comando por voz.
* Creamos dos etiquetas **div**. En la primera añadimos una clase. En este caso ***main-input-container*** (porque es el contenedor que lleva el input)
* Hacemos un ***span*** para colocar un ícono y le añadimos una clase. En este caso ***search-icon*** (por la lupa).
* Generamos un ***input***
* Creamos una etiqueta ***a*** para ligar el ícono de micrófono a una acción y le añadimos una clase. En este caso ***micro-icon***
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/10.2.png)
* En la tercera sección añadimos una clase. En este caso ***main-buttons***
* Necesitamos dos contenedores, por lo que creamos dos ***div***
* Añadimos una etiqueta ***button*** en cada una y escribimos el texto que lleva cada una
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/10.3.png)
Deberías tener un resultado como este:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2857%29.png)

Lo sé, lo sé. Es bastante feo. Por eso no vemos en la [siguiente clase](https://platzi.com/clases/1758-html-practico/24692-estilos-en-la-seccion-del-input/) para [aplicarle estilos a nuestro maquetado](https://platzi.com/clases/1802-accesibilidad-web/26072-que-es-el-html-semantico-y-por-que-es-importante/).

# Estilos en la sección principal
Ya [maquetamos todo el esqueleto de la sección principal](https://platzi.com/clases/1758-html-practico/24690-maquetado-de-la-seccion-principal/). Es hora de aplicar estilos a las secciones de nuestro main. Vayamos a nuestro archivo CSS y empecemos a llamar esas clases.

## **Pasos para darle estilos al main**
1. Luego de llamar a nuestra etiqueta ***main***, lo primero es separarla un poco del ***header***.
2. Añadimos un ***margin-top*** de **150** píxeles.
3. Centramos el contenido con un ***text-align: center***.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/11.1.png)

## **Pasos para poner la sección Logo de Google**
1. Llamamos la clase desde la etiqueta padre para ser específicos: ***main .main-logo***
2. Le definimos un ***width*** de 530 píxeles, que serán las dimensiones que tendrá el logo.
3. Le damos un ***margin: 0 auto***. Cuando agregamos un ancho a una etiqueta, pero aún hay espacio sobrante y queremos que se posicione de manera automática, aplicamos ***auto***. Esto hace que divida el espacio sobrante entre dos y coloca a los lados. Así nos aseguramos que se mantenga siempre en el centro
4. Le damos un ***margin-bottom*** de **35** pixeles.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/11.2.png)

Además, si queremos que el logo tenga exactamente las dimensiones que tiene el logo original de Google, podemos crear otro estillo llamando a la etiqueta ***img*** y aplicando un ***width*** de ***272px*** y un ***height*** de ***92px***.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/11.3.png)

Tendríamos un resultado como este:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2858%29.png)

# Estilos en la sección del input
Ahora, vamos a **darle estilos al input para introducir los datos de búsqueda**. Así que abre tu editor de texto y tu archivo CSS.

Al observar la barra de búsqueda de Google, nos damos cuenta de los varios asuntos que debemos resolver: una barra más ancha, dos botones dentro del input y un efecto de sombra al posicionar el cursor encima. Resolvamos todos uno por uno.

## **Cómo darle estilos al input**
* Llamamos la clase ***main. main-input***.
* Ajustamos el ***width*** a ***530*** píxeles.
* Colocamos el ***margin: 0 auto*** para que se posicione en la mitad.
* ***margin-bottom: 35px*** para que la sección del input empuje la sección de botones a la parte de abajo.

![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/12.1.png)

* Llamamos la clase que contiene a los íconos ***main .main-input-container***. Recuerda que creamos un contenedor dentro de un contenedor para manejar correctamente sus estilos.
* Ajustamos un ***width: 525px*** para que no tenga el mismo tamaño que su padre.
* Colocamos un ***border-radius: 100px*** para redondear los extremos.
* Generamos un borde de un pixel con el color del borde del input original de Google con ***border: 1px solid #dfe1e5***.
* Colocamos ***display: flex*** para que los elementos se posicionen de manera lineal.
* Colocamos ***justify-content: center*** para situarlos en el centro.
* Alineamos los elementos al centro con ***align-items: center***.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/12.2.png)

Hasta ahora podremos ver en nuestro navegador algo como esto:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2867%29.png)

## **Redimensionando el input**
Llamamos una clase ***main-input*** que llegue a la etiqueta input con ***main .main-input input***.
* Ajustamos el ***width: 450px*** y el ***height: 40px*** para que sea mas pequeño que su contendor padre.
* Quitamos el borde permanente con ***boder: none*** y el que se genera al hacer clic sobre el input con ***outline: none***.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/12.3.png)

¡Genial! Ahora nuestro diseño se parece mucho más al original. Estás haciendo un excelente trabajo.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2868%29.png)

## **Propiedades que puedes usar para distintos estilos de bordes**
**Adicional, te dejo una lista de propiedades que puedes usar para distintos estilos de bordes**.
La ***border-stylepropiedad*** especifica qué tipo de borde mostrar.
Se permiten los siguientes valores:

* ***dotted*** - Define un borde punteado
* ***dashed*** - Define un borde punteado
* ***solid*** - Define un borde sólido
* ***double*** - Define un doble borde
* ***groove-*** Define un borde acanalado en 3D. El efecto depende del valor del color del borde.
* ***ridge-*** Define un borde ondulado en 3D. El efecto depende del valor del color del borde.
* ***inset-*** Define un borde insertado en 3D. El efecto depende del valor del color del borde.
* ***outset-*** Define un borde de inicio 3D. El efecto depende del valor del color del borde.
* ***none*** - Define sin borde
* ***hidden*** - Define un borde oculto
* La ***border-stylepropiedad*** puede tener de uno a cuatro valores (para el borde superior, el borde derecho, el borde inferior y el borde izquierdo).

# Íconos y manejo de background hover
Continuemos añadiendo estilos a nuestro input. Aún tenemos que incrustar y posicionar los íconos de lupa y micrófono, además del bonito efecto de sombra al poner el cursor encima. Esto no se va a lograr solo, así que vamos a abrir nuestro archivo CSS justo donde nos quedamos.

## **Cómo añadir el efecto hover**
1. Llamamos la etiqueta contenedora del ***input*** con el pseudo-elemento ***hover***. Es decir, los diseños con hover que apliquemos solo se mostrarán cuando coloquemos el cursor encima del elemento.
2. Con ***box-shadow: 0 1px 6px 0 #20212447*** agregamos una sombra paralela con un color en tono oscuro.
3. Con ***border-color: #dfele500*** añadimos un borde más oscuro, es decir, resalta más como el input original.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/13.1.png)

## **Cómo agregar íconos**
Vamos a agregar dos íconos: el de lupa y el de micrófono.

### **Pasos para agregar el ícono de lupa**
1. Primero, llamamos la clase ***.search-icon*** desde nuestra clase ***.main input***.
2. Añadimos un ***background-image*** e insertamos la ***url*** del ícono entre comillas. Te dejo el enlace: “https://cdn0.iconfinder.com/data/icons/google-material-design-3-0/48/ic_search_48px-512.png”.
3. ***background-repeat: no-repeat*** para evitar que el navegador repita la imagen por rellenar espacio.
4. ***background-position: center*** para centrarlo.
5. ***background-size: contain*** para que tome el tamaño del contenedor padre.
6. Añadimos un ***width: 18px*** y un ***height: 18px*** para redimensionar el ícono.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/13.2.png)

### **Pasos para agregar el ícono de micrófono**
1. Llamamos la clase **.micro-icon** desde nuestra clase .main input.
Copiamos el código de arriba y cambiamos la url del ícono de micrófono. 2. Te dejo el enlace: “https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Google_mic.svg/726px-Google_mic.svg.png”.
3. Añadimos ***cursor: pointer*** para que el cursor adopte la forma de la manita al colocarlo sobre el ícono.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/13.3.png)

Deberíamos tener renderizado en nuestro navegador algo como esto:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2878%29.png)

¿Ya la ves muy parecida? Apuesto a que sí. Pero no hemos terminado, por lo que vamos a centrarnos en los botones de abajo en la siguiente clase.

# Estilos en los botones
¡Esta es la última sección de nuestro main! Vamos a generar nuestros estilos para que no se note la diferencia entre los nuestros y los de Google.

## **Cómo aplicar los estilos de los botones**
1. Llamamos la clase que contiene los botones dentro de la etiqueta ***main***.
2. Ajustamos el ***width: 530px***.
3. Ajustamos el ***margin: 0 auto*** para que se posicione siempre en el centro.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/14.1.png)

## **Definir la posición de los botones**
1. Llamamos la clase que contiene los botones que contenga una etiqueta ***div*** con ***main .main-buttons div***.
2. Ajustamos el ***display*** en ***inline-block***. Esto es porque por defecto el navegador le asigna a las cajas ***display: block***, lo que hace que esté una encima de otra. Al usar ***inline-block*** las ponemos una a lado de otra. Por esto le asignamos la misma propiedad a las dos cajas.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/14.2.png)

## **Pasos para darle diseño de caja a los botones**
1. Llamamos la clase que contiene los botones que contenga la etiqueta ***button*** con ***main .main-buttons button***.
2. Le damos una altura con ***height: 36px***.
3. Ajustamos el color de fondo con ***background-color: #f2f2f2***.
4. Cambiamos el borde para que no se desplaze al colocar el cursor encima con ***border: 1px solid #f2f2f2***.
5. Cambiamos el tamaño de fuente con ***font-size: 14px***.
6. Cambiamos el color de la fuente con ***color: #5f6368***.
7. Redondeamos los bordes con ***border-radius: 5px***.
8. Añadimos espacio interno a los lados con ***padding: 0 15px***.
9. Añadimos una separación entre los botones con ***margin-right: 15px***.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/14.3.png)

## **Cómo poner el efecto hover en los botones**
Ahora necesitamos que al pasar el cursor sobre los botones, cambie el color del texto y se cree una sombra alrededor de la caja. Para ello:

1. Llamamos la clase que contiene los botones con el pseudo-elemento ***hover***. Así: ***main .main-buttons button:hover***.
2. Generamos un borde sólido con ***border: 1px solid #c6c6c6***.
3. Generamos una sombra con ***box-shadow: 0 1px 1px rgba(0, 0, 0, 0.1)***.
4. Cambiamos el color del texto con ***color: #222***.
5. Añadimos un color de fondo con ***background-color: #f8f8f8***.
6. Agregamos ***cursor: pointer*** para que el ícono del cursor cambie a una manita al posicionarlo sobre los botones.

En nuestro navegador deberíamos tener un resultado como este:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2883%29.png)

# Maquetado del Footer
Ya estamos en el final de nuestro proyecto clon de Google. ¡Hasta ahora ha sido bastante divertido! ¿Verdad? Justo ahora vamos a maquetar la estructura del pie de página o footer. Los estilos los aplicaremos más adelante. ¡Directo a nuestro archivo HTML!

## **Pasos para poner la estructura del footer**
1. Primero abrimos nuestra etiqueta ***footer***. Necesitamos seccionarla en dos partes: contenedores izquierdos y derechos.
2. Creamos dos listas no ordenadas ***(ul)*** con cuatro y tres elementos ***(li)*** respectivamente.
3. Creamos una etiqueta ancla ***(a)*** a cada elemento ***(li)*** de nuestra lista.
4. Asignamos la clase ***footer-left*** a la primera lista y ***footer-right*** a la segunda.
5. Ahora solo agregamos el texto dentro de cada una de los elementos ***(li)*** de las listas.
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/15.png)
**Tip:** puedes usar *emmet* para abreviar la creación de las listas. De esta manera: ***<ul2>li4>a>***.

Deberíamos tener una imagen así en nuestro navegador:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2884%29.png)
Por ahora, es funcional. ¡En la siguiente clase la dejaremos mucho más bonita!

# Estilos en Footer
Bienvenida y bienvenido a la recta final de nuestro proyecto! Ya sabes cómo [maquetar la estructura del footer](https://platzi.com/clases/1758-html-practico/24695-maquetado-del-footer/). Ahora, aplicaremos los estilos. Vamos directo a nuestro archivo CSS.

## **Etiqueta footer**
1. Llamamos la etiqueta *footer*.
2. Le asignamos el ***width:*** **100%** para que ocupe todo el ancho de la página y un ***height:*** **50px**.
3. Para asegurarnos que el *footer* siempre esté al final de la página y no se mueva, le damos ***position: absolute***.
4. Además, quitamos el espacio de abajo con ***bottom: 0***.
5. Usamos ***display: grid*** para generar la cuadrícula en que estará el contenido de nuestro proyecto. La propiedad grid-template-colums: 1fr 1fr nos permite dividir el footer en dos fracciones.
6. Alineamos los elementos con ***align-items: center***.
7. Cambiamos el tamaño de fuente con ***font-size: 13px***.
8. Le damos un color de fondo con ***background-color: #f2f2f2***.
9. Añadimos un borde superior con ***border-top: 1px solid #e4e4e4***.

## **Etiqueta ul**
1. Llamamos la etiqueta ul desde el *footer*.
2. Le damos un ***margin: 10px*** para que el contenido no esté tan pegado al contenedor padre.
3. Le quitamos los *bullets* con ***list-style: none***.
4. Posicionamos el contenido en horizontal con ***display: flex***.
5. Quitamos el espaciado interno izquierdo con ***padding-left: 0***.
## **Contenedor izquierdo**
1. Llamamos la clase *footer-left* desde nuestra etiqueta *footer* con *footer .footer-left*.
2. Movemos los elementos a la izquierda con ***justify-self: left***.
## **Contenedor derecho**
1. Llamamos la clase *footer-left* desde nuestra etiqueta *footer* con *footer .footer-right*.
2. Movemos los elementos a la derecha con ***justify-self: right***.
## **Agregar estilos a los elementos**
1. Llamamos a las etiquetas ancla dentro de los elementos li de las listas no ordenadas de nuestra etiqueta *footer* con *footer ul li a*
2. Agregamos un ***margin: 10px*** para separar los elementos entre sí.
3. Cambiamos su color con ***color: #5f6368***.

Nuestro proyecto final se debería ver así:
![](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/image%2885%29.png)

¡Y listo! Hemos terminado de trabajar en nuestro clon de Google. ¡Muy bien por ti! Hemos aplicado muchos de los conceptos aprendidos en el Curso Definitivo de HTML y CSS. Pero esto no termina aquí.

## **Te proponemos un reto**
Aprendimos a modelar paso a paso un header, main y footer. Ahora te toca a ti clonar otra icónica página usada por los estudiantes, ¡Wikipedia!

Te dejo los enlaces de los íconos de pie de página para ahorrarte un poco de tiempo:

* [Commons](https://upload.wikimedia.org/wikipedia/commons/4/4a/Commons-logo.svg)
* [Wikivoyage](https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/Wikivoyage-Logo-v3-icon.svg/1024px-Wikivoyage-Logo-v3-icon.svg.png)
* [Wiktionary](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Wiktfavicon_en.svg/1024px-Wiktfavicon_en.svg.png)
* [Wikibooks](https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Wikibooks-logo.svg/1200px-Wikibooks-logo.svg.png)
* [Wikinews](https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Wikinews-logo.svg/1200px-Wikinews-logo.svg.png)
* [Wikidata](https://upload.wikimedia.org/wikipedia/commons/thumb/6/67/Notification-icon-Wikidata-logo.svg/1200px-Notification-icon-Wikidata-logo.svg.png)
* [Wikiversity](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Wikiversity_logo_2017.svg/1200px-Wikiversity_logo_2017.svg.png)
* [Wikiquote](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Notification-icon-Wikiquote.svg/1200px-Notification-icon-Wikiquote.svg.png)
* [Mediawiki](https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Notification-icon-MediaWiki-logo.svg/1200px-Notification-icon-MediaWiki-logo.svg.png)
* [Wikisource](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Wikisource-logo.svg/1200px-Wikisource-logo.svg.png)
* [Wikispecies](https://upload.wikimedia.org/wikipedia/commons/thumb/d/df/Wikispecies-logo.svg/1200px-Wikispecies-logo.svg.png)
* [Metawiki](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Meta-Wiki_Proposed_logo.svg/1200px-Meta-Wiki_Proposed_logo.svg.png)