# Tienda_Automatizada 🛒

Proyecto de la materia **Análisis y Modelamiento de Software**: análisis y modelamiento
UML de un sistema de tienda automatizada.

> **Este repositorio contiene documentación y modelos, no código.**
> La implementación queda fuera de alcance por ahora.

---

## 1. Estructura del proyecto

```
proyectoVacio/
├── AGENTS.md                    # Reglas que sigue el agente de IA al trabajar aquí
├── README.md                    # Este archivo
├── .gitignore
│
├── docs/
│   ├── 01-requisitos/           # Actores, alcance, RF, RNF y glosario
│   ├── 02-casos-de-uso/         # Índice y detalle de los casos de uso (UC-XX)
│   ├── 03-modelo-dominio/       # Entidades del dominio y sus relaciones
│   ├── 04-modelos-interaccion/  # Secuencia, estados y actividades
│   ├── 05-entregables/          # Informes y entregas de la materia
│   └── plantillas/              # Plantillas para copiar antes de redactar
│
├── diagramas/
│   ├── drawio/                  # Archivos fuente .drawio
│   └── exportaciones/           # PNG/SVG exportados desde draw.io
│
├── apuntes/
│   ├── conceptos.md             # Conceptos explicados con mis propias palabras
│   └── dudas-para-clase.md      # Preguntas para llevar a clase
│
├── recursos/
│   └── bibliografia.md          # Bibliografía, enlaces y apuntes de clase
│
└── .opencode/skills/            # Skills del proyecto (ver sección 4)
```

---

## 2. Flujo de trabajo (fases)

El análisis sigue un orden: **cada fase alimenta a la siguiente** y todas se trazan entre sí.

| Fase | Carpeta | Qué produce | Depende de |
|------|---------|-------------|------------|
| 1️⃣ Requisitos | `docs/01-requisitos/` | Actores, alcance, RF, RNF, glosario | — |
| 2️⃣ Casos de uso | `docs/02-casos-de-uso/` | Diagrama y fichas UC-XX | Fase 1 |
| 3️⃣ Modelo de dominio | `docs/03-modelo-dominio/` | Entidades, atributos, relaciones | Fase 2 |
| 4️⃣ Interacción | `docs/04-modelos-interaccion/` | Secuencia, estados, actividades | Fases 2 y 3 |
| 5️⃣ Entregables | `docs/05-entregables/` | Informes de la materia | Todas |

**Regla de trazabilidad:** cada requisito (RF) se asocia a uno o más casos de uso (UC);
cada caso de uso usa entidades; cada entidad aparece en algún UC. Si no se puede
trazar, probablemente sobra o falta algo.

---

## 3. Convenciones

- **Idioma:** español en todo (archivos, diagramas, commits).
- **Archivos:** nombres en minúsculas y con guiones (`requisitos-funcionales.md`).
- **Nomenclatura:**
  - `RF-01`, `RF-02`… → requisitos funcionales
  - `RNF-01`, `RNF-02`… → requisitos no funcionales
  - `UC-01`, `UC-02`… → casos de uso
  - `uc-01-nombre.drawio` → diagramas (misma numeración que su documento)
- **Diagramas:** se dibujan en **draw.io**. El archivo fuente va en `diagramas/drawio/`
  y el PNG exportado en `diagramas/exportaciones/`. Desde Markdown se referencian
  con imagen + link al fuente (ver `docs/plantillas/plantilla-diagrama-drawio.md`).
- **Antes de redactar** cualquier documento nuevo, copiar la plantilla correspondiente
  de `docs/plantillas/`.

---

## 4. Skills del proyecto

Son instrucciones reutilizables que el agente carga cuando hacen falta.
Se invocan nombrándolas (`usá la skill redactar-caso-de-uso`) o con `@id-de-skill`.

| Skill | Para qué sirve |
|-------|----------------|
| `tutor-modelamiento` | Explicar conceptos de la materia con ejemplos de la tienda y proponer ejercicios |
| `redactar-caso-de-uso` | Escribir o mejorar fichas de casos de uso (UC-XX) |
| `revisar-requisitos` | Revisar calidad de RF/RNF: ambigüedad, verificabilidad, trazabilidad |
| `modelo-dominio` | Derivar entidades, atributos y relaciones a partir de los casos de uso |
| `diagramas-drawio` | Convenciones para crear, revisar y exportar diagramas UML en draw.io |

---

## 5. Estado del proyecto

| Fase | Estado | Última actualización |
|------|--------|----------------------|
| 1. Requisitos | ⬜ Pendiente | 2026-10-08 |
| 2. Casos de uso | ⬜ Pendiente | 2026-10-08 |
| 3. Modelo de dominio | ⬜ Pendiente | 2026-10-08 |
| 4. Modelos de interacción | ⬜ Pendiente | 2026-10-08 |
| 5. Entregables | ⬜ Pendiente | 2026-10-08 |

Leyenda: ⬜ Pendiente · 🟡 En curso · ✅ Completo

---

## 6. Cómo empezar

1. Leer `AGENTS.md` (las reglas del proyecto).
2. Abrir `docs/01-requisitos/README.md` y responder la guía de preguntas iniciales.
3. Ir fase por fase, usando las skills cuando el agente necesite producir documentos.
4. Anotar dudas en `apuntes/dudas-para-clase.md` y conceptos nuevos en `apuntes/conceptos.md`.
