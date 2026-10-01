# Mecánicas

> Definición de las mecánicas del MVP. `[ACTUALIZADO: 4 personajes y modelo de fervor 0–3]`
> Modelo: **selección de personaje por nivel** (1 nivel por personaje). `[PROPUESTA — pendiente de validar por el usuario]`

## Principios comunes

- **Un input principal por personaje**, claro en móvil.
- **Fervor del espectador** compartido: empieza en cero, crece con los aciertos y **baja con los fallos**; al cerrar cada chicotá/tramo otorga una **calificación de 0 a 3** (nada / 1 / 2 / 3). **No bloquea la progresión**: fallar solo resta puntuación.
- **Ritmo, no velocidad**: cada chicotá tiene un **tiempo objetivo** y **ir corriendo también resta**; se busca un ritmo idóneo.
- **Sesiones de 3–5 min** por nivel.
- **Fallo justo**: el bloqueo siempre es recuperable (reintentar o revivir con rewarded).
- **Accesibilidad**: el ritmo no debe ser la única forma de jugar; prever apoyos visuales y modo simplificado.

---

## 1. Costalero — Ritmo, voces de mando y calle

**Fantasía:** llevar el paso al compás de la marcha, dando las voces correctas para recorrer la calle sin descomponerse.

**Núcleo rítmico:** el juego se rige por **pulsos**. Cada voz de mando define el **son** (medio o pulso completo), la **zancada** y, a veces, el **patrón de pies**. El jugador ejecuta la voz correcta al compás según lo que pida el recorrido.

**Las 12 voces (todas en el MVP):**

| # | Voz | Función | Efecto | Desgaste |
| --- | --- | --- | --- | --- |
| 1 | Andando | Avance normal | Avance base, **medio pulso** | Mínimo |
| 2 | Racheado | Avance | **Zancada larga** | Medio |
| 3 | Izquierdo | Patrón de pies | Avanza un pulso con el **izquierdo** y **iguala con el derecho** al siguiente | **Alto** |
| 4 | Costero | Avance | El **son dura un pulso completo** | **Alto** |
| 5 | Picaíto | Balance | **Balance alante y atrás**, **4 medios pulsos** | Alto |
| 6 | Pasito | Avance + mantener | Avanza **un paso en medio pulso** y se **mantiene tres** | Bajo |
| 7 | Tres Pasitos | Avance múltiple | **3 pasos decididos en 3 medios pulsos** + otros medios pulsos **en el sitio** | **Máximo** |
| 8 | Gateado | Avance mínimo | Anda **avanzando muy poco** | **Máximo** |
| 9 | Vámonos | Avance decidido | Avance decidido, **medio pulso** | **Medio** |
| 10 | Levantá | Postura | **Inicio** de la chicotá | `[ABIERTO]` depende de la mecánica de *levantar* |
| 11 | Arriar | Postura | **Descanso / recuperación** (cierre) | Recupera |
| 12 | **Sobre los pies** | En el sitio | Sin avanzar, **al son de medio pulso** | **Medio** |

**Escala de desgaste:** Mínimo · Bajo · Medio · Alto · Máximo.
`Valores provisionales: se equilibrarán en las pruebas de mecánicas.`

**Chicotá y desgaste:** cada **paso usado desgasta** a los costaleros y **reduce el tiempo de la chicotá**. Si el desgaste agota el tiempo antes del `Arriar`, la chicotá se cierra forzada. `Arriar` recupera.

**Obstáculos de calle:** curvas, calles estrechas, cambios de tempo de la marcha, saludos.

**Control táctil:** paleta de **voces de mando** (botones) + `tap` al compás para ejecutar la voz seleccionada.

**Cierre de chicotá:** `Arriar` → se calcula el **fervor del espectador 0–3**.

---

## 2. Nazareno — Plataformas de precisión

**Fantasía:** recorrer el cortejo entre la multitud con el cirio encendido.

**Bucle:** moverse y saltar con precisión → evitar multitud y obstáculos → llegar a la meta con el cirio encendido.

**Reglas:**
- Movimiento lateral con **salto medido** y **doble salto** desbloqueable.
- El Nazareno lleva un **cirio**: un golpe apaga la llama → fin del nivel.
- **Checkpoints** (hermandad/parada) para no reiniciar todo.
- **Obstáculos:** multitud, escalones, bordillos, alcantarillas, cables, tráfico.
- **Recolectables:** flores y estampas que dan fervor.

**Control táctil:** `joystick` virtual (izquierda) + `botón` de salto (derecha); `swipe arriba` = salto.

**Victoria:** alcanzar la meta con el cirio encendido.

---

## 3. Cofrade — Coordinar la hermandad

**Fantasía:** organizar a la hermandad para cumplir la carrera oficial a tiempo.

**Bucle:** ordenar la comitiva → liberar tramos → ajustar el ritmo de avance al horario → siguiente tramo.

**Reglas:**
- El jugador **ordena la comitiva** arrastrando piezas: nazarenos, pasos y bandas.
- La colocación **influye en el ritmo de avance** de cada tramo.
- Cada tramo de la carrera oficial tiene un **hito horario**; cumplirlo otorga **fervor 0–3**.
- Sin acción en tiempo real: el error **bloquea**, no mata; se reintenta sin coste.

**Control táctil:** `arrastrar` para colocar/ordenar piezas + `tap` para liberar el tramo.

**Victoria / puntuación:** completar la carrera oficial; fervor total por tramos.

---

## 4. Músico — Rhythm game (2 líneas)

**Fantasía:** tocar la marcha tras el paso sin desafinar ni perder el ritmo.

**Bucle:** seguir la partitura → acertar notas en cada línea → subir el fervor → cerrar la chicotá.

**Reglas:**
- **Dos líneas**: **instrumento solista** (melodía) y **ritmo del tambor**.
- Las notas avanzan al compás; acertar suma fervor, **fallar lo baja**.
- Cambios de tempo y pasajes de dificultad creciente.
- **Música:** marchas **libres de uso en formato MIDI**.
- **Cierre de chicotá:** se calcula el **fervor del espectador 0–3**.

**Control táctil:** `tap` (o `swipe`) sobre las notas de cada línea.

**Victoria / puntuación:** cerrar la chicotá; fervor 0–3.

---

## Mapeo resumen de controles

| Personaje | Input principal | Input secundario | Cierre / fracaso |
| --- | --- | --- | --- |
| Costalero | Paleta de voces + `tap` al compás | — | Desgaste agota la chicotá → cierre forzado |
| Nazareno | `joystick` + `botón salto` | `swipe arriba` | Cirio apagado (checkpoint) |
| Cofrade | `arrastrar` para ordenar | `tap` para liberar tramo | Tramo bloqueado (reintentable) |
| Músico | `tap`/`swipe` en 2 líneas | — | Notas falladas bajan el fervor |

**Reglas del fervor del espectador**

- Empieza en **cero**; sube con aciertos y **baja con los fallos**.
- Al cerrar cada **chicotá** (Costalero, Músico) o **tramo** (Cofrade) otorga **0–3** (nada / 1 / 2 / 3).
- **No bloquea la progresión**: fallar solo **resta puntuación**; el nivel se supera igualmente.
- **Tiempo objetivo**: cada chicotá debe cumplir un tiempo, pero **ir corriendo también resta** puntuación. El objetivo es un ritmo idóneo, no ir lo más rápido posible.

**Chicotás por nivel**

- **Variable según el nivel**: niveles cortos con **una sola chicotá**; niveles más largos con **varias**. El tiempo objetivo se aplica a cada chicotá.

## Preguntas abiertas de mecánica

- ¿El doble salto del Nazareno entra en el MVP o se desbloquea? `[SUPUESTO: desbloqueable]`
- Curva de aprendizaje de las **12 voces** en pantalla de móvil.
- **Mecánica de "levantar"**: de momento abierta; determina el desgaste de `Levantá`.
- **Equilibrio del desgaste** de las 12 voces: se ajustará en las **pruebas de mecánicas**.
