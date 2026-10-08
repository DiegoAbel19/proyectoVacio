# Fase 3 — Modelo de dominio

Se identifican las **entidades** del mundo del problema (clases, atributos y
relaciones) que el sistema necesita conocer. Es el puente entre los casos de uso
y el modelo de clases del diseño.

## Documentos

| Archivo | Contenido |
|---------|-----------|
| `01-listado-entidades.md` | Entidades, atributos clave y responsabilidades |
| `02-relaciones.md` | Asociaciones, cardinalidades y jerarquías |
| `diagrama-clases-dominio.md` | Referencia al diagrama de clases (fuente `.drawio`) |

## Cómo derivar las entidades

1. Revisar los UC y subrayar los **sustantivos** que aparecen en los flujos
   (pedido, producto, cliente, pago…).
2. Preguntar de cada uno: ¿el sistema debe **recordar** o **registrar** algo de él?
   Si sí, es candidato a entidad.
3. Definir sus atributos mínimos (solo los que el sistema guarda).
4. Establecer relaciones y **cardinalidades** (1..1, 0..*, 1..*).

## Checklist de salida

- [ ] Cada entidad se justifica en al menos un UC.
- [ ] No entidades «de relleno» sin UC que la use.
- [ ] Atributos: solo datos que el sistema persiste (los cálculos van en operaciones).
- [ ] Cardinalidades revisadas y coherentes con las reglas de negocio.
- [ ] Entidades del glosario coinciden con las del modelo.

> **Duda típica:** «¿esto es clase o atributo?» — si tiene subestructura propia o
> aparece repetido en varios UC, suele ser clase; si es un dato simple de una
> clase, es atributo. Registrar la duda en `apuntes/dudas-para-clase.md`.
