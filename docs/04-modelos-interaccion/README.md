# Fase 4 — Modelos de interacción

Detalle **cómo** ocurren los casos de uso: qué objetos intervienen, en qué orden
se intercambian mensajes y cómo cambian de estado los objetos a lo largo del tiempo.

## Subcarpetas

| Carpeta | Diagrama UML | Responde |
|---------|--------------|----------|
| `secuencia/` | Diagrama de secuencia | ¿En qué orden se comunican los objetos para cumplir un UC? |
| `estados/` | Diagrama de estados | ¿Qué ciclo de vida tiene un objeto clave (pedido, producto)? |
| `actividad/` | Diagrama de actividades | ¿Cómo es el flujo de trabajo o las decisiones del proceso? |

## Qué va en cada una

- `secuencia/`: un `.md` por UC relevante + placeholder/diagrama `.drawio`.
- `estados/`: un `.md` por objeto con ciclo de vida interesante.
- `actividad/`: un `.md` por proceso con reglas o ramas condicionales.

## Checklist de salida

- [ ] Cada diagrama de secuencia corresponde a un UC existente (Fase 2).
- [ ] Participantes del diagrama = entidades del Fase 3.
- [ ] Mensajes coherentes con el flujo principal de la ficha UC.
- [ ] Diagrama de estados: todos los estados y transiciones tienen condición/disparador.
- [ ] Sin estados «fantasma» que no aparecen en ninguna parte.
- [ ] Fuentes `.drawio` en `diagramas/drawio/` y PNG en `diagramas/exportaciones/`.

> **Orden recomendado:** primero secuencia (valida los UC), luego estados (solo
> objetos con ciclo de vida), actividades si el proceso tiene mucha lógica ramificada.
