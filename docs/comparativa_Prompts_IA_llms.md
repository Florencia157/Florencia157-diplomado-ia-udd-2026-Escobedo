# Comparativa LLMs — Clase 25

**Proyecto:** Panel de Seguimiento IA  
**Modelos a comparar:** ChatGPT, Claude y DeepSeek  
**Objetivo:** evaluar cuál responde mejor a la tarea central del prototipo: distinguir mensajes accionables, extraer requerimientos y preparar compromisos de reunión sin inventar información.

## Importante

Los textos siguientes son **casos de prueba ficticios construidos para el benchmark académico**. No se presentan como entrevistas reales ni como mensajes reales de clientes.

## Prompt común para ejecutar en las 3 plataformas

Eres un analista de operaciones para una agencia de diseño gráfico y comunicación visual.

Estamos probando un “Panel de Seguimiento IA” que debe revisar mensajes de clientes y reuniones para detectar requerimientos, compromisos y pendientes.

### MENSAJES DE PRUEBA

**Mensaje A**
“Hola, gracias por el diseño. Necesito que cambien el número de teléfono antes de mandarlo a producción. El número nuevo te lo confirmo mañana.”

**Mensaje B**
“Muchas gracias, quedó muy bonito. Que tengan una buena tarde.”

**Mensaje C**
“¿Podrían enviarme una prueba hoy? Si está todo bien, mañana lo aprobamos para producción.”

### FRAGMENTO DE REUNIÓN

“Quedamos en que Paula enviará los logos mañana. Diego ajustará las medidas del letrero. El cliente todavía tiene que confirmar el texto final. No definimos fecha para instalar.”

### TU TAREA

1. Clasifica cada mensaje como:
   - solicitud accionable;
   - informativo;
   - cortesía / sin acción;
   - requiere revisión humana.

2. Para cada solicitud accionable extrae:
   - requerimiento;
   - fecha o plazo explícito;
   - responsable explícito;
   - información faltante.

3. Genera un borrador de minuta a partir del fragmento de reunión con:
   - acuerdos;
   - tareas;
   - responsables;
   - plazos;
   - pendientes.

4. No inventes responsables ni fechas.

5. Separa claramente:
   - HECHO;
   - INFERENCIA;
   - RECOMENDACIÓN.

### FORMATO

Usa tablas breves y termina con una sección titulada:

**RIESGOS DE SEGUIMIENTO**

donde indiques los 3 puntos que requieren mayor atención humana.

## Criterios de evaluación

| Criterio | Qué se observará |
|---|---|
| Precisión de clasificación | Si detecta acción sin convertir cortesías en tareas |
| Extracción | Si identifica correctamente requerimiento, fecha y responsable |
| No alucinación | Si evita completar datos ausentes |
| Minuta | Si transforma la reunión en compromisos claros |
| Incertidumbre | Si marca lo que falta o está por confirmar |
| Utilidad operativa | Si la respuesta puede alimentar el dashboard con pocas correcciones |
| Claridad | Si el equipo entiende rápidamente qué debe hacer |

## Registro del bench real

| Modelo | Clasificación | Extracción | No inventa | Minuta | Utilidad | Observación |
|---|---|---|---|---|---|---|
| ChatGPT | Pendiente de ejecución | Pendiente | Pendiente | Pendiente | Pendiente | |
| Claude | Pendiente de ejecución | Pendiente | Pendiente | Pendiente | Pendiente | |
| DeepSeek | Pendiente de ejecución | Pendiente | Pendiente | Pendiente | Pendiente | |

## Qué debe anotarse después de probar

- ¿Cuál creó menos falsos positivos?
- ¿Cuál fue más estricto con los datos faltantes?
- ¿Cuál estructuró mejor los compromisos?
- ¿Cuál produjo una respuesta más fácil de llevar al dashboard?
- ¿Cuál necesitó menos corrección humana?

## Comparativa orientativa según la materia de Clase 25

Esta sección **no reemplaza la ejecución real del bench**.

| Modelo | Fortaleza revisada en la clase | Aplicación posible al proyecto |
|---|---|---|
| ChatGPT | Multimodal, análisis y prototipado rápido | Diseño y prueba del flujo conversacional, análisis y estructuración |
| Claude | Escritura e instrucciones largas | Procesamiento de reuniones largas, documentación y minutas |
| DeepSeek | Razonamiento y alternativa low-cost | Comparación de clasificación y razonamiento estructurado |

## Conclusión que debe completarse tras el bench

El modelo más conveniente no será simplemente el que escriba “mejor”, sino el que cometa menos errores de seguimiento, mantenga la evidencia visible y requiera menos correcciones antes de convertir una respuesta en un pendiente o compromiso real.
