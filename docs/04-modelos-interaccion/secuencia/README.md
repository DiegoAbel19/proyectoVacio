# Secuencia

Diagramas de secuencia UML: **en qué orden** se intercambian mensajes los objetos
para cumplir un caso de uso.

## Estructura

- Un `.md` por UC relevante: `seq-uc-XX-nombre.md` (copiar bloque de
  `docs/plantillas/plantilla-diagrama-drawio.md`).
- Fuente: `diagramas/drawio/seq-uc-XX-nombre.drawio`
- PNG: `diagramas/exportaciones/seq-uc-XX-nombre.png`

## Reglas

- El diagrama debe corresponder a un **UC existente** (Fase 2) — indicar cuál.
- Participantes = actores + entidades del modelo de dominio (Fase 3).
- Mensajes numerados en el mismo orden que el flujo principal de la ficha UC.
- Devoluciones con flecha punteada; marcar inicio y fin.

## Pendiente

- [ ] Definir qué UC tienen diagrama de secuencia (los principales primero).
