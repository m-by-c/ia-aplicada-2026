Documento técnico preliminar (v1)

Proyecto: Detección de incendios en edificios inteligentes · Sección: Introducción, alcance y requisitos

1. Introducción
   
El proyecto Detección de incendios en edificios inteligentes tiene como objetivo contribuir a la detección temprana de humo mediante inteligencia artificial de tipo. La solución está dirigida a los inquilinos de edificios inteligentes y emite una alerta ante una detección de humo en un tiempo máximo de 1 minuto. El sistema no almacena direcciones ni datos personales, conforme a la política de datos del proyecto.

3. Alcance
Incluye:
• Modelo de IA que clasifica humo / no humo.
• Alerta a los inquilinos ante una detección de humo.
No incluye:
• Recopilación, almacenamiento o divulgación de direcciones y datos personales.
Decisiones de alcance pendientes:
• Integración con sistemas de alarmas y sensores existentes.
• Activación automática de sistemas de extinción de incendios.

5. Requisitos funcionales
   
1. RF-1: El sistema deberá clasificar imágenes o señales de entrada como humo / no humo mediante inteligencia artificial.
2. RF-2: El sistema deberá enviar una alerta cuando la probabilidad de humo supere (dato a definir).
3. RF-3: El sistema deberá emitir la alerta en un máximo de 1 minuto.
4. RF-4: El sistema deberá notificar a los inquilinos mediante un sonido.
5. RF-5: El sistema no deberá de revelar datos personales.

4. Requisitos no funcionales
   
• RNF-1 – Privacidad: El sistema no deberá almacenar ni divulgar direcciones ni datos personales de los inquilinos.
• RNF-2 – Confiabilidad: El sistema deberá alcanzar una precisión mínima de 1 minuto.
• RNF-3 – Disponibilidad: El sistema deberá estar disponible al menos del tiempo designado.

Declaración de generación asistida

• Modelo usado: ChatGPT
• Fecha: 1 de noviembre de 2026
• Prompt usado: el del Paso 1.1 del laboratorio ("Eres redactor técnico. Escribe la sección 'Introducción, alcance y requisitos'…"), completado con los datos de la ficha del proyecto. [DATO PENDIENTE: pegar el prompt completo tal como lo enviaste]
• Correcciones aplicadas: 12 (hallazgos 1 a 12 de la tabla de auditoría). Los hallazgos 13 y 14 eran marcadores correctos y se conservaron.
• Nota: el borrador original se conserva sin editar en documento_tecnico_borrador.md.
