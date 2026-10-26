# Plantilla: clasificación de incidente v1
# Variables: {ROL_LECTOR}, {CATEGORIAS}, {SEVERIDADES}, {ENTRADA}

Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es {ROL_LECTOR} y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: {CATEGORIAS}. Las severidades posibles son: {SEVERIDADES}.

Ejemplo de entrada:
"Recibí un correo del banco pidiendo que confirme mi tarjeta en un enlace. Di clic y puse mis datos. Fue hoy a las 10 am desde la laptop de la oficina."

Ejemplo de salida:

| Campo | Valor |
|---|---|
| Tipo de incidente | phishing |
| Severidad | alta |
| Activo afectado | credenciales bancarias del usuario; laptop de oficina |
| Primera acción recomendada | contactar al banco para bloquear la tarjeta y reportar al área de seguridad |
| Información faltante | ninguna |

Antes de la tabla, escribe una sección titulada "Análisis" con tres viñetas: qué información explícita hay en el texto, qué se puede inferir con seguridad y qué no se puede determinar. Después escribe la tabla en Markdown con estos campos:

| Campo | Valor |
|---|---|
| Tipo de incidente | |
| Severidad | |
| Activo afectado | |
| Primera acción recomendada | |
| Información faltante | |

Si un campo no puede determinarse a partir del texto, escribe "NO ESPECIFICADO" en Valor y explica qué falta en la fila "Información faltante". No agregues texto fuera de la sección "Análisis" y la tabla.

Texto a clasificar:
{ENTRADA}

---

## Instrucciones de uso

- {ROL_LECTOR}: quién leerá la respuesta. Ejemplo: "un técnico que atenderá el incidente".
- {CATEGORIAS}: lista cerrada de tipos. Ejemplo: "acceso no autorizado, phishing, malware, pérdida de dispositivo, otro".
- {SEVERIDADES}: escala cerrada. Ejemplo: "baja, media, alta".
- {ENTRADA}: el texto libre del usuario, sin editar.
- Modelo probado: [COMPLETAR: ChatGPT / Gemini / Deepseek y versión].
- Puntaje obtenido: [COMPLETAR] / 18 en las tres entradas; entrada de robustez: [COMPLETAR] / 6.
- Limitaciones conocidas: [COMPLETAR con lo que observaste; por ejemplo, el ejemplo few-shot puede sesgar hacia "phishing", y el texto de "Análisis" antes de la tabla impide copiar la respuesta directo a un sistema].
- Úsala en una conversación nueva por cada reporte.
