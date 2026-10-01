[politica_datos_proyecto.md]
# Política de datos del proyecto Registro de Accesos

## 1. Alcance

Esta política cubre los siguientes datos, numerados según el inventario del proyecto:

- **D1 — nombre** (personal)
- **D2 — correo** (personal)
- **D3 — telefono** (personal)
- **D4 — fecha_acceso** (personal)
- **D5 — hora_entrada** (personal)
- **D6 — area** (no personal, identificador indirecto)
- **D7 — empresa** (no personal, identificador indirecto)
- **D8 — motivo** (no personal)
- **D9 — id** (no personal)

## 2. Ciclo de vida

El recorrido completo está documentado en `ciclo_vida_dato_proyecto.drawio` / `.png`. En resumen, el dato pasa por seis etapas: Captura (recepcionista), Almacenamiento (administrador de sistemas / proveedor de nube), Uso (analista de datos), Compartición (analista de datos, con un servicio de correo transaccional y un modelo generativo como terceros), Retención (oficial de cumplimiento) y Eliminación (administrador de sistemas). El dato D1 (nombre) sale por primera vez del control directo de la organización en la etapa de Almacenamiento, al residir en un proveedor de nube externo.

## 3. Normativa aplicable

El proyecto se evaluó contra tres marcos (ver `matriz_cumplimiento_proyecto.xlsx`): la Ley de IA de la Unión Europea (aplica de forma limitada, ya que este sistema no es de alto riesgo bajo el Anexo III, pero sus principios de transparencia y gobernanza de datos se adoptan como buena práctica), la LFPDPPP de México vigente desde el 20 de marzo de 2025 (aplica de forma obligatoria porque se tratan datos personales de personas físicas en México) y el NIST AI RMF (marco voluntario adoptado para estructurar la gestión de riesgo del análisis de patrones).

## 4. Controles comprometidos

- Publicar y mantener visible el aviso de privacidad — *Oficial de cumplimiento*
- Capturar solo los datos necesarios (sin pedir identificación oficial u otros datos extra) — *Líder del proyecto*
- Cifrar los datos en reposo y controlar el acceso por rol en la base de datos — *Administrador de sistemas*
- Seudonimizar el nombre y generalizar fecha/hora/empresa antes de cualquier análisis o envío a un modelo generativo — *Analista de datos*
- Nunca enviar correo ni teléfono a un modelo generativo o proveedor externo de análisis — *Analista de datos*
- Firmar un acuerdo de confidencialidad / encargado de tratamiento con el proveedor de nube — *Oficial de cumplimiento*
- Definir y respetar un plazo de retención de 12 meses, con revisión semestral — *Oficial de cumplimiento*
- Ejecutar borrado seguro y documentar cada eliminación en bitácora — *Administrador de sistemas*

## 5. Manejo de datos con herramientas de IA

**Nunca se ingresan a ChatGPT, Gemini, Deepseek, Dify u otra herramienta de IA generativa:** nombre, correo ni teléfono (D1, D2, D3) en su forma original, ni ninguna combinación de fecha+hora+área+empresa que pudiera volver a identificar a una persona.

**Sí pueden ingresarse** datos ya generalizados y seudonimizados: `id_persona` (código Pxxx), semana del año, franja horaria, área, tipo de empresa y motivo — siempre que se verifique primero que ninguna combinación de esas columnas identifica a una sola persona (ver reflexión de la Parte 6, pregunta 2).

Para pruebas o demostraciones que no requieran datos reales, se usarán datos ficticios generados a propósito, nunca un recorte del dataset real sin anonimizar.

## 6. Revisión

Esta política se revisará cada semestre, o antes si cambia el alcance del sistema (por ejemplo, si se automatizan decisiones sobre personas). La aprueba el responsable del proyecto en conjunto con el oficial de cumplimiento del equipo.
