# Prompts — TP 1

El registro del proceso, en orden. Tres prompts en una sola conversación de Gemini Canvas. El artefacto quedó terminado en el tercero.

---

## 1 — Prompt inicial


```
Crear un pagina html que imite la pantalla de creacion de un jugador del juego Pro Evolution
Soccer 2010 en PlayStation 2.



Estructura:

- en <head> agrega un <title> con el título "PES 2010 - Creación de Jugador - PS2" y en la 
esquina superior derecha la consola "PlayStation 2" y tambien los estilos de css

- agregar un header con el mismo titulo  "PES 2010 - Creación de Jugador"  y en la esquina 
superior derecha la consola "PlayStation 2"

- agrega secciones de div para incluir 3 form horizontales para cargar Nombre , Edad y Altura.

- agrega 2 <button> abajo, para los botones Crear Jugador y Cancelar.

- agrega una seccion con <button> con la misma disposicion que un Joystick de Playstation 2,
con las flechas de direciones, y cuadrado, circulo, triaunglo y X.

- Agrega una seccion de <fotter> con las leyendas de lo que hace cada boton



Estilo:

- Utiliza estilos de letra y colores que usaba el juego original, asi como los estilos para el
mando y menciones a Playstation 2. Agrega iconos y sonidos de ser posibles, con referencias al
juego original, Sony o Konami.



Comportamiento:

-  La interfaz debe ser incomoda para el usuario por lo cual los form no pueden completarse
con el teclado ni haciendo clic directo sobre el form o los botones sino haciendo clic en los
iconos del joystick debajo para manejarlo. Con X se selecciona la casilla o boton, con circulo
se vuelve hacia atras y se posiciona en el boton de cancelar, con triangulo se vuelve hacia
atras, con cuadrado se borra la ultima letra de la casilla del nombre. Con las flechas se
debe navegar entre botones y casillas.

- para agregar o cambiar el nombre del jugador se debe seleccionar la casilla para completar
el nombre y se abrira un menu con un teclado con letras y numeros.

- para cambiar la altura o la edad, se debe seleccionar la casilla correspondiente y se debe
abrir una ventana que vaya cambiando en +1 si se hace con la flecha hacia arriba o -1 si hace
la flecha hacia abajo.

- el nombre debera estar restringuido a un maximo de 15 caracteres con al menos 2 como minimo
para poder permitir crear el jugador

- la edad debe ser de entre 16 y 44 años

- la altura debe estar entre 140 y 210 cm



Constraints:

- Un solo archivo HTML, con el CSS en un <style> y el JS en un <script>.

- Vanilla JS, sin frameworks ni dependencias externas.
```

**Qué intentaba lograr:** Intentaba lograr una web que imite completamente la interfaz
incomoda que se usaba para los juegos en nuestra infancia al momento de tener que colocar un
nombre con un mando de PS2. No conocia los estilos de letras asi que esperaba que la IA
determinara el estilo original por mi. 

**Qué devolvió:** Devolvio una web que a primera vista cumple con el estilo de letras y
colores del juego original, quizas los colores no son exactamentes los mismos pero si muy
parecidos. Agrego sonidos y logos de konami y PS2. La interfaz es incomoda segun el
comportamiento que se describio, salvo por dos problemas:
- Al abrir una casillas para completar, se abre como pop up encima de la ventana original
impidiendo hacer clic en los botones.
- Permite usar las teclas del teclado fisico para emular el hacer clic en el Joystick. Como
la idea es hacer una interfaz incomoda se debe corregir.


**Qué hice con eso:** Como una primera version esta bien, pero necesita corregir el
comportamiento al editar las casillas de Nombre, Edad y Altura. Ademas, de bloquear 
el uso del teclado.

---

## 2 — Iterar sobre el estado: Correccion de Comportamiento

```
La web en general esta muy bien, pero se debe corregir lo siguiente en el comportamiento:

- al abrir una casilla para completar un dato, no debe abrirse como un pop up que impida
hacer clic en el mando sumulado ya que se la idea es que el usario use este mando para
navegar y completar la entrada de datos.

- con el teclado fisico se puede simular el comportamiento del teclado, es necesario
restringir esto y que la unica forma de navegar por la web y entrar datos sea haciendo
clic sobre el mando. 


```

**Qué intentaba lograr:** Corregir el comportamiento indeseado.

**Qué devolvió:** Se corregio el comportamiento y la web esta casi completa. Me devolvio
solo parte del codigo porque el html termino siendo muy extenso.

**Problema:** La web termino siendo muy extensa por un solo archivo html. Sobre todo
contiene muchos tipos de estilos.

---

## 3 — Correciones menores del estilo, sintaxis, etc. Y disminuir la cantidad de estilos.

```
el archivo actual es este. Realiza estos pasos en orden:

Primero agrega ":" despues de Nombre, Edad y Altura.

Segundo, cambia el estilo de las casillas con lo datos actuales. Pasa casillas mas
minimalistas con un espacios iguales y divididos para cada caracter, con fondo blanco y
minimalista y letras negras. El nombre debe tener 15 casillas de caracter, algunas puede
quedar vacias. La edad debe tener 2 al lado de las casillas colocar "años" y la altura 3
casillas y al lado colocar "cm". Ten en cuenta que con este cambio al seleccionar una
casilla para entrar datos, debe poder seguirse usando los botones del mando.

Tercero cambia "Mando Playstation 2 (Haz clic ... )" por solo la palabra SONY en el
medio de los mandos.

Cuarto simplifica los estilos, funciones y variables.

```

Nota: Ajunte el archivo html del con los cambios del promt 2, ya que no me lo dio completo.

**Qué intentaba lograr:** Resolver fix menores de estilo y sobre todo disminuir la
cantidad de lineas de codigo para simplificar y que todo entre dentro del contexto
del modelo.

**Qué devolvió:** Simplifico el codigo, aplico los cmabios en los estilos. Y la web
quedo lista.

---

## Conversación completa

Una sola conversación de Gemini Canvas, sin reiniciar el hilo. El artefacto final tiene 989 líneas en un archivo.
