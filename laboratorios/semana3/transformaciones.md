| Tipo de error | Introducidos | Detectados por mi limpieza | Faltaron | Por qué faltaron |
|---|---|---|---|---|
| Fila duplicada exacta | 3 pares (1 original: filas 1/4 + 2 nuevos: 13/14, 15/16) | 0 | 3 pares | No estaban en la lista de tipos que se pidió corregir/marcar en ese paso (solo se pidió fecha, teléfono y correo). Se mencionaron aparte en el texto, pero nunca se procesaron ni se registraron en la pestaña de incidencias. |
| Fecha en formato distinto (dd/mm/aaaa) | 4 (1 original: fila 2 + 3 nuevos: 17, 18, 19) | 4 | 0 | — |
| Fecha inválida (mes 13, día 32) | 2 (1 original: fila 7 + 1 nuevo: 20) | 2 | 0 | — |
| Correo sin dominio o con mayúsculas | 5 (2 originales: filas 2, 5 + 3 nuevos: 21, 22, 23) | 5 | 0 | — |
| Teléfono con espacios o <10 dígitos | 4 (1 original: fila 2 + 3 nuevos: 24, 25, 26) | 4 | 0 | — |
| Área con distinta capitalización | 4 (1 original: fila 2 + 3 nuevos: 27, 28, 29) | 0 | 4 | Mismo motivo que los duplicados: no venía en la lista explícita de ese paso. |
| Celda vacía en empresa o teléfono | 5 (2 originales: filas 3, 6 + 3 nuevos: 30, 31, 32) | 5 | 0 | — |
| Hora fuera de horario laboral | 4 (1 original: fila 9 + 3 nuevos: 33, 34, 35) | 4 (reconocidas y dejadas intactas a propósito) | 0 | — |

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
