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

### La voz

La voz sintética del móvil es el punto débil de cualquier juego así: la prosodia
en español es mala y un niño que está aprendiendo a hablar necesita un modelo
bueno. Hay tres opciones, en el panel de adultos → **Tu voz**:

**1. Mi voz (lo mejor).** Una grabadora integrada: mantienes pulsado, dices la
palabra, la sueltas y pasa sola a la siguiente. Voz familiar, entonación real y
puedes exagerar los labios donde te convenga.

Solo se graban **palabras sueltas**, no frases. Las frases se montan encadenando
tus clips, que es justo lo que interesa: el niño oye «come… manzana» segmentado,
en el mismo ritmo en el que se iluminan los pictogramas de la tira. Para el
nivel 3 la voz sintética dice la frase completa y bien construida («Osito come
la manzana») mientras que con tu voz suena segmentada; las dos cosas son
correctas para lo que hace cada una.

El vocabulario está agrupado **por habitación**, así que no hay que grabarlo todo
para empezar: la cocina son ocho clips, menos de un minuto, y esa escena ya
funciona entera con tu voz. En total son unas 69 palabras. Lo que falte lo cubre
la voz del móvil, y el panel lleva la cuenta de lo grabado.

**2. Voz del móvil.** Si se usa, conviene instalar una voz «mejorada», que es
gratis y suena bastante mejor que la de fábrica: en iPhone/iPad, Ajustes →
Accesibilidad → Contenido hablado → Voces → Español → *Mónica (Mejorada)*; en
Android, Ajustes → Sistema → Idiomas → Salida de texto a voz → Google. También
se puede ajustar velocidad y tono.

**3. «La digo yo».** El juego se queda mudo: solo marca con un tono suave cuándo
toca cada palabra, y la dices tú en directo. Es lo que haría una logopeda, y no
requiere grabar nada.

### Copia de seguridad de la voz

Las grabaciones viven en IndexedDB, o sea en ese navegador y solo ahí: se
pierden si se borran los datos de navegación. En el panel hay **Exportar** e
**Importar**, que las empaquetan en un único `.json` (unos cientos de KB con
todo grabado). Sirve para dos cosas: no perder media hora de trabajo, y llevar
la misma voz del móvil a la tablet.

La importación **fusiona**: añade las que falten y reemplaza las que coincidan,
nunca borra lo que no venga en el fichero. Si la copia se grabó con otro nombre
para Osito, avisa de que las frases con el nombre habrá que rehacerlas.

La exportación tiene dos caminos, porque el visor de artifacts de claude.ai
bloquea las descargas que inicia la propia página: si la página se abre ahí, usa
la capacidad `downloads` de la plataforma (el visor pide confirmación); en
cualquier otro sitio —el fichero guardado en el dispositivo, GitHub Pages— usa
una descarga normal.

Detalles: el micrófono necesita https o el fichero abierto desde el propio
dispositivo. Si le cambias el nombre a Osito habrá que regrabar las dos frases
que lo contienen.

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

- Voz grabada por el adulto en `MediaRecorder` a 48 kbps, guardada como blobs en
  `IndexedDB` y reproducida por Web Audio (`decodeAudioData` + `BufferSource`),
  que en iOS es mucho más fiable que un `<audio>` suelto. Todo lo que suena pasa
  por una sola función, que decide entre clip grabado, voz sintética o silencio.
- Respaldo con `SpeechSynthesis` del propio dispositivo. Si no hay voz en español
  instalada, los juegos avisan en el panel de adultos y siguen funcionando:
  dibujos, frase escrita y premio sonoro.
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
