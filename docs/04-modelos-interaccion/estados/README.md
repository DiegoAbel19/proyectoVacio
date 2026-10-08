# Estados

Diagramas de estados UML: **ciclo de vida** de los objetos con estado interesante
(en la tienda probablemente: Pedido, Quizás Producto o Pago).

## Estructura

- Un `.md` por objeto: `est-<objeto>.md` (bloque de
  `docs/plantillas/plantilla-diagrama-drawio.md`).
- Fuente: `diagramas/drawio/est-<objeto>.drawio`
- PNG: `diagramas/exportaciones/est-<objeto>.png`

## Reglas

- Nodo inicial = punto ●; final = diana ◉; estados en rectángulos redondeados.
- Cada transición con **evento [condición] / acción**.
- Sin estados «fantasma»: todo estado debe poder justificarse en un UC o regla
  de negocio.

## Pendiente

- [ ] Elegir los objetos con ciclo de vida real (no modelar estados de todo).
