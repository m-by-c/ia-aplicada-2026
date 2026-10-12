# Tablas del laboratorio: tokens, temperatura y ventana de contexto

## 1. Tokens frase (Parte 1)

| tokens | characters |
|---|---|
| 9 | 63 |

## 2. Español 1.2

| tokens | characters |
|---|---|
| 9 | 63 |

## 3. Inglés 1.2

| tokens | characters |
|---|---|
| 7 | 54 |

## 4. Caracteres por token

| Texto | Idioma | Caracteres | Tokens | Caracteres por token |
|---|---|---|---|---|
| Frase corta | Español | 93 | 15 | 4.6 |
| Frase corta | Inglés | 92 | 15 | 6.1 |
| Párrafo de 100 palabras | Español | 691 | 132 | 3.6 |
| Párrafo de 100 palabras | Inglés | 640 | 110 | 4.9 |

## 5. Respuestas por temperatura

| Temperatura | Ejecución | Respuesta | ¿Identifica a la anterior? |
|---|---|---|---|
| 0 | 1 | Barrera de seguridad que filtra el tráfico de red para proteger un sistema de accesos no autorizados. | No aplica |
| 0 | 2 | Un firewall actúa como una barrera entre una red interna confiable (como la de tu casa o empresa) y una red externa no confiable (como Internet). Su función principal es inspeccionar cada paquete de datos que intenta entrar o salir y, basándose en un conjunto de reglas de seguridad preestablecidas, decidir si permite el paso o lo bloquea para evitar ataques o accesos no permitidos. | No |
| 0 | 3 | Es una barrera de seguridad que filtra el tráfico de red para proteger un sistema de accesos no autorizados. | Similar a la primera |
| 0.7 | 1 | Es un sistema de seguridad que filtra el tráfico de red para prevenir accesos no autorizados. | No aplica |
| 0.7 | 2 | Es un sistema de seguridad que filtra el tráfico de red para prevenir accesos no autorizados. | Si |
| 0.7 | 3 | Es una barrera de seguridad que filtra el tráfico de red para prevenir accesos y amenazas no autorizadas. | No |
| 1.5 | 1 | Es una barrera de seguridad que filtra el tráfico de red para proteger un sistema de accesos no autorizados. | No aplica |
| 1.5 | 2 | Se trata de un Firewall (también conocido en español como Cortafuegos).<br><br>Aquí te explico brevemente cómo funciona:<br><br>1. Punto de control: Actúa como una barrera situada entre una red interna (confiable, como la de tu casa o empresa) y una red externa (no confiable, como Internet).<br>2. Filtrado de paquetes: Examina los datos que intentan entrar o salir de la red (llamados "paquetes").<br>3. Reglas de seguridad: Utiliza un conjunto de reglas predefinidas para decidir si permite el paso de un paquete o si lo bloquea. Por ejemplo, puede bloquear el acceso desde una dirección IP sospechosa o impedir que un programa no autorizado envíe datos hacia afuera.<br>4. Prevención: Su objetivo principal es evitar que atacantes, malware o accesos no autorizados penetren en el sistema y comprometan la información.<br><br>Existen principalmente dos tipos:<br><br>- Firewall de software: Se instala directamente en un dispositivo (como el que viene integrado en Windows o macOS).<br>- Firewall de hardware: Es un dispositivo físico independiente que se coloca entre el router y la red para proteger todos los dispositivos conectados. | No |
| 1.5 | 3 | Barrera de seguridad que filtra el tráfico de red para proteger un sistema de accesos no autorizados. | No |

## 6. Variabilidad 2.3

| Temperatura | Palabras distintas en total | Respuestas idénticas entre sí |
|---|---|---|
| 0 | 0.55 | 0 (la 1 y 3 son similares) |
| 0.7 | 20 | 1 (la 1 y 3 son idénticas) |
| 1.5 | 112 | 0 |

## 7. Métricas del documento

| Métrica | Valor estimado |
|---|---|
| Palabras del documento | 1,980 |
| Caracteres estimados | 11,100 |
| Tokens estimados | 3,500 - 3,900 aprox |
| Páginas | 4 |

## 8. Satura contexto 3.3

| Intento | Copias del documento | Tokens aproximados | Respuestas del modelo | ¿Correcta? |
|---|---|---|---|---|
| 1 | 1 | 3,900 aprox | AZUL-7342 | Si |
| 1 | 2 | 7,800 aprox | AZUL-7342 | Si |
| 1 | 3 | 11,700 aprox | AZUL-7342 | Si |
| 1 | 4 | 15,600 aprox | AZUL-7342 | Si |
| 1 | 5 | 19,500 aprox | Sé rechazó el texto | No aplica |

## 9. Posición aguja 3.4

| Posición de la aguja | Respuesta | ¿Es correcta? |
|---|---|---|
| Inicio | AZUL-7342 | Si |
| Mitad | No aparece | No |
| Final | AZUL-7342 | Si |
