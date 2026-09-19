# Juegos

Juegos caseros de estimulación del lenguaje para jugar en el móvil o la tablet.
HTML puro: sin dependencias, sin servidor, sin cuentas y sin enviar ningún dato
fuera del dispositivo.

Los dos juegos son el mismo motor en dos escalones distintos del desarrollo. Se
elige por lo que el niño hace hoy, no por su edad.

| | Objetivo | Cuándo |
|---|---|---|
| [**La casa de Osito**](casa-de-osito/index.html) | Verbos y combinación de 2–3 palabras | Ya dice palabras sueltas |
| [**Dilo conmigo**](dilo-conmigo/index.html) | Primeras palabras, con onomatopeyas | Aún no dice palabras |

Lo que comparten, y que es lo que de verdad hace trabajo:

- **Pausa expectante.** Tras modelar, la app **se calla** durante 3, 5 u 8
  segundos y lo señala en pantalla (👂 «te toca» y una barra que se vacía). Ese
  silencio es la parte activa: es el hueco que el niño tiene que llenar. El
  adulto mira a la cara con gesto de espera y no lo rellena.
- **Cero fracaso.** No hay puntos, ni tiempo, ni sonido de error, ni se pierde.
- **Refuerzo del intento, no de la pronunciación.** El botón **¡Lo dijo!** lo
  pulsa el adulto ante *cualquier* aproximación. No hay reconocimiento de voz a
  propósito: con habla infantil falla mucho y convertiría el juego en un examen
  que el niño pierde.
- **Panel de adultos** tras mantener pulsada la rueda ⚙️, para que el niño no
  entre solo, con el recuento de intentos de los últimos 7 días.

---

## La casa de Osito

Osito vive en cinco escenas —cocina, baño, cuarto, salón y parque— con seis
objetos cada una. El niño le da un objeto y Osito hace algo con él; la acción se
convierte en una **frase visible**, pieza a pieza, que luego se dice en voz alta.

Sin onomatopeyas: aquí el material de trabajo son **verbos**. Hay veintitantos
(come, bebe, se lava, duerme, lee, se viste, abraza, construye, sopla, monta,
huele, acaricia, llena…), que es justo la pieza que suele faltar cuando un niño
se queda atascado en palabras sueltas: sin verbo no hay frase.

### La tira de frase

Es el mecanismo central. Cada acción se muestra como pictogramas encadenados que
se van iluminando mientras se pronuncian, y después se dice la frase entera:

```
[😋 come] [🍎 manzana]     →  «come manzana»
```

Ver la frase montada en trozos hace visible algo que en el habla es invisible:
que una frase son piezas que se combinan, y que se pueden cambiar de una en una.

### Los tres modos

| Modo | Qué entrena |
|---|---|
| **Jugar con Osito** | Producción. El niño elige, Osito actúa, la frase se construye y se oye. Elegir es lo que provoca hablar. |
| **Hazlo tú** | Comprensión de **órdenes de dos elementos**: «guarda la sopa en la caja», «dale la manzana a Osito». Objeto *y* destino. |
| **Construye la frase** | El niño monta la frase pieza a pieza eligiendo entre dos o tres opciones, y Osito la ejecuta. A partir del nivel 2. |

### Los tres niveles

El nivel cambia la frase entera del juego, no solo el texto:

| Nivel | Osito diría | Para quién |
|---|---|---|
| 1 · palabra | «manzana» | Aún dice palabras sueltas |
| 2 · dos palabras | «come manzana» | **El salto importante**: abre la gramática |
| 3 · frase | «Osito come la manzana» | Ya junta dos palabras |

En el nivel 1 el modo «Hazlo tú» se reduce a una orden de un elemento («toca la
manzana») y basta con tocar; el modo «Construye la frase» queda desactivado.

### Dos formas de manejarlo

Se puede **arrastrar** el objeto hasta Osito o, si le cuesta motrizmente,
**tocar el objeto y después a Osito**. Las dos rutas hacen exactamente lo mismo;
no hay que elegir ni configurarlo.

### Ajustes

Manteniendo pulsada la rueda ⚙️: nivel, **nombre de Osito** (se le puede poner el
de su peluche de verdad, y se dice en voz alta), voz y velocidad, duración de la
pausa, escenas activas, sonido de premio, animaciones e historial de intentos.

Recomendación de arranque: nivel **2**, solo la **cocina**, velocidad lenta,
pausa de 5 s. Comer y beber son las acciones más frecuentes de su día y las que
antes se generalizan fuera del juego.

---

## Dilo conmigo

El escalón anterior, para cuando todavía no hay palabras. Onomatopeya antes que
palabra («guau» sale antes que «perro»), troceo en sílabas para las palabras sin
sonido propio, un modo de comprensión con dos o tres opciones y un modo de
petición con pompas de jabón que entrena pedir «más».

---

## Notas técnicas

- Voz con `SpeechSynthesis` del propio dispositivo. Si no hay voz en español
  instalada, los juegos avisan en el panel de adultos y siguen funcionando:
  dibujos, frase escrita y premio sonoro. Decir tú las palabras en voz alta
  funciona mejor que cualquier síntesis.
- El premio se genera con Web Audio; no hay ficheros de audio.
- Los dibujos son emoji del sistema: nada que descargar, nítidos a cualquier
  tamaño.
- Arrastre con Pointer Events, así que funciona igual con dedo y con ratón.
- Ajustes e historial en `localStorage`, solo en ese dispositivo.
- Respetan `prefers-reduced-motion` y el tema claro/oscuro del sistema.

### Sin conexión

Cada juego es un único fichero. Basta con guardarlo en la tablet y abrirlo, o
servir el repositorio estático (GitHub Pages lo sirve tal cual). En iOS y Android
también vale «Añadir a la pantalla de inicio» para abrirlo a pantalla completa.

### Aviso

Son juguetes para acompañar, no una terapia. Si hay retraso del lenguaje, quien
marca los objetivos y el plan es la logopeda o el equipo de atención temprana;
estos juegos pueden usarse para practicar en casa el vocabulario que ellos
indiquen. Añadir palabras, objetos o acciones nuevas es editar el array `SCENES`
(o `DATA`) al principio del `<script>` de cada juego.
