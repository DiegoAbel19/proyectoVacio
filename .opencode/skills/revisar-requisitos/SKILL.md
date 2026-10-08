---
name: Revisar requisitos
description: Crea, audita y corrige requisitos funcionales (RF) y no funcionales (RNF) de la Tienda_Automatizada evaluando calidad (ambigüedad, verificabilidad, completitud, consistencia, trazabilidad) y devolviendo observaciones priorizadas. Usar cuando se agreguen requisitos, se pida revisar/corregir un listado de RF o RNF, o se prepare la sección de requisitos de un entregable.
---

# Revisar requisitos

Trabaja sobre `docs/01-requisitos/02-requisitos-funcionales.md` y
`03-requisitos-no-funcionales.md`, con el formato de
`docs/plantillas/plantilla-requisito.md`.

## Flujo de trabajo

1. **Leer** los listados actuales + `01-actores-y-alcance.md` (los requisitos
   deben respetar el alcance definido).
2. **Si es alta de nuevos requisitos:**
   - Pedir la fuente de cada uno (¿quién lo pidió? ¿observación? ¿normativa?).
     Sin fuente → marcar `[SUPUESTO]`.
   - Redactarlos con el formato de la plantilla (fila en tabla + detalle si hace falta).
   - Asignar `RF-XX` / `RNF-XX` correlativos sin reutilizar números.
3. **Si es auditoría:** aplicar la revisión por dimensiones y devolver
   observaciones (formato abajo).
4. **Actualizar** la trazabilidad hacia los UC si ya existen.

## Revisión por dimensiones

| Dimensión | Pregunta clave | Señal de alarma |
|-----------|----------------|------------------|
| Claridad | ¿Una sola lectura se entiende? | «etc.», «y/o», «si es posible» |
| Verificabilidad | ¿Se puede comprobar sí/no? | «rápido», «fácil», «amigable», «intuitivo» |
| Atomicidad | ¿Una idea por requisito? | frases con «y» uniendo funciones |
| Consistencia | ¿Choca con otro RF? | dos RF que exigen comportamientos opuestos |
| Completitud | ¿Cubre todo el alcance? | funcionalidad del alcance sin RF |
| Trazabilidad | ¿Tiene fuente y UC? | RF sin origen ni UC |
| No solucionar | ¿Describe QUÉ no CÓMO? | «usar base MySQL», «botón azul» |

- **RF:** funciones del sistema (qué hace).
- **RNF:** calidad o restricciones (cómo debe ser). Se recomienda clasificarlos:
  rendimiento, seguridad, usabilidad, disponibilidad, mantenibilidad, legal.
  Un RNF que no es medible ni comprobable → rechazar o pedir métrica.

## Formato de devolución

Devolver una tabla ordenada por severidad:

| ID | Severidad | Problema | Regla | Sugerencia |
|----|-----------|----------|-------|------------|
| RF-03 | 🔴 Alto | No verificable («rápido») | Claridad | Poner métrica: «< 3 s» |
| RF-07 | 🟡 Medio | Sin fuente | Trazabilidad | Marcar `[SUPUESTO]` o preguntar |
| — | 🟢 Bajo | Nomenclatura desalineada | Corregir a RF-XX |

- 🔴 Alto = bloquea la entrega · 🟡 Medio = corregir antes de modelar · 🟢 Bajo = cosmético.
- Nunca corregir en silencio: siempre mostrar original → sugerencia.

## Después de la auditoría

1. Aplicar los cambios **solo** con el visto bueno del usuario.
2. Recordar que los RF recién aprobados deben traducirse en UC
   (ofrecer la skill `redactar-caso-de-uso`).
3. Actualizar la fecha de la última revisión en el documento.
