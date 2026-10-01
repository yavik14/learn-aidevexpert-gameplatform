# Build Brief

## Problem

La Semana Santa andaluza tiene un público enorme y muy fiel (cofrades, andaluces y turistas), pero apenas existe representación **interactiva y atractiva en móvil**. El interés cultural no tiene un producto digital con el que jugar y sentirse parte de la tradición.

## Current Workaround / Existing System

El público consume la Semana Santa de forma **pasiva**: vídeos, retransmisiones, fotos y apps informativas de hermandades o itinerarios. Los juegos de plataformas móviles existentes son genéricos y no conectan con la tradición.

## Target Users

- **Primario:** público cofrade/andaluz, con vínculo real con la Semana Santa (alta identificación con el tema).
- **Secundario:** turistas que visitan Andalucía durante la Cuaresma y la Semana Santa y quieren una puerta de entrada lúdica a la tradición.

## Goals

- Diseñar y publicar en **Google Play** un juego de plataformas 2D para Android con identidad propia de Semana Santa.
- Ofrecer **tres personajes jugables con mecánicas diferenciadas**: Costalero (ritmo/música), Nazareno (plataformas de precisión), Cofrade (puzle).
- Estructurar el MVP como **tres niveles, uno por personaje**, con selección de personaje por nivel.
- Monetizar de forma no intrusiva con **rewarded + intersticial**.

## Non-Goals

Estos límites son parte de la definición del producto. `[PROPUESTO — confirmar]`

- **Sin multijugador**, online ni rankings sociales.
- **Sin compras dentro de la app (IAP)** ni suscripciones: solo publicidad.
- **Sin más de 3 niveles** en el MVP.
- **Sin localización** a otros idiomas: solo español.
- **Sin editor de niveles** ni contenido generado por el usuario.
- **Sin personajes adicionales** ni modo historia largo.
- **Sin versión iOS** en el MVP.

## MVP Slice

Tres niveles jugables, **uno por personaje**, con selección de personaje antes de cada nivel:

1. **Costalero** — avanza al compás de la marcha; acertar el ritmo da impulso y fervor.
2. **Nazareno** — plataformas de precisión entre la multitud.
3. **Cofrade** — puzle de sincronía y entorno para abrir paso.

Incluye: pantalla de selección, HUD mínimo, progreso con fervor, y los dos formatos de anuncio. Reutiliza el mismo escenario base donde sea posible para reducir coste de arte.

## Validation Plan

**Publicación directa** en Google Play (elección del usuario). Se aprende con datos de producción en lugar de un test cerrado previo.

- Instrumentar métricas mínimas desde el día uno: finalización por nivel, retención D1, impresiones y aceptación de anuncios.
- Revisar resultados a las 2 semanas y decidir el siguiente paso.

## Success Criteria

`[SUPUESTO — confirmar umbrales]`

- La mayoría de jugadores completa **al menos el primer nivel**.
- Retención **D1** suficiente para sostener el modelo de ads (objetivo inicial: >20 %).
- Los anuncios se muestran **sin romper la sesión** y sin errores en consola.
- Comentarios cualitativos del público cofrade que confirmen que el tema se trata **con respeto**.

## Notes

- **Motor:** Godot 4, exportación Android.
- **Arte:** pixel art **lo-fi de 32 bits** (ver `DESIGN.md`).
- **Fuente de partida:** `docs/brief-prompt.md` (prompt Rol–Audiencia–Tarea–Contexto–Salida).
- Documentación **en español**.
