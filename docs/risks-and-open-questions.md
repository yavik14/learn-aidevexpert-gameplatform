# Risks and Open Questions

## Blocking Next Phase

- **Validar las mecánicas concretas.** Las reglas y controles de los cuatro personajes están redactados en `docs/mechanics.md`, pero **falta que el usuario los confirme** antes de escribir la spec del primer nivel.
- **Integración del SDK de anuncios** (p. ej. AdMob) en Godot 4 para Android: confirmar plugin y compatibilidad con la versión de Godot elegida.

## Implementation-Time Questions

- ¿Cómo se guarda el progreso (fervor, niveles desbloqueados) de forma local?
- ¿Qué plugin de anuncios se usa y cómo se prueba sin publicar?
- ¿Se reutiliza el mismo escenario en los cuatro niveles o cada uno tiene arte propio?
- ¿El fervor de un nivel completado se puede volver a ganar al repetirlo?
- ¿Qué resolución/orientación objetivo y cómo escala el pixel art lo-fi?
- ¿Tamaño máximo del APK/AAB con assets y SDK de ads?

## Later / Not MVP

- Multijugador, rankings y logros sociales.
- Compras dentro de la app (IAP) y quitado de anuncios.
- Localización a otros idiomas.
- Más niveles y nuevos personajes.

## Assumptions

- El público cofrade responderá bien a una representación **respetuosa** (no paródica).
- Godot 4 exporta a Android con rendimiento suficiente en gama media.
- Los ingresos por rewarded + intersticial bastan para cubrir el mantenimiento mínimo.
- El turista captado durante Cuaresma/Semana Santa mantiene algo de retención después.
- **Música:** marchas **libres de uso en formato MIDI** (decisión tomada, sin licencias).

## Risks

- **Publicación directa sin test cerrado**: se aprende con usuarios reales, lo que puede dañar las primeras valoraciones en Play Store si hay bugs o problemas de UX.
- **Sensibilidad cultural**: cualquier error en símbolos, hermandades o tono puede generar rechazo del público objetivo.
- **Rendimiento en gama media** con estética lo-fi y música sincronizada.
- **Políticas de anuncios de Google**: formatos y frecuencia deben cumplir las reglas de Play.
- **Dependencia de una sola fuente de ingresos** (solo ads).
- **Curva de aprendizaje de las 12 voces de mando** del Costalero en pantalla de móvil.
- **Alcance de 4 niveles con un solo dev**: riesgo de no terminar el MVP.
- **Latencia de audio/input** en la mecánica de ritmo (Costalero y Músico) según dispositivo.

## Research Tasks

- Comparar plugins de anuncios para Godot 4 Android y su soporte actual.
- Revisar referentes de plataformas con mecánica de ritmo y su mapeo táctil.
- Documentar buenas prácticas de representación cultural de la Semana Santa antes de definir arte y narrativa.
- Definir cómo se reproducen las **marchas MIDI** en Godot 4 (reproducción, timbre y sincronía con el compás).
