---
name: Costaleros (MVP Semana Santa)
description: Juego de plataformas 2D para Android con estética pixel art lo-fi de 32 bits y paleta cofrade andaluza.
designAssets:
  sourceOfTruth: []
  generatedConcepts: []
colors:
  primary: "#5B1A2B"
  secondary: "#3B2A5A"
  accent: "#C9A227"
  background: "#0E1020"
  surface: "#1B1F3A"
  text: "#F2EAD9"
typography:
  h1:
    fontFamily: "pixel-serif, monospace"
    fontSize: "24px"
    fontWeight: 700
  body:
    fontFamily: "pixel-sans, monospace"
    fontSize: "16px"
    fontWeight: 400
rounded:
  sm: "2px"
  md: "4px"
spacing:
  sm: "8px"
  md: "16px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.text}"
    rounded: "{rounded.md}"
  button-action:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.background}"
    rounded: "{rounded.md}"
---

# Design Direction

## Overview

Plataformas 2D para Android con **pixel art lo-fi de 32 bits**: paleta más rica que el 16-bit clásico, con aire onírico y nocturno que evoque las procesiones de madrugada. La identidad la marca la **paleta cofrade** (granate, morado, oro, azul noche) y la luz de los cirios.

## Existing Design Assets

Ninguno. No hay Figma, capturas, logo ni guía de marca previos. Esta es la **dirección inicial** creada por la skill `build-brief`.

## Generated Concept Images

Todavía no se han generado imágenes de concepto. `[PENDIENTE — ofrecer generación si el usuario la quiere]`. Si se generan, guardarlas en `docs/design/concepts/` y referenciarlas aquí como inspiración, no como fuente de verdad.

## Product Feel

- **Solemne pero jugable**: respeto por la tradición sin renunciar al placer de un plataformas.
- **Nocturno y cálido**: contraste entre el azul de la noche y el oro de los cirios.
- **Táctil y legible**: botones y zonas de toque pensados para pulgares.

## Colors

- **Granate** `#5B1A2B` — vestimentas, elementos principales.
- **Morado** `#3B2A5A` — penitencia, fondo de escenario.
- **Oro** `#C9A227` — cirios, detalles, recompensas, acento de acción.
- **Azul noche** `#0E1020` — fondo, cielo de madrugada.
- **Superficie** `#1B1F3A` — paneles de UI.
- **Texto** `#F2EAD9` — crema cálido, alto contraste sobre los fondos.

## Typography

Fuente **pixel/monospace** para coherencia con el estilo. `[SUPUESTO — elegir fuente concreta libre]`. Tamaños grandes para legibilidad en pantalla pequeña.

## Layout

- Orientación **horizontal** para el plataformas.
- HUD mínimo: fervor arriba, controles táctiles abajo.
- Zona de juego despejada, sin elementos que tapen al personaje.

## Shapes

- Bordes **poco redondeados** (`2–4px`) para conservar la sensación pixelada.
- Iconos y botones con silueta clara y tamaño de toque mínimo cómodo.

## Components

- `button-primary`: fondo granate, texto crema.
- `button-action`: fondo oro, texto oscuro (acción/compra con fervor).
- `voz-button`: botón de voz de mando (Costalero).
- `nota-lane`: carril de notas (Músico, 2 líneas).
- `fervor-meter`: medidor de fervor del espectador (0–3).
- HUD de fervor y de progreso de nivel.

## Core Screens

1. **Selección de personaje** — Costalero, Nazareno, Cofrade y Músico con su mecánica.
2. **Juego (nivel)** — HUD (**fervor del espectador 0–3**) + controles táctiles; incluye la paleta de **voces de mando** del Costalero y las **2 líneas** del Músico.
3. **Resultado de nivel** — calificación de fervor **0–3** por chicotá/tramo, siguiente nivel, anuncio intersticial.
4. **Revivir (rewarded)** — oferta opcional al fallar.

## Responsive Baseline

- Objetivo: pantallas de móvil Android, orientación horizontal.
- Escalado por píxeles enteros para no emborronar el pixel art.
- Zonas táctiles adaptadas a distintos tamaños de pantalla.

## Accessibility Baseline

- Alto contraste texto/fondo.
- No depender solo del color para indicar estado.
- Opción de reducir/reintentar en puzles (mecánica del Cofrade).
- Considerar alternativa a la dependencia total del ritmo para jugadores con dificultades auditivas/motoras.

## Do's and Don'ts

- **Sí**: tratar los símbolos con respeto; luz cálida; paleta cofrade coherente.
- **No**: parodiar la tradición; usar estereotipos ofensivos; recargar el HUD.
- **No**: mezclar estilos gráficos (todo pixel art lo-fi consistente).

## Open Design Questions

- ¿Fuente pixel concreta (licencia abierta) para títulos y UI?
- ¿Se generan conceptos visuales con `imagegen` para alinear antes de producir arte?
- ¿Cómo se representa a los personajes sin caer en simplificaciones que molesten al público cofrade?
