# Plantilla — Requisito (RF / RNF)

> No se crea un archivo por requisito: se copia el bloque siguiente y se pega en
> `02-requisitos-funcionales.md` o `03-requisitos-no-funcionales.md`.

## Formato de fila (para tablas)

| ID | Requisito | Prioridad | Fuente / Origen | UC relacionados | Estado |
|----|-----------|-----------|-----------------|-----------------|--------|
| RF-XX | … | Alta/Media/Baja | Entrevista / Observación / Normativa | UC-XX | Propuesto |

## Formato detallado (cuando haga falta desarrollar uno)

### RF-XX — Título corto

- **Descripción:** qué debe hacer el sistema, en una sola idea.
- **Criterio de aceptación:** cómo se comprueba que se cumple (sí/no).
- **Prioridad:** Alta / Media / Baja.
- **Fuente:** de dónde salió (quién lo pidió, norma, observación).
- **UC relacionados:** UC-XX.
- **Notas / supuestos:** [SUPUESTO] …

## Reglas de redacción

1. Una idea por requisito (si aparece «y», suele ser dos requisitos).
2. Verificable: otro estudiante debe poder comprobarlo sí/no.
3. Sin ambigüedades: evitar «rápido», «fácil», «amigable», «etc.», «si es posible».
4. Si es medible, poner la métrica: «en menos de 3 s bajo carga de 100 usuarios».
5. **No** meter detalles de tecnología en los RF (eso es diseño, no análisis).

## Preguntas para el checklist

- ¿Este requisito se puede comprobar con una prueba concreta?
- ¿Quién lo pidió y por qué? (si no se sabe → fuente dudosa)
- ¿Tiene conflictos con otro RF?
