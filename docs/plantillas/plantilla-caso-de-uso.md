# Plantilla — Caso de uso (UC)

> Copiar a `docs/02-casos-de-uso/UC-XX-nombre.md`. Ejecutar antes la skill
> `redactar-caso-de-uso` si se necesita guía.

---

# UC-XX — Nombre del caso de uso

| Campo | Valor |
|-------|-------|
| **ID** | UC-XX |
| **Nombre** | Verbo en infinitivo + objeto (ej. «Registrar pedido») |
| **Actor principal** | Quién tiene la meta |
| **Actor(es) secundario(s)** | Sistemas/personas auxiliares |
| **Descripción** | Una frase: qué logra el actor |
| **Requisitos relacionados** | RF-XX, RF-XX |

## 1. Precondiciones

- Situación que debe darse **antes** de que el caso de uso pueda iniciar.

## 2. Postcondiciones

- **Éxito:** en qué estado queda el sistema si todo sale bien.
- **Fallo:** en qué queda si algo falla.

## 3. Flujo principal

1. El actor inicia…
2. El sistema valida…
3. El sistema registra…
4. El caso de uso termina con…

## 4. Flujos alternativos

### A1 — [nombre o condición]

1. Se produce cuando… (condición concreta)
2. El sistema…
3. Vuelve al paso X del flujo principal (o termina).

## 5. Flujos de excepción

### E1 — [qué falla]

1. Ocurre cuando… (error, caída, dato inválido)
2. El sistema informa…
3. El caso de uso termina sin cumplir la postcondición.

## 6. Reglas de negocio

- Regla BR-XX: …

## 7. Diagrama

Ver `docs/plantillas/plantilla-diagrama-drawio.md` para insertarlo.

---

## Errores frecuentes (revisar antes de dar por buena la ficha)

- ❌ Nombre con «Hacer clic en…» o nombres de pantalla → nivel de interfaz.
- ❌ Un solo paso tipo «El sistema procesa el pedido» → falta el flujo real.
- ❌ Alternativos sin condición clara.
- ❌ Mezclar varios objetivos del usuario en una misma ficha.
