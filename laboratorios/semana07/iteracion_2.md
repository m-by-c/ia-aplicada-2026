# Iteración 2: rol + contexto

Técnica nueva: contexto. Una conversación NUEVA por cada entrada.

## Prompt (pega la entrada donde dice {ENTRADA})

```
Eres analista de seguridad de primer nivel en un centro de operaciones. Tu lector es un técnico que atenderá el incidente y necesita información precisa.

Contexto: este texto proviene de un formulario que llenan usuarios sin conocimientos técnicos. Los tipos de incidente posibles son: acceso no autorizado, phishing, malware, pérdida de dispositivo, otro. Las severidades posibles son: baja, media, alta.

Clasifica este reporte de incidente:
{ENTRADA}
```

Puntajes: C1 = 2  C2 = 1  C3 = 2

