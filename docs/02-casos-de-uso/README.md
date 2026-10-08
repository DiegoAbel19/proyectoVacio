# Fase 2 — Casos de uso

Aquí se traducen los requisitos en **interacciones concretas** entre actores y el
sistema. Un caso de uso (UC) describe una meta completa del usuario.

## Documentos

| Archivo | Contenido |
|---------|-----------|
| `00-indice-casos-de-uso.md` | Tabla maestra de todos los UC con su trazabilidad a RF |
| `UC-XX-nombre.md` | Una ficha por caso de uso (crearlas copiando la plantilla) |

## Reglas

- Nombre del archivo y del UC: `UC-01`, `UC-02`… con 2 dígitos.
- Nombre del caso de uso: **verbo en infinitivo + objeto** («Registrar pedido»).
- **Sin** detalles de interfaz (botones, pantallas) ni de tecnología.
- Un caso de uso = una meta completa del actor; si se corta a mitad, sobra o falta.
- Flujo principal numerado; flujos alternativos y de excepción con su condición.

## Checklist de salida

- [ ] Todo RF tiene al menos un UC que lo cubra.
- [ ] Todo UC está en el índice con su trazabilidad.
- [ ] Los nombres son de nivel meta-usuario (no «Hacer clic en…»).
- [ ] Cada ficha tiene precondiciones y postcondiciones.
- [ ] Flujos alternativos justificados por una condición concreta.
- [ ] El diagrama de casos de uso existe en `diagramas/` (o su placeholder).

> Si un RF no tiene UC, o un UC no cubre ningún RF, es una señal de que algo
> está mal en la Fase 1 o en esta.
