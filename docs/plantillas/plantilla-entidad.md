# Plantilla — Entidad del dominio

> Copiar el bloque por cada entidad en `docs/03-modelo-dominio/01-listado-entidades.md`.

---

## EN-XX — Nombre de la entidad

| Campo | Valor |
|-------|-------|
| **Nombre** | Sustantivo en singular, singular del dominio (ej. «Pedido») |
| **Responsabilidad** | Una frase: qué concepto del negocio representa |
| **UC que la justifica** | UC-XX |

### Atributos

| Atributo | Tipo lógico | Obligatorio | Observación |
|----------|-------------|-------------|-------------|
| idPedido | entero | Sí | Identificador |
| fecha | fecha | Sí | |
| total | decimal | Sí | [SUPUESTO] ¿se calcula o se guarda? |

### Operaciones (solo si aporta al análisis)

- método() → …

### Relaciones

| Hacia | Cardinalidad | Descripción |
|-------|--------------|-------------|
| Cliente | 1..* | Un pedido pertenece a un cliente |

---

## Derivación de entidades (recordatorio)

1. Subrayar sustantivos en los flujos de los UC.
2. Preguntar: ¿el sistema debe recordar algo de esto? → si sí, es entidad.
3. Revisar cardinalidades contra las reglas de negocio.
4. Verificar que no aparezcan entidades sin UC que las use.

## Dudas frecuentes

- **¿Clase o atributo?** Si es un dato simple de otra clase → atributo.
- **¿Tabla o entidad?** En análisis no se piensa en tablas (eso es diseño de BD).
