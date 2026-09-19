# Juegos

Juegos caseros para jugar en el móvil o la tablet. HTML puro: sin dependencias,
sin servidor, sin cuentas y sin enviar ningún dato fuera del dispositivo.

## Dilo conmigo

Juego de **estimulación del lenguaje** para un niño de 2–3 años que está
empezando a hablar. Pensado para jugarlo **un adulto y un niño juntos**, no para
dejar al niño solo con la pantalla.

Abrir: [`dilo-conmigo/index.html`](dilo-conmigo/index.html)

### En qué se basa

No es un juego de acertar. Está construido alrededor de cinco cosas que son las
que, en la práctica, hacen que un niño con retraso del lenguaje expresivo se
arranque a vocalizar:

1. **Onomatopeya antes que palabra.** «guau», «muu», «brum» son sílabas
   repetidas con sonidos tempranos: salen mucho antes que «perro» o «coche». El
   juego dice primero el sonido y sólo después la palabra.
2. **Pausa expectante.** Después del sonido la app **se calla** durante 3, 5 u 8
   segundos y lo señala en pantalla (👂 «te toca» + una barra que se vacía). Ese
   silencio es la parte activa del juego: es el hueco que el niño tiene que
   llenar. El adulto debe mirarle a la cara con gesto de espera y no rellenarlo.
3. **Cero fracaso.** No hay puntos, ni tiempo, ni sonido de error, ni se pierde.
   En «¿Dónde está?» una respuesta equivocada solo produce «ese es el gato» y se
   vuelve a preguntar; a la segunda, la opción correcta se mueve para ayudar.
4. **Refuerzo del intento, no de la pronunciación.** El botón grande **¡Lo dijo!**
   lo pulsa el adulto cuando el niño emite *cualquier* aproximación («ua» por
   «guau» cuenta). Suena una celebración inmediata y se anota el intento. No se
   usa reconocimiento de voz a propósito: con habla infantil falla mucho y
   convertiría el juego en un examen que el niño pierde.
5. **Repetición previsible.** La misma secuencia siempre: dibujo → sonido →
   silencio → palabra → palabra. La previsibilidad es lo que permite anticipar y
   participar.

### Los tres modos

| Modo | Qué entrena |
|---|---|
| **Toca y suena** | Producción. Causa-efecto inmediato, onomatopeya, pausa expectante y palabra. Las palabras sin onomatopeya se trocean en sílabas («pe-lo-ta»). |
| **¿Dónde está?** | Comprensión. Elegir entre 2 o 3 dibujos. Sin fracaso posible. |
| **¡Más!** | Petición. Salen pompas, se paran y aparece «¿más?». Al tocar, se dice «¡más!» y vuelven. Entrena la palabra funcional más rentable a esta edad: pedir. |

### Ajustes (para el adulto)

Se abren **manteniendo pulsada la rueda ⚙️** de la pantalla de inicio durante un
segundo, para que el niño no entre solo. Desde ahí se puede cambiar la voz y su
velocidad, la duración de la pausa, las repeticiones del sonido, el número de
opciones, activar o desactivar categorías y ver el recuento de intentos de los
últimos 7 días.

Recomendación de arranque: solo **animales**, velocidad **lenta**, pausa **5 s**,
**2** repeticiones. Se amplía cuando ya repita los sonidos de animales.

### Notas técnicas

- Voz mediante `SpeechSynthesis` del propio dispositivo. Si no hay voz en español
  instalada, el juego avisa en el panel de adultos y sigue funcionando: dibujos,
  palabra escrita y sonido de premio. Decir la palabra tú en voz alta funciona
  mejor que cualquier síntesis.
- El sonido de premio se genera con Web Audio; no hay ficheros de audio.
- Los dibujos son emoji del sistema: nada que descargar y se ve bien en cualquier
  tamaño de pantalla.
- Ajustes y recuento se guardan en `localStorage`, solo en ese dispositivo.
- Respeta `prefers-reduced-motion` y el tema claro/oscuro del sistema.

### Para usarlo sin conexión

Es un único fichero. Basta con guardarlo en la tablet y abrirlo, o servirlo
estático (GitHub Pages sirve el repositorio tal cual). En iOS y Android también
se puede usar «Añadir a la pantalla de inicio» para abrirlo a pantalla completa.

### Aviso

Esto es un juguete para acompañar, no una terapia. Si hay retraso del lenguaje,
quien marca los objetivos y el plan es la logopeda o el equipo de atención
temprana; este juego puede usarse para practicar en casa el vocabulario que ellos
indiquen (añadir palabras nuevas es editar la lista `DATA` al principio del
`<script>`).
