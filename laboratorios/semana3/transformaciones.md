| Columna original | Qué le hiciste (eliminar, seudonimizar, generalizar, enmascarar, conservar) | Técnica | Por qué |
|---|---|---|---|
| id | Conservar | - | Es solo un índice interno de la tabla, no identifica a nadie por sí mismo |
| nombre | Seudonimizar | Código P001-P036 asignado | Identificador directo pero el análisis de patrones de acceso necesita agrupar a una misma persona sin exponer quién es |
| correo | Eliminar | Se quitó la columna completa | Identificador directo y no aporta nada al análisis de patrones de acceso |
| telefono | Eliminar | Se quitó la columna completa | Mismo motivo que correo |
| fecha_acceso | Generalizar | Número de semana equivalente del año | La fecha exacta combinada con hora y área podía exponer demasiado quién estuvo dónde y cuándo |
| hora_entrada | Generalizar | Franja horaria | Mismo motivo que fecha_acceso |
| area | Conservar | - | Es la variable que el análisis de patrones necesita para comparar y generalizar |
| empresa | Generalizar | Tipo de empresa | Nombre exacto es un identificador indirecto por agrupar sectores |
| motivo | Conservar | - | Categoría de actividad |



| id | campo | problema | valor_original | accion |
|---|---|---|---|---|
| 3 | telefono | Ya venía vacío en los datos originales (dato faltante, no un error de captura) | (vacío) | Se mantuvo vacío |
| 5 | correo y hora | Correo sin dominio, dato no recuperable. Fuera de horario laboral | pedro.salgado@correo | Vaciado |
| 6 | empresa | Ya venía vacío en los datos originales (dato faltante, no un error de captura) | (vacío) | Se mantuvo vacío |
| 7 | fecha_acceso | Fecha inválida: mes 13 no existe, dato no recuperable | 2026-13-04 | Vaciado |
| 9 | hora | Fuera de horario laboral | 23:40 | Se mantuvo el dato |
| 20 | fecha_acceso | Fecha inválida: día 32 no existe, dato no recuperable | 2026-09-32 | Vaciado |
| 21 | correo | Correo sin dominio, dato no recuperable | alejandro.cortes@correo | Vaciado |
| 25 | telefono | Teléfono con 9 dígitos (menos de 10), dato no recuperable | 551122334 | Vaciado |
| 30 | empresa | Ya venía vacío en los datos originales (dato faltante, no un error de captura) | (vacío) | Se mantuvo vacío |
| 31 | telefono | Ya venía vacío en los datos originales (dato faltante, no un error de captura) | (vacío) | Se mantuvo vacío |
| 32 | empresa | Ya venía vacío en los datos originales (dato faltante, no un error de captura) | (vacío) | Se mantuvo vacío |
| 33 | hora | Fuera de horario laboral | 5:30 | Se mantuvo el dato |
| 34 | hora | Fuera de horario laboral | 22:45 | Se mantuvo el dato |
| 35 | hora | Fuera de horario laboral | 23:10 | Se mantuvo el dato |
