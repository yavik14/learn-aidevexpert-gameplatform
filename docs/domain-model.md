# Domain Model

## Core Concepts

- **Personaje**: entidad jugable. Tres instancias: *Costalero*, *Nazareno*, *Cofrade*. Cada una define una mecánica, una habilidad y una debilidad.
- **Mecánica**: regla de juego propia de un personaje. *Ritmo* (Costalero), *Precisión* (Nazareno), *Puzle* (Cofrade).
- **Nivel**: unidad jugable vinculada a un personaje y a una meta. En el MVP hay tres.
- **Meta / Objetivo de nivel**: condición de victoria (p. ej. completar un tramo de la carrera oficial).
- **Fervor**: recurso acumulable que se gana ejecutando bien la mecánica; se usa para progreso y como recompensa canjeable.
- **Obstáculo**: elemento que impide el avance (multitud, tráfico, caída, pérdida de compás).
- **Progreso**: estado de desbloqueo y finalización de niveles.
- **Anuncio**: *rewarded* (opt-in con recompensa) e *intersticial* (entre niveles).

## Relationships

- Un **Personaje** tiene exactamente una **Mecánica** principal.
- Un **Nivel** pertenece a un **Personaje** (MVP: 1:1).
- Un **Nivel** contiene uno o más **Obstáculos** y ofrece **Fervor** al superarse.
- El **Progreso** agrega el estado de los tres **Niveles**.
- Un **Anuncio rewarded** entrega **Fervor** o una segunda oportunidad; un **intersticial** no entrega nada.

## States and Lifecycles

### Nivel
- `bloqueado` → `desbloqueado` (al alcanzar el progreso requerido)
- `desbloqueado` → `en_curso` (al iniciarse)
- `en_curso` → `completado` (al cumplir la meta) o → `fallido` (al agotar vidas/tiempo)
- `completado` desbloquea el siguiente nivel.

### Partida de nivel
- `inicio` → `jugando` → (`revivir` con rewarded) → `jugando` → `completado` | `fallido`

### Anuncio
- `no_solicitado` → `solicitando` → `mostrado` → `cerrado_en_recompensa` | `cerrado_sin_recompensa` | `error_de_carga`

## Important Scenarios

1. **Elegir personaje** antes de un nivel y ver su mecánica y control.
2. **Costalero**: mantener el compás de la marcha para no frenar; el fallo reduce fervor.
3. **Nazareno**: superar plataformas de precisión evitando la multitud.
4. **Cofrade**: resolver un puzle de entorno/sincronía para abrir el paso.
5. **Fallar y revivir**: ver un rewarded para continuar en el mismo punto.
6. **Terminar nivel**: intersticial y retorno a la selección con progreso guardado.

## Edge Cases

- Cierre de la app en mitad de un nivel: el progreso no debe corromperse.
- Anuncio que falla al cargar: el juego debe continuar sin bloquearse (fallback sin recompensa).
- Jugador sin conexión: los niveles deben poder jugarse; los anuncios no.
- Repetición de un nivel ya completado: ¿se vuelve a otorgar fervor? `[ABIERTO]`
- Conflicto entre el compás musical y el input táctil en dispositivos con latencia.
