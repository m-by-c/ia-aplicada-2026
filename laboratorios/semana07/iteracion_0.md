# Iteración 0: línea base (zero-shot)

Técnica: ninguna. Una conversación NUEVA por cada entrada.

## Prompt (pega la entrada donde dice {ENTRADA})

```
Clasifica este reporte de incidente:
{"Hola, creo que alguien entró a mi correo porque me llegó un aviso raro. No sé desde cuándo. Ya cambié la contraseña. ¿Qué hago?"
}
```

## Respuesta a la entrada 1

**Clasificación del reporte**

- **Tipo:** Posible compromiso de cuenta de correo (acceso no autorizado)
- **Categoría:** Seguridad de la información / Cuenta comprometida
- **Severidad:** Alta. El correo suele ser la llave de recuperación de otras cuentas (banco, redes sociales, compras).
- **Estado:** Sospecha sin confirmar. No hay evidencia del alcance, y el momento de la intrusión es desconocido.
- **Contención:** Parcial. Cambió la contraseña, pero eso no basta si el atacante dejó otras puertas abiertas.
- **Prioridad de atención:** Inmediata

**Qué hacer ahora**

1. **Revisa la actividad reciente de la cuenta.** En Gmail: *Administrar tu cuenta de Google → Seguridad → Tus dispositivos / Actividad reciente*. En Outlook: *Seguridad → Actividad de inicio de sesión*. Cierra todas las sesiones que no reconozcas.
2. **Activa la verificación en dos pasos**, de preferencia con app autenticadora o llave de seguridad en vez de SMS.
3. **Revisa la configuración del correo**, que es donde los atacantes suelen dejar rastros:
   - Reglas o filtros que reenvíen o borren mensajes automáticamente
   - Direcciones de reenvío que no pusiste tú
   - Apps o accesos de terceros conectados
   - Correo y teléfono de recuperación (confirma que sean tuyos)
4. **Cambia contraseñas en cadena**, empezando por banco, tiendas en línea y redes sociales. Usa contraseñas únicas en cada una, idealmente con un gestor de contraseñas. Si usabas la misma contraseña del correo en otros sitios, cámbiala en todos.
5. **Revisa tu bandeja de enviados y la papelera** por mensajes que no escribiste o que fueron borrados, y busca correos de "restablecer contraseña" o "nuevo inicio de sesión" de otros servicios.
6. **Vigila tus cuentas bancarias** y activa alertas de movimientos. Si ves algo raro, avisa a tu banco de inmediato.
7. **Cuidado con el aviso que recibiste.** Si fue un correo pidiéndote entrar a un enlace, no vuelvas a abrirlo. Para verificar, entra directamente al sitio oficial escribiendo la dirección tú mismo. Revisa también tu equipo con un antivirus por si hubo malware.
8. **Avisa a tus contactos** si detectas que se enviaron mensajes desde tu cuenta, para que no abran enlaces sospechosos.

Si me dices qué proveedor usas (Gmail, Outlook, Yahoo, etc.) y qué decía el aviso raro, puedo darte los pasos exactos y ayudarte a saber si fue un intento real o phishing.

Puntajes: C1 = 1  C2 = 1  C3 = 1  Observación: 3

## Respuesta a la entrada 2
**Clasificación del reporte**

| Campo | Valoración |
|---|---|
| **Tipo de incidente** | Posible compromiso de cuenta (acceso no autorizado a correo electrónico) |
| **Categoría** | Cuenta / identidad, posible *phishing* o robo de credenciales |
| **Severidad** | **Media-Alta** (provisional) |
| **Confianza del reporte** | Baja: el indicio es un "aviso raro" no especificado |
| **Estado** | Contención parcial (cambio de contraseña) |
| **Prioridad de atención** | Alta: atender hoy |

**Por qué esa severidad:** el correo suele ser la llave de recuperación de otras cuentas (banco, redes, servicios), así que un compromiso real tiene impacto en cadena. Se sube de "media" a "media-alta" porque el tiempo de exposición es desconocido ("no sé desde cuándo"). Bajaría a media si el aviso resulta ser un correo de *phishing* que el usuario no llegó a abrir o contestar.

**Información faltante para confirmar:**
- ¿Qué decía el aviso y quién lo envió (dirección real del remitente)?
- ¿Hizo clic en enlaces o ingresó su contraseña en alguna página?
- ¿Usa esa contraseña en otros servicios?
- ¿Tiene verificación en dos pasos activada?
- ¿Qué proveedor de correo es (Gmail, Outlook, corporativo)?
- ¿Es correo personal o de trabajo? (si es de trabajo, hay que escalar al área de TI)

**Qué debe hacer ahora (respuesta al usuario):**
1. **Activar la verificación en dos pasos**, de preferencia con app autenticadora o llave física en lugar de SMS.
2. **Cerrar todas las sesiones activas** y revisar los dispositivos conectados desde la configuración de seguridad de la cuenta.
3. **Revisar reglas de reenvío, filtros y direcciones de recuperación**: los atacantes suelen dejar un reenvío automático oculto.
4. **Revisar el historial de actividad reciente** (inicios de sesión, ubicaciones, horas desconocidas) y la carpeta de enviados y papelera.
5. **Cambiar la contraseña en otras cuentas** donde la haya reutilizado, empezando por banco y redes sociales, y usar un gestor de contraseñas.
6. **Revisar el aviso con cuidado:** no abrir enlaces ni adjuntos; si es de una empresa, entrar escribiendo la dirección a mano.
7. **Avisar a sus contactos** si se enviaron mensajes sospechosos desde su cuenta.
8. Si hay indicios de uso fraudulento (cargos, suplantación), **reportar a la policía cibernética** de su localidad o a su banco.

**Siguiente paso para el analista:** pedir el correo del aviso (con encabezados completos) y la captura del historial de accesos para pasar de "sospecha" a incidente confirmado o falsa alarma.

Puntajes: C1 = 2  C2 = 1  C3 = 2  Observación: 5

## Respuesta a la entrada 3
## Clasificación del incidente

| Campo | Valoración |
|---|---|
| **Tipo de incidente** | Posible compromiso de cuenta de correo (Account Takeover / acceso no autorizado) |
| **Vector probable** | Phishing o credenciales robadas/reutilizadas (por confirmar) |
| **Estado** | Sospechado, no confirmado |
| **Severidad inicial** | **Alta** (provisional) |
| **Prioridad** | **P2**, escalable a **P1** si se confirma acceso real |
| **Categoría** | Seguridad de identidad / Correo electrónico |
| **Fuente del reporte** | Interna (empleado), de buena fe y oportuno |

## Justificación

- **Alta, no crítica:** en una empresa grande, un buzón comprometido puede exponer información confidencial, permitir suplantación (BEC) y servir de punto de apoyo para moverse lateralmente. Aún no hay evidencia confirmada de acceso ni de exfiltración, por eso se mantiene en alta y no en crítica.
- **Incertidumbre importante:** el empleado no sabe desde cuándo ni qué aviso recibió. Podría ser una alerta legítima de inicio de sesión inusual o un correo de phishing. Esto debe verificarse primero.
- **Contención parcial:** cambió la contraseña, lo cual es positivo, pero no basta. Si el atacante creó reglas de reenvío, tokens OAuth o sesiones activas, puede mantener acceso.

## Información faltante (a solicitar al empleado)

1. ¿Qué decía exactamente el aviso, quién lo envió y cuándo? (pedir captura o reenvío como adjunto)
2. ¿Hizo clic en enlaces o abrió adjuntos del aviso? ¿Ingresó credenciales en algún sitio?
3. ¿Cambió la contraseña desde un dispositivo de confianza?
4. ¿Tiene MFA activado? ¿Recibió solicitudes de aprobación que no inició?
5. ¿Reutiliza esa contraseña en otros servicios?

## Acciones recomendadas para el equipo de seguridad

**Inmediatas (primeras horas)**
- Revocar todas las sesiones activas y tokens de actualización de la cuenta.
- Revisar registros de inicio de sesión (IPs, ubicaciones, dispositivos, user agents) de los últimos 30 a 90 días.
- Buscar reglas de bandeja de entrada sospechosas, reenvíos automáticos, delegados y aplicaciones OAuth autorizadas.
- Confirmar o forzar MFA resistente a phishing.
- Analizar el correo del aviso (cabeceras, URLs, adjuntos) y buscar si otros empleados lo recibieron.

**Contención y alcance**
- Bloquear dominios, URLs y remitentes maliciosos en el gateway de correo y el proxy.
- Revisar correos enviados desde la cuenta y accesos a recursos conectados (SharePoint, VPN, SSO).
- Si hay evidencia de acceso no autorizado, elevar a P1 y activar el proceso formal de respuesta a incidentes.
- Evaluar obligaciones de notificación si se expuso información sensible o datos personales.

**Cierre**
- Documentar la línea de tiempo, causa raíz y lecciones aprendidas.
- Recordar al empleado reportar rápido y no reutilizar contraseñas.

## Respuesta sugerida al empleado

> Gracias por reportarlo tan pronto, fue lo correcto. No hagas clic en nada más del aviso ni lo borres; reenvíalo como adjunto al equipo de seguridad. Mientras investigamos, no uses esa contraseña en otros servicios y avísanos si ves actividad extraña (correos enviados que no reconoces, solicitudes de MFA inesperadas). Te contactaremos con los siguientes pasos.

Si quieres, puedo adaptar esta clasificación a un marco específico (NIST 800-61, MITRE ATT&CK, la matriz de severidad de tu empresa) o convertirla en una plantilla de ticket.

Puntajes: C1 = 5  C2 = 3  C3 = 4  Observación: 12

## Total de la iteración: 12 / 18
