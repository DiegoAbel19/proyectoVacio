# Actividades

Diagramas de actividades UML: flujo de trabajo con **decisiones, ramas y
actores** (si el proceso de la tienda tiene mucha lógica condicional).

## Estructura

- Un `.md` por proceso: `act-<nombre>.md` (bloque de
  `docs/plantillas/plantilla-diagrama-drawio.md`).
- Fuente: `diagramas/drawio/act-<nombre>.drawio`
- PNG: `diagramas/exportaciones/act-<nombre>.png`

## Reglas

- Rombo de decisión siempre con etiquetas en las ramas (Sí/No, condiciones).
- Barras de fork/join si hay pasos paralelos.
- Incluir swimlanes si intervienen varios actores.

## Pendiente

- [ ] Evaluar si hace falta: si el proceso es lineal, el diagrama de secuencia
      suele alcanzar.
