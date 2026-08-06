<h1 align="center">Aldo Cáceres Ruiz Díaz</h1>

<p align="center">
  <strong>Construyo sistemas de agentes de IA que corren en producción.</strong><br>
  Sin escribir código a mano — con método, evidencia y control humano.
</p>

<p align="center">
  <a href="https://github.com/bioqruizdiazaldo-cmd/praxia-ops">PraxIA Ops</a> ·
  Microbiología, bioseguridad y gobernanza QBRN ·
  Argentina 🇦🇷
</p>

---

## Qué hago

Vengo de la ciencia: microbiología, infectología, bioseguridad y gobernanza QBRN-CBRN. En julio de 2026 empecé a construir **PraxIA Ops**, una plataforma de agentes de IA operativos. En 22 días pasó de un primer workflow a un sistema 24/7 con orquestador, 15 subagentes, memoria persistente en PostgreSQL, aprobación humana en las acciones consecuentes y despliegue con rollback.

No escribo la aplicación línea por línea. **Diseño la arquitectura, escribo los contratos, defino las invariantes en la base de datos, y dirijo agentes de código que implementan bajo supervisión.** Esa es la disciplina: el modelo propone, la evidencia decide, la persona aprueba.

Lo que traigo de la bioseguridad resulta que se aplica igual acá: trazabilidad, control de acceso, contención, procedimientos escritos, y la costumbre de asumir que las cosas van a fallar.

---

## Proyecto principal

### [praxia-ops](https://github.com/bioqruizdiazaldo-cmd/praxia-ops) — plataforma de agentes de IA en producción

Documentación completa, sanitizada y verificable de un sistema real.

| | |
|---|---|
| Agentes en producción | 1 orquestador + 15 subagentes |
| Workflows n8n registrados / activos | 217 / 25 |
| Migraciones SQL versionadas | 33+ |
| Casos de test automatizados | 554 |
| Endpoints de API | 60+, ninguno `DELETE` |
| Herramientas MCP | 22, en 4 scopes OAuth |

**Adentro vas a encontrar:**

- Un [manual de usuario](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/00-manual-de-usuario) de 9 capítulos.
- Un [desglose de criterios de decisión](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/02-desglose-tecnico): cuándo va en SQL, cuándo en n8n, cuándo amerita un subagente, cuándo un MCP, cuándo una API propia, cuándo una pantalla.
- [9 ADRs](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/04-decisiones), incluido el de un buscador que **no** se publicó porque dio 2 de 7 pruebas.
- [Runbooks e incidentes reales](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/06-runbooks): un PDF de 21,9 MB que rompió el pipeline, y cinco días de drift entre repositorio y servidor.
- Un [método de trabajo con agentes de IA](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/05-gobernanza) — SDLC, plantillas y checklists — reutilizable en cualquier equipo. También [en inglés](https://github.com/bioqruizdiazaldo-cmd/praxia-ops/tree/main/docs/05-gobernanza/en).

---

## Stack

**Orquestación** n8n self-hosted · Model Context Protocol (MCP) · OpenAI (chat, Whisper, TTS)
**Datos** PostgreSQL 16 · SQL como contrato: triggers, funciones, vistas, roles sin `DELETE`
**Runtime** Docker · Traefik + TLS · VPS propio · backups con verificación y rollback
**Backend** Node.js ESM · OpenAPI 3.1 · OAuth 2.0 + PKCE
**Interfaces** Telegram (texto, voz, imagen, PDF) · dashboard web · MCP para agentes externos
**Integraciones** Gmail · Google Calendar, Drive y Sheets · Tavily · Europe PMC · OpenAlex · RSS
**Método** ADRs · manifiestos de workflow · canary · post-mortems blameless · `node --test` + PGlite

---

## Cómo trabajo

> **Sin orden no hay sistema, solo experimentos.**

1. **Planificación antes que implementación.** Siempre. El error caro casi nunca es técnico: es de secuencia.
2. **Inspección no equivale a autorización de cambio.** Un agente puede leer todo; escribir necesita permiso explícito.
3. **La ausencia de dato no se convierte en un dato inventado.** Si no hay evidencia, se declara el vacío.
4. **La aprobación humana no es un trámite.** Mandar un mail, gastar, borrar o publicar pasan por una persona.
5. **Todo despliegue tiene rollback verificado.** Si no se puede volver atrás, no se sube.

---

## Sobre publicar los fracasos

En [praxia-ops](https://github.com/bioqruizdiazaldo-cmd/praxia-ops) están documentados los incidentes, el drift, los 73 workflows de laboratorio que quedaron conviviendo con producción y el buscador que no pasó la validación.

Están ahí a propósito. Un sistema que solo muestra sus éxitos no está documentado: está publicitado.

---

<p align="center">
  <sub>Toda la documentación pública está sanitizada. El runtime, las credenciales y los datos reales viven en infraestructura privada.</sub>
</p>
