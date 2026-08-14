# Ficha de proyecto — Detección de Requerimientos y Minutas con IA

*Documento vivo. Se completa clase a clase — es tu model card en versión de borrador. Súbelo a tu repo como `docs/ficha_proyecto.md`.*

## 1. Nombre interno del proyecto

**"Panel de Seguimiento IA"** — Automatización administrativa de detección de requerimientos de clientes y generación de minutas de reunión

## 2. Problema (2-3 frases)

Un equipo operativo/administrativo debe revisar manualmente cada correo, mensaje de WhatsApp Business y reunión para identificar qué necesita cada cliente, distinguiendo mensajes con una solicitud real de mensajes de cortesía — un proceso repetitivo y propenso a que algo quede sin responsable o sin seguimiento. Además, los acuerdos tomados en reuniones (quién es responsable de qué y para cuándo) rara vez quedan documentados de forma sistemática, generando pérdida de trazabilidad.

## 3. Usuario / cliente objetivo

Equipo operativo o administrativo de una organización que gestiona múltiples clientes y proyectos por distintos canales (correo, WhatsApp, reuniones) y que hoy no tiene un punto único donde ver pendientes, estado y fechas límite, ni una forma automática de documentar acuerdos de reunión.

## 4. Tipo de modelo que vas a necesitar

- [ ] Generativo (crea contenido nuevo: texto, imagen, audio, video)
- [ ] Analítico (clasifica, predice, extrae)
- [x] Ambos (pipeline combinado)

*Analítico: clasificación rápida de mensajes (solicitud real vs. cortesía) por cliente, proyecto y urgencia. Generativo: razonamiento sobre transcripciones extensas de reuniones para generar el borrador editable de la minuta (acuerdos, responsables, próximos pasos).*

## 5. Modelos candidatos (2-3 concretos)

1. **Gemini Flash** — clasificación rápida de mensajes entrantes (correo, WhatsApp) por urgencia y tipo de solicitud.
2. **Gemini Pro** — razonamiento sobre transcripciones extensas de reuniones para generar minutas.
3. **Google AI Studio** como entorno de prototipado de ambos modelos en un solo flujo.

## 6. Roadmap del proyecto (se completa clase a clase)

- [ ] Clase 23 — Datasheet del dataset (`docs/datasheet_v1.md`)
- [ ] Clase 24 — Hallazgos NotebookLM (`docs/hallazgos_notebooklm.md`)
- [ ] Clase 25 — System prompt (`docs/system_prompt_v3.md`)
- [ ] Clase 26 — Modelos HF candidatos (`docs/modelos_hf_candidatos.md`)
- [ ] Clase 27 — Sistema visual (`docs/sistema_visual.md`)
- [ ] Clase 28 — Arquitectura del agente (`docs/arquitectura_agente.md`)
- [ ] Clase 29 — Video generativo (`docs/video_generativo.md`)
- [ ] Clase 30 — Casos de uso Hermes (`docs/hermes_casos_uso.md`)
- [ ] Clase 31 — Antigravity Loop + cierre (`docs/antigravity_loop.md`)

## 7. Notas para Mauricio (Unidad 4)

Funcionalidades ya implementadas en el prototipo (Google AI Studio):

- Dashboard único con todos los pendientes de clientes y compromisos de reuniones (estado: pendiente/en proceso/atendido + fecha límite).
- Simulador de ingesta de mensajes para probar en tiempo real la clasificación (solicitud urgente vs. mensaje irrelevante).
- Editor interactivo de minutas para revisar y ajustar antes de compartir.
- Alertas proactivas para pendientes por vencer o sin responsable asignado.
- Módulo de integraciones pensado para Calendar, Trello o Asana (evitar duplicar seguimiento).
- Historial y auditoría trazable por cliente, proyecto o fecha.
- Control de acceso por roles (Administrador, Operativo, Auditor) para proteger datos de clientes y conversaciones de negocio.

Punto clave para la próxima unidad: es un prototipo conceptual/funcional, no productivo — falta definir integración real con las herramientas externas (Calendar, Trello, Asana) y el manejo de datos sensibles de clientes en producción.
