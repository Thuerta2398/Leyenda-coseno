# La Leyenda del Coseno 🐉📐

RPG educativo de navegador para practicar la **Ley de los Cosenos** (Matemáticas V, preparatoria).

El estudiante explora un reino en vista cenital, encuentra monstruos en la hierba alta y los vence **resolviendo triángulos**. Cada respuesta correcta es un golpe; cada error, un golpe del monstruo, y el juego muestra la solución paso a paso.

## Cómo se juega

| Zona | Tipo de problema |
|---|---|
| Hierba alta (aldea) | Encontrar un **lado** (LAL): `c² = a² + b² − 2ab·cos(C)` |
| Bosque Sombrío (nivel 3+) | Lados y **ángulos** (LLL): `cos(C) = (a² + b² − c²) / (2ab)` |
| Castillo del Dragón (nivel 5+) | **Problemas aplicados**: barcos, terrenos, túneles, torres |

- Los problemas se generan al azar, así que cada partida es distinta.
- Se pide redondear a 1 decimal, con un margen de tolerancia (±1 % o ±0.15 en lados, ±0.6° en ángulos).
- **Pistas**: la 1.ª muestra la fórmula, la 2.ª la fórmula con los valores sustituidos. Usarlas reduce a la mitad la XP.
- **Calculadora integrada** en grados: `sqrt(5^2+7^2-2*5*7*cos(40))`, `acos(0.25)`.
- Al vencer al Dragón aparece un **certificado** con nombre, aciertos, precisión, pistas usadas y tiempo, para que el estudiante tome captura y lo entregue.

## Computadora, celular y tablet

- **Computadora**: flechas / WASD para moverse, Espacio / Enter para hablar; la respuesta se escribe con el teclado.
- **Celular o tablet** (Chrome o Safari): aparecen una cruceta y un botón **A**. En batalla se usa un **teclado numérico propio del juego** (no se abre el teclado del sistema, que taparía la pantalla); al abrir la calculadora aparecen teclas de √, cos, acos, ^ y paréntesis, y el botón **➜ Resp.** copia el resultado a la respuesta.
- **Vertical**: el juego arriba y los controles abajo.
- **Horizontal** (recomendado en tablet): el juego a la izquierda y la pregunta y los controles a la derecha, todo sin desplazarse.
- Sugerencia: pidan a los estudiantes subir el volumen o tocar 🔊 para silenciar; el sonido solo se activa después de tocar **COMENZAR**.

## Publicar en GitHub Pages

Todo el juego es un solo archivo (`index.html`), sin dependencias que instalar.

1. Crea un repositorio nuevo en GitHub (por ejemplo `leyenda-del-coseno`), público.
2. Sube `index.html` y `README.md` (botón **Add file → Upload files**).
3. Ve a **Settings → Pages**, en *Source* elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`, y guarda.
4. En 1–2 minutos el juego estará en `https://TU-USUARIO.github.io/leyenda-del-coseno/`. Comparte ese enlace con tus grupos.

## Ajustes rápidos para docentes

Al inicio del `<script>` en `index.html`:

```js
const NIVEL_BOSQUE = 3;     // nivel para cruzar el río
const NIVEL_CASTILLO = 5;   // nivel para enfrentar al Dragón
const PROB_ENCUENTRO = 0.12; // probabilidad de encuentro por paso en la hierba
```

- Los textos de los personajes están en el objeto `TXT`.
- Los rangos de los problemas por zona están en la función `genProblem()`.
- El mapa es la lista `SRC` (cada carácter es una casilla; la leyenda está en el comentario de arriba).

Duración aproximada: 20–35 minutos para terminarlo.
