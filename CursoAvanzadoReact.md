# Instalar APP

https://github.com/betoquiroga/react-desde-cero/blob/master/src/components/Pages/Course.jsx
https://v5.reactrouter.com/web/example/no-match

https://test.negocioleonisa.com/wps/myportal/$project/CR-pago-con-tarjeta-credito/costa-rica/servicios/pagos/pago-con-tarjeta

https://validatejs.org/
https://reactrouter.com/docs/en/v6/examples/multi-app

# Qué es React

Si React es tu primera librería de JavaScript, debes saber que muchas de las librerías están basadas en componentes, pero… ¿Realmente qué significa un “componente”? Si ya has tomado el Curso Básico de Web Components con JavaScript pues el concepto es prácticamente el mismo, pero aplicados a React. Pero si es la primera vez que escuchas sobre componentes…

- ☝ Básicamente un componente es un pedacito de tu página web, es decir, puede ser una sección específica de tu página web, o puede ser algún elemento que se repita múltiples veces en la misma. Lo importante a tener en cuenta es que, un componente es una parte específica de tu página, es algo que cumple una acción simple 👀.
- ¿El header de mi página puede ser un componente? ¡Sí!
- ¿El sidebar puede ser un componente? ¡Por su puesto!
- Y si tengo varios articulos en mi página… ¿Puedo convertirlos a componentes? ¡Por su pollo! 😄
- Recuerda que todo puede ser un componente, y esto nos permite modularizar nuestro código. Es decir, podemos dividir y “aislar” cada parte de nuestra página. Si por alguna razón necesitaramos actualizar nuestro header (por ejemplo), bastaría con entrar al componente header modificar una pequeña línea y listo! Ya no tendríamos que buscar el header dentro de tooooodo nuestro HTML UwU.
- 👀 Otra ventaja de los componentes es que son reutilizables, es decir, puedes usarlos cuantas veces quieras. Por ejemplo, si tuvieras un sitio web sobre blogs, ya sabes que muchos blogs suelen tener una imagen, un título y una descripción. Entonces podríamos crear un componente con la estructura de nuestro blogpost y únicamente mandarle la información que necesitemos por cada blogpost y cada uno se crearía automáticamente!!

[<img src="./images/React-components-blog-image.jpg" width="400"/>](./images/React-components-blog-image.jpg)

## Características básicas de react

- Es un sistema de plantillas para gestionar las vistas que utiliza un lenguaje de marcado llamado JSX, similar a HTML

- Está basado en componentes: Toda la UI se divide en elementos más pequeños llamados componentes, en react, todo es un componente.

- Es declarativo: expresa la lógica de un cálculo sin describir su flujo de control, es un estilo de programación en el que el que se define “qué” es la solución sin importar cómo se llegó a ella.

- División de código utilizan react lazy

- Compartir la logica con entre diferentes componentes utilizando las técnica (componentes de orden superior, render props, custom hooks)

- Espia el código es decir cuando hay algun cambio compila la app y recarga la pagina para ver los cambios.

- Como react utiliza JSX se utiliza className para acceder a un estilo.

## Lecturas recomendadas

- Curso de React.js
  https://platzi.com/cursos/react/

- Curso de Git y GitHub Profesional | Platzi
  https://platzi.com/cursos/git-github/

- Curso de Desarrollo Web Online
  https://platzi.com/cursos/html5-css3/

- Introducción a Terminal y Línea de Comandos
  https://platzi.com/cursos/terminal/

- Fundamentos de JavaScript
  https://platzi.com/cursos/fundamentos-javascript/

# Instalación con Create React App

Opcion 1 (Recomendada)
Crea una carpeta con el nombre que definas y toda la configuración de React que se muestra en la clase.

1. $ npx create-react-app mi-proyecto-react
2. $ npm start -> localhost:3000
3. A partir de aquí nos quedaría eliminar logo.svg, reportWebVitals.js, setupTest.js, App.css y App.test.js de la carpeta SRC.
4. En Index.js eliminamos la línea 5 y de la 14 a la 17
5. En App.js la línea 1 , la linea 2 y de la linea 6 a la 21. Dentro del return podemos escribir un <div>Hola</div>, y listo
6. env-cmd (https://www.npmjs.com/package/env-cmd)
7. Variables de entorno (https://www.codingdeft.com/posts/react-environment-variables/)

# Guia de estilos

- AIRBNB: https://github.com/airbnb/javascript/tree/master/react
- pagar.me: https://github.com/pagarme/react-style-guide
- ghengeveld (Chromatic): https://github.com/ghengeveld/react-redux-styleguide
- Khan (Khan Academy): https://github.com/Khan/style-guides/blob/master/style/react.md#use-flow-instead-of-proptypes
- Daniel Junch (CSS Tricks): https://css-tricks.com/react-code-style-guide/

# Que es JSX

Aquí una breve explicación de lo que es JSX que encontré por ahí:
JSX es una extensión de JavaScript creada por Facebook para el uso con su librería React. Sirve de preprocesador (como Sass o Stylus a CSS) y transforma el código a JavaScript. De primeras te puede parecer que estás mezclando código HTML dentro de tus ficheros JavaScript, pero nada más lejos de la realidad.

# Componentes

- Sintaxis -> La primera letra en mayuscula para identificar que es un componente
- Un componente puede retornar varios elementos con la sintaxis de JSX
- Se usa llaves para acceder a las variables enviadas al componente {parameter}
- Los componentes son invisibles para HTML pero son visibles para react para poder renderizar, lo que renderiza son los elementos del componente (div, p, img etc...)
- Se utiliza la sintaxis JSX que parece HTML estamos escribiendo React.createElement('div', {}) y babel se encargar de transformar en HTML
- Elementos de JSX son div, p, img y etiquetas HTML son div, p, img, aunque se parecen son diferentes porque los elementos utilizan la sintaxis JSX
- La magia de utilizar los componentes en react son las propiedades en la etiquetas o elementos.
- En los componentes se pueden enviar propiedades ejemplo: <App parameter="Saludo"> y en archivo JS donde esta definido el componente se recibe de la siguiente manera: function App(props){ <h1>{props.parameter}</h1> }

# Eventos

☝ Por si no entendiste bien por qué a veces enviamos arrow functions y por qué otras veces no, aquí te lo explico:

- Cualquier evento recibe sí o sí una función, es decir, debemos mandarle sí o sí una función para que React internamente pueda ejecutarla en cuanto dicho evento ocurre.

- El asunto, es que tiene que ser sí o sí una función que React pueda ejecutar, por eso no podemos mandar directamente un console.log() ni un alert(), porque aunque ambos son funciones, nosotros estamos ejecutándolas directamente al ponerles los paréntesis, pero nosotros no debemos ejecutarlas, nosotros solo debemos mandarlas y ya React se encargará de ejecutarlas.

- Es por eso que mandamos arrow functions, porque estas son funciones que React puede ejecutar cuando quiera, y pues dentro de esas arrow functions está el código que queremos ejecutar cuando el evento suceda.

- onClick={() => alert("React sí puede ejecutar esta arrow function cada que le de la gana OwO")}

- Sin embargo, recordando que los eventos reciben funciones, yo puedo crear una variable que dentro guarde una función, por ejemplo:

const adentroTengoUnaFuncion = () => {
console.log("Hola");
console.log("Soy una función que está siendo guardada dentro de una variable UwU");
}

- Yo puedo ejecutar esta función sin problemas de esta forma adentroTengoUnaFuncion(), pero también puedo mandarsela a React para que él lo ejecute cuando quiera (en este caso, cuando el evento suceda):

onClick={adentroTengoUnaFuncion}

- Nota como aquí mandamos la función sin paréntesis, esto es porque en el momento en el que le ponemos paréntesis seríamos nosotros quienes ejecutan la función, pero recuerda que nosotros no debemos ejecutar la función, sino React es quien tiene que ejecutarla. ¿Por qué? Pues porque si la ejecutamos nosotros, esta se va a ejecutar justo en el momento que esa línea de código sea leída por nuestra computadora, y nosotros no queremos eso, nosotros queremos que nuestra función se ejecute únicamente cuando el evento suceda, por eso la mandamos sin paréntesis, para que React pueda ejecutarla cuando dicho evento ocurra 😄

- Peeeeeero, podemos hacer algo genial (y puede ponerse complicado), no veo razón para hacer esto, pero te lo explico por alimentar tu curiosidad jaja:
- Sí podemos ejecutar nosotros la función 👀… Yo sé, esto es totalmente lo contrario a lo que te acabo de decir, pero checa esto 👇
- Nosotros sí podemos hacer esto:
  onClick={adentroTengoUnaFuncion()}

- Solamente sí nuestra función está así:
  const adentroTengoUnaFuncion = () => {
  return () => {
  console.log("Hola");
  console.log("Soy una función que está siendo guardada dentro de una variable UwU");
  }
  }

- Wait… what? Es simple 👀 Mi función adentroTengoUnaFuncion está retornando otra función, eso significa que, en el momento que mi código se ejecute, mi función adentroTengoUnaFuncion también se va a ejecutar inmediatamente, pero como esta función está retornando otra función, al final mi evento onClick acabará recibiendo la función que necesita para funcionar!!! OwO
  .
  ¿Por qué haríamos esto? Seguramente tenga algún caso de uso, pero también es interesante saber que se pueden hacer este tipo de cosas UwU

# Lecturas recomendadas

Organización de archivos en el frontend
https://platzi.com/clases/2239-frameworks-javascript/36174-organizacion-de-archivos-en-el-frontend/

Peacock - Visual Studio Marketplace
https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf
GitHub - platzi/curso-intro-react at 1ed02fc76fb2b5bb4d4f00b6aeb9176380887e38
https://github.com/platzi/curso-intro-react/tree/1ed02fc76fb2b5bb4d4f00b6aeb9176380887e38

# stateful vs stateless

Luego se habló sobre stateful vs stateless y sobre como ordenar ya nuestro código del componente, dejo acá unas lecturas para interiorizar sobre el tema ya que no recuerdo haber hablado sobre el tema anteriormente:

https://programmingwithmosh.com/javascript/stateful-stateless-components-react/
https://medium.com/@cgcrutch18/stateful-vs-stateless-react-components-13f647f7fc4
https://dev.to/jessadaggs/stateful-and-stateless-components-in-react-1lo1
https://www.cronj.com/blog/learn-stateful-and-stateless-components-in-reactjs/

## Stateful

Los componentes stateful son los componentes que guardan y manejan estados. Por lo que hemos aprendido hasta ahora sería los que usan alguna variable que usa React.useState

## stateless

Mientras los componentes stateless son los componentes que solo presentan información. Es decir son los componentes que reciben props o simplemente muestran algun contenido
Fuente: https://programmingwithmosh.com/javascript/stateful-stateless-components-react/

# API de almacenamiento web

- localStorage: guarda la información en memoria incluso cuando el navegador se cierre y se reabra.

- sesionStorage: guarda la informacion en memoria mientras dure la sesión de la página.

- Storage.setItem() -> cuando recibe un nombre y valor, lo almacena o actualiza si ya existe.

Ejemplo:

```js
storage.setItem(nombre, valor);
```

- Storage.getItem() -> Devuelve el valor cuando le pasamos el nombre.

Ejemplo

```js
let userBackground = storage.getItem(userBackground);
// #000000
```

- Storage.removeItem() -> Elimina el valor almacenado cuando le pasamos el nombre:

Ejemplo

```js
let userBackground = storage.removeItem(userBackground);
// Queda el valor por defecto en caso que exista, por lo ejemplo un background blanco.
```

Storage.length -> Devuelve un entero que indica el número de elementos guardados en el objeto ** Storage.**

Ejemplo

```js
function userSettings() {
localStorage.setItem('userBackground', '#000000');
localStorage.setItem('font', comic sans');
localStorage.setItem('fontSize', '18');

localStorage.length;

// 3
}
```

storage.clear() -> borra todos los registros guardados en local.

## Local storage VS Session Storage🥳

- Me pareció muy curioso compartir estas dos interesantes herramientas que llamaron mi atención. 🤔
- La principal diferencia entre estas dos, es que el Local Storage no tiene una fecha de expiración y está disponible en la web que estamos desarrollando de forma global. 💯 Lo interesante del Session Storage es que solo esta disponible ventana actual en la que estamos navegando y solo son accesibles para el dominio actual. 🔐

## Manejo de errores

- Using the Effect Hook – React
  https://reactjs.org/docs/hooks-effect.html

- GitHub - platzi/curso-intro-react at 2cff4d4d612a8d4eab2b7e3e1bf31add74fa9e45
  https://github.com/platzi/curso-intro-react/tree/2cff4d4d612a8d4eab2b7e3e1bf31add74fa9e45

- 5 estados clave para crear interfaces coherentes
  https://platzi.com/blog/ui-stack/

- useEffect vs. useLayoutEffect - Platzi
  https://platzi.com/blog/useeffect-uselayouteffect/

### Buenas Practicas

- Envolver las acciones en funciones en arrobas functions ej: onClick={() => alert("Hola mundo !!!")}
  Ract no puede renderidar varias etiquetas en un mismo componente sino que tenemos qye tener una etiqueta de envuelva todos los elementos o enviar un array
  se debe tener cuidado con los estado por que pueden hacer mucho re-render y esto afecta el browser y el rendimiento de la APP

- Evitar lo export por default ya que se pueden cambiar los nombres a los exports
  export defult AppUI -> Mala practica
  export {AppUi} -> Buena practica

- Crear los propios react-Hook deben empezar por use ejemplo:

```js
function useName() {}
```

# Reto: loading skeleton
Muchas aplicaciones se quedan en blanco mientras cargan su contenido. Otras muestran algún mensaje de “cargando” y luego sí renderizan todo el contenido de la aplicación.

Pero para ofrecerle una mejor experiencia a nuestros usuarios (UX) es mejor renderizar todo el contenido posible, incluso si no ha terminado de cargar alguna parte de la aplicación. En TODO Machine, por ejemplo, podemos mostrar varios componentes desde el principio aunque no hayamos terminado de cargar la lista de TODOs.

Pero un párrafo que diga “cargando” definitivamente NO es la mejor forma de comunicarle a los usuarios que estamos cargando (el mensaje es claro, pero podríamos buscar una solución más… estética).

Existen muchas posibles soluciones, desde animaciones sencillas (como 3 puntitos intercalando diferentes niveles de opacidad) hasta loading skeletons (esqueletos de carga). Incluso existen herramientas interactivas como Create React Content Loader para agilizar estos desarrollos.

El reto de esta clase es que maquetes cualquiera de estas soluciones y nos la muestres en la sección de comentarios. En esta lectura te mostraré mi solución, pero te recomiendo que no la veas hasta intentar tu propia solución.

💡 Te recomiendo esta lectura: 5 estados clave para crear interfaces coherentes

## Tu propio loading skeleton en React
Lo primero que vamos a hacer es crear 3 nuevos componentes para trabajarlos independientemente: TodosError, TodosLoading y EmptyTodos.

[<img src="./images/skeleton.webp" width="400"/>](./images/skeleton.webp)

Ya que tenemos estos 3 componentes, ahora vamos a llamarlos desde el componente AppUI para conectarlos con la aplicación.

[<img src="./images/skeleton2.webp" width="400"/>](./images/skeleton2.webp)
¡Muy bien! Ahora sí podemos concentrarnos mucho mejor para trabajar el estado de carga de TODOS dentro del componente TodosLoading.

Para empezar, voy a crear y conectar un archivo TodosLoading.css para definir los estilos de mi esqueleto:

[<img src="./images/skeleton3.webp" width="400"/>](./images/skeleton3.webp)

Llegó el momento más importante: maquetar.

Debemos definir qué elementos necesitamos para el esqueleto y luego les daremos estilos con CSS. Como la idea es replicar la estructura de un TODO, vamos a necesitar una cajita para el contenedor del TODO, una cajita para el ícono de completar, otra cajita para el ícono de borrar y una última cajita para el texto.

💡 Le digo a cada elemento “cajita” porque el objetivo de los esqueletos de carga no es replicar todos estos elementos, sino que cada uno será un elemento “fantasma”. Deben ser lo suficientemente parecidos a los TODOs reales para que los usuarios entiendan que estos elementos están relacionados con los TODOs, pero lo suficientemente abstractos y grisáceos para que se entienda que aún los estamos cargando.

[<img src="./images/skeleton4.webp" width="400"/>](./images/skeleton4.webp)

¡Y ahora debemos crear los estilos!

Primero vamos a definir los tamaños y posiciones de cada elemento (tal cual copiando y pegando los estilos del TodoItem.css, pero cambiando los nombres de las clases y descartando las propiedades innecesarias):

[<img src="./images/skeleton5.webp" width="400"/>](./images/skeleton5.webp)

Ahora vamos a todas las cajitas (menos la del texto) para darles un color de fondo con gradiente:

[<img src="./images/skeleton6.webp" width="400"/>](./images/skeleton6.webp)

Luego le configuraremos un tamaño de fondo lo suficientemente grande como para que pueda darla vuelta sin dejar espacios vacíos (400% es más que suficiente):

[<img src="./images/skeleton7.webp" width="400"/>](./images/skeleton7.webp)

Y finalmente le daremos una animación que cambie la posición del fondo al principio, a la mitad y al final (te recomiendo darle al menos 3 segundos de duración para que tu animación no se vea atropellada, sino por el contrario con un efecto suave e hipnotizante):

[<img src="./images/skeleton8.webp" width="400"/>](./images/skeleton8.webp)

💡 Puedes ir a useLocalStorage.js y cambiar el tiempo que tardamos en llamar a nuestro efecto con la función setTimeout para poder visualizar tu esqueleto de carga correctamente.

👉 Aquí puedes encontrar el repositorio de este reto: Clase bonus: loading skeleton

- https://github.com/platzi/curso-intro-react/tree/a0b647c563f0a5df45769931fda292e332af43a5 
- https://github.com/jorgemacper/random-user.git 
- https://www.youtube.com/watch?v=cg_tmJBisp8&list=PL4cUxeGkcC9i6bZhMuAzQpC6YgLmB4k4-


# Reto: icon component
Por ahora los íconos de nuestra aplicación solo son etiquetas span con algún carácter representando la acción que conseguirán los usuarios al presionarlos. No está mal, funciona. Pero queremos reutilizar estos íconos fuera del componente TodoItem.

Por eso el reto de esta clase es que crees tu propio componente TodoIcon, las reglas son:

Te debe permitir elegir qué tipo de ícono quieres (marcar como completado, borrar o incluso algunos más que podamos necesitar).
Cada ícono también debe poder tener estados (cambios al color o alguna otra propiedad del ícono para darle feedback a los usuarios de que realizaron alguna acción, como dar click o pasar el mouse por encima).
Es válido que uses varios componentes en vez de solo uno para definir la lógica de tus íconos.

Haz tu mayor esfuerzo por completar el reto y publicar tu solución en los comentarios. Luego de eso puedes ver mi propuesta de solución.

Solución:
La ventaja de usar letras para simular el comportamiento de nuestros íconos es que podemos cambiarles el color con CSS extremadamente fácil. La desventaja es que no son muy “estéticas”.

La ventaja de usar imágenes es que podemos tener la versión más estética de cada ícono. La desventaja es que no podemos cambiarles el color con CSS, necesitamos a fuerzas otra imagen con el nuevo color.

Afortunadamente, tenemos una tercera alternativa con las ventajas de ambos mundos: svg.

Las imágenes en SVG son diseñadas por la persona encargada del diseño, pero al exportarlas en formato SVG tenemos la imagen “maquetada” con etiquetas HTML que podemos modificar con CSS.

Su única desventaja es la complejidad de su implementación. Pero somos hijas e hijos de Platzi, no vinimos para lo fácil, sino para nunca parar de aprender. ¡Así que a la carga!

Empecemos creando un componente TodoIcon en su propia carpeta y con sus respectivos archivos de JavaScript y CSS:

[<img src="./images/reto.png" width="400"/>](./images/reto.png)

Ahora debemos pensar qué propiedades pueden necesitar nuestros íconos, yo elegí las siguientes:

- type: para seleccionar qué ícono svg vamos a mostrar.
- color: para seleccionar el color de nuestro ícono svg, por defecto será gray.
- onClick: para invocar alguna función cuando le demos click al contenedor de nuestro ícono.

Recuerda que los usuarios no siempre dan click o presionan la pantalla de sus celulares con completa precisión, por lo que es muy buena idea crear un contenedor invisible alrededor de nuestros íconos.

💡 Material Design tiene una excelente guía sobre diseño de íconos, te recomiendo estudiarla para descubrir más detalles interesantes.

Yo decidí utilizar una etiqueta span para el contenedor de los íconos. Así que este span recibirá la propiedad onClick, mientras que el SVG (que ya en un momento vamos a crear) recibirá las otras dos propiedades.

También utilizaré la prop type para darle clases personalizadas a cada contenedor de mis íconos.

[<img src="./images/reto1.png" width="400"/>](./images/reto1.png)

¡Contenedor listo!

Ahora debemos encargarnos de los SVG. Está perfecto si quieres hacerlos a mano con herramientas como Figma o Illustrator.

En mi caso simplemente usaré alguna herramienta de íconos como Flaticon y descargaré los íconos que vea conveniente en la misma carpeta TodoIcon. De esta forma podremos importarlos como componentes de React gracias a la configuración por defecto que nos ofrece Create React App.

Te recomiendo importar tus íconos SVG desde tus componentes en React de esta forma:

[<img src="./images/reto2.png" width="400"/>](./images/reto2.png)

Que luego podremos llamar así:

[<img src="./images/reto3.png" width="400"/>](./images/reto3.png)

Yo usaré dos íconos (uno de hecho y otro de delete):

[<img src="./images/reto4.png" width="400"/>](./images/reto4.png)

Lo que nos falta es determinar cuál SVG mostrar dependiendo de la propiedad type que nos envíe el componente que llame a nuestro TodoIcon.

Hay muchas formas de lograr esto, mi forma favorita es crear un objeto con todos los íconos que nuestro componente puede mostrar:

[<img src="./images/reto5.png" width="400"/>](./images/reto5.png)

Y luego dentro de nuestro componente TodoIconllamamos al SVG que esté dentro de la propiedad con el mismo nombre que recibamos en la prop type:

[<img src="./images/reto6.png" width="400"/>](./images/reto6.png)

Así automáticamente mostraremos el icono CheckSVG cuando la prop type tenga el valor check o el icono DeleteSVG cuando tenga el valor delete.

Aunque hay un superpoder más que podemos usar. Si envolvemos nuestros íconos dentro de funciones vamos a poder enviarles propiedades que cambien su presentación o comportamiento.

En este caso voy a usar esta funcionalidad para enviarle la prop color a nuestros SVG (y así cambiarles su color cuando los componentes que llamen a nuestros íconos así lo requieran).

[<img src="./images/reto7.png" width="400"/>](./images/reto7.png)

El último paso para que nuestros componentes funcionen sería agregar nuestro código CSS al nuevo archivo de estilos TodoIcon.css (y de paso borrar el código que ya no necesitamos en TodoItem.css):

[<img src="./images/reto8.png" width="400"/>](./images/reto8.png)

¡Excelente! Nuestro componente TodoIcon ya funciona y podemos llamarlo desde el componente TodoItem para darle sus íconos mucho mejor configurados.

Aunque antes quiero hacer un poco más de composición.

Cada vez que llamamos a nuestro ícono debemos enviar varias props. Pero ¿qué tal si crearamos un componente que envíe todas esas props por nosotros?

Lo que voy a hacer es crear dos nuevos componentes, CompleteIcon y DeleteIcon. Cada uno llamará al componente TodoIcon con sus respectivas props necesarias. Y luego podremos llamar mucho más fácil a estos dos nuevos componentes donde los necesitemos.

[<img src="./images/reto9.png" width="400"/>](./images/reto9.png)

Y estos componentes ahora sí los llamaremos desde TodoItem:

[<img src="./images/reto10.png" width="400"/>](./images/reto10.png)

Así seguiría construyendo mi componente TodoIcon con todos los íconos que vaya requiriendo nuestra aplicación TODO Machine.

¡Te espero en la siguiente clase para desplegar nuestra aplicación a GitHub Pages!

👉 Aquí puedes encontrar el repositorio de este reto: Clase bonus 2: TodoIcon

