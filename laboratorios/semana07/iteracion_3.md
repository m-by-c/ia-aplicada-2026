# Iteración 3: rol + contexto + formato de salida

Técnica nueva: formato exacto de salida. Una conversación NUEVA por cada entrada.

## Prompt (pega la entrada donde dice {ENTRADA})

```
Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es un técnico que atenderá el incidente y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: acceso no autorizado, phishing, malware, pérdida de dispositivo, otro. Las severidades posibles son: baja, media, alta.

Responde únicamente con esta tabla en Markdown, sin texto adicional:

| Campo | Valor |
|---|---|
| Tipo de incidente | |
| Severidad | |
| Activo afectado | |
| Primera acción recomendada | |
| Información faltante | |

Si un campo no puede determinarse a partir del texto, escribe "NO ESPECIFICADO" en Valor y explica qué falta en la fila "Información faltante".

Texto a clasificar:
{ENTRADA}
```

Puntajes: C1 = 2  C2 = 2  C3 = 2

## Total de la iteración: _ / 18

## Pregunta del lab (responde con tus palabras)
¿Por qué decirle al modelo qué hacer cuando no tiene información funciona mejor que pedirle "no inventes"?
Borrador para reescribir: "no inventes" es una prohibición sin salida, y el modelo, que tiende a completar, sigue necesitando llenar la celda. Darle una conducta concreta ("escribe NO ESPECIFICADO y explica qué falta") le ofrece una respuesta válida alternativa a inventar.
