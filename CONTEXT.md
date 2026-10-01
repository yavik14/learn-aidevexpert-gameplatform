# Context

> Glosario y lenguaje de dominio del proyecto. **No** es un PRD, un plan ni un registro de decisiones.

## Glossary

### Semana Santa
Celebración religiosa y cultural andaluza en la que las hermandades procesionan durante la Cuaresma y la Semana Santa. Es el tema y el escenario del juego.

### Cofrade
Persona que pertenece a una hermandad y participa activamente en su vida. En el juego es uno de los **cuatro personajes jugables**; su mecánica es de **coordinación** (ordenar la comitiva y cumplir la carrera oficial).

### Costalero
Cofrade que porta el paso sobre sus hombros, bajo la trabajadera. Personaje jugable con mecánica de **ritmo y voces de mando** dentro de un recorrido de calle.

### Nazareno
Cofrade que desfila con túnica, capirote y cirio como penitente. Personaje jugable con mecánica de **plataformas de precisión**.

### Músico
Componente de la banda de música que toca tras el paso. Personaje jugable con mecánica de **rhythm game** a dos líneas: instrumento solista y ritmo del tambor.

### Hermandad
Asociación de cofrades que organiza el culto y la procesión de uno o varios pasos.

### Paso
Conjunto escultórico (imágenes, canasto, varales, palio) que procesiona, portado por los costaleros o sobre ruedas.

### Trabajadera
Estructura de varales bajo el paso sobre la que cargan los costaleros.

### Marcha
Composición interpretada por la banda de música tras los pasos; marca el compás al que avanza la cuadrilla.

### Chicotá
Tramo de recorrido que la cuadrilla recorre de una sola vez, desde la **levantá** hasta el **arriar**. Es la unidad de juego de los niveles de Costalero y Músico.

### Levantá
Voz que marca el **inicio** de la chicotá (levantar el paso).

### Arriar
Voz que marca el **descanso / recuperación** y cierra la chicotá (bajar el paso).

### Pulso
Unidad de tiempo de la marcha. Según la voz, el *son* dura **medio pulso** o **un pulso completo** (p. ej. *costero*).

### Son
Duración/compás de cada paso respecto al pulso de la marcha.

### Zancada
Longitud del avance de cada paso (p. ej. *racheado* = zancada larga; *gateado* = avance muy corto).

### Voces de mando
Órdenes que el capataz da a la cuadrilla y que el jugador ejecuta al compás. Conjunto del MVP (**12 voces**). El **desgaste** (Mínimo · Bajo · Medio · Alto · Máximo) es provisional y se equilibrará en pruebas.

- **Andando** — avance normal (medio pulso). Desgaste: Mínimo.
- **Racheado** — andar con **zancada larga**. Desgaste: Medio.
- **Izquierdo** — avanzar un pulso solo con el pie izquierdo y **igualar** con el derecho en el siguiente. Desgaste: Alto.
- **Costero** — el *son* dura **un pulso completo** (no medio). Desgaste: Alto.
- **Picaíto** — **balance alante y atrás** (4 medios pulsos). Desgaste: Alto.
- **Pasito** — avanza **un paso en medio pulso** y se **mantiene tres**. Desgaste: Bajo.
- **Tres Pasitos** — **tres pasos decididos en tres medios pulsos** y otros medios pulsos **en el sitio**. Desgaste: Máximo.
- **Gateado** — andar **avanzando muy poco**. Desgaste: Máximo.
- **Vámonos** — avance decidido (medio pulso). Desgaste: Medio.
- **Levantá** — inicio de la chicotá. Desgaste: depende de la mecánica de *levantar* `[ABIERTO]`.
- **Arriar** — descanso / recuperación (cierre). Desgaste: recupera.
- **Sobre los pies** — en el sitio, **al son de medio pulso**. Desgaste: Medio.

### Desgaste
Gasto que produce cada voz de mando al ejecutarse. Se mide en **5 niveles**: Mínimo, Bajo, Medio, Alto y Máximo. Consume el tiempo de la chicotá; `Arriar` recupera. Valores provisionales hasta las pruebas de mecánicas.

### Fervor del espectador
Medidor-puntuación que empieza en cero y crece con las acciones correctas. Al cerrar cada chicotá otorga **una calificación de 0 a 3** (nada / 1 / 2 / 3 niveles de fervor). No hace "perder"; solo puntúa.

### Fervor
Recurso/puntuación del juego vinculado al fervor del espectador y a las recompensas. Se gana ejecutando bien la mecánica de cada personaje.

### Carrera oficial
Recorrido pautado que una hermandad debe cumplir dentro de una franja horaria. Es la base del nivel del Cofrade.

### Nivel
Unidad jugable del MVP. Existen **cuatro**, uno por personaje.

### Selección de personaje
Modelo de juego del MVP: el jugador elige uno de los **cuatro** personajes **antes** de cada nivel; cada uno tiene reglas y mecánica propias.

### Anuncio recompensado (rewarded)
Anuncio que el jugador decide ver a cambio de una ventaja (revivir, fervor extra, continuar).

### Anuncio intersticial
Anuncio a pantalla completa que se muestra entre niveles, sin recompensa.

## Rejected / Ambiguous Terms

### Espectador
Descartado **como personaje**. Usar `Cofrade`. Motivo: en el dominio, un espectador solo observa, mientras que el personaje participa en la hermandad. (El término sigue vivo solo en `Fervor del espectador`.)
