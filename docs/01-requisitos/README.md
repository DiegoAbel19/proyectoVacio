# Fase 1 — Requisitos

Primera fase del análisis. Aquí se responde **qué** debe hacer el sistema y
**para quién**, antes de pensar en diagramas o tecnología.

## Documentos

| Archivo | Contenido |
|---------|-----------|
| `01-actores-y-alcance.md` | Quiénes usan el sistema y qué está dentro/fuera del alcance |
| `02-requisitos-funcionales.md` | Listado de RF-XX: funciones que el sistema debe realizar |
| `03-requisitos-no-funcionales.md` | Listado de RNF-XX: calidad, rendimiento, seguridad, etc. |
| `04-glosario.md` | Términos del dominio con su definición única |

## Orden sugerido

1. Glosario (palabras nuevas aparecerán a medida que avance).
2. Actores y alcance.
3. Requisitos funcionales.
4. Requisitos no funcionales.

## Checklist de salida

- [ ] Todos los actores tienen rol definido y justificación.
- [ ] El alcance tiene explícito lo que **no** hace el sistema.
- [ ] Cada RF es verificable (se puede comprobar sí/no).
- [ ] No hay ambigüedades («rápido», «fácil», «etc.»).
- [ ] Cada RNF es medible o al menos comprobable.
- [ ] El glosario cubre todos los términos usados en RF y UC.
- [ ] Todo RF queda trazado al menos a un caso de uso (Fase 2).

> **Nota:** los RF se numeran `RF-01`, `RF-02`… y no se reutilizan números borrados.

## Preguntas iniciales para arrancar

Respondé estas (o pedime que te ayude con la skill `tutor-modelamiento`):

1. ¿Qué es exactamente la «tienda automatizada»? (física, virtual, kiosco…)
2. ¿Quiénes la usan? (cliente, vendedor, admin, proveedor…)
3. ¿Qué opera sola y qué requiere una persona? (el «automatizado» del nombre)
4. ¿Hay algo explícitamente fuera de alcance?
