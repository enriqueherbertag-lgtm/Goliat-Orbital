# Protocolo Failsafe - Modo Seguro y Recuperación

## Descripción

El protocolo failsafe es el conjunto de procedimientos automáticos que Goliat-Orbital ejecuta cuando detecta una anomalía grave: fallo de sistemas, pérdida de comunicación con Tierra, consumo anómalo de energía, o cualquier situación que ponga en riesgo la nave. Su objetivo es preservar la integridad de la nave, mantener las funciones esenciales, y establecer un enlace de emergencia para recibir instrucciones.

---

## Niveles de Anomalía

| Nivel | Descripción | Acción automática |
|:---|:---|:---|
| **Nivel 1 (Advertencia)** | Desviación menor de parámetros (ej: temperatura de compresor por encima de lo normal) | Reporte a Tierra, ajuste automático si es posible |
| **Nivel 2 (Degradado)** | Fallo de un sistema redundante (ej: falla un compresor, pero los otros cinco funcionan) | Aislamiento del sistema fallado, operación con sistemas restantes, reporte a Tierra |
| **Nivel 3 (Crítico)** | Fallo de un sistema no redundante (ej: pérdida de comunicación por banda X) | Conmutación automática al sistema de respaldo (banda S), reporte de emergencia |
| **Nivel 4 (Catastrófico)** | Fallo generalizado, pérdida de control, o amenaza de colisión | Modo seguro inmediato: apagado de sistemas no esenciales, activación de enlace de emergencia, espera de instrucciones |

---

## Secuencia de Modo Seguro

| Paso | Acción | Duración |
|:---|:---|:---|
| **1. Detección** | El cerebro de Goliat identifica una anomalía de nivel 3 o 4 | Milisegundos |
| **2. Aislamiento** | Se desconectan los sistemas no esenciales (ej: horno, compactador) | Segundos |
| **3. Orientación** | La nave se orienta para maximizar la captura de energía (si aplica) y apuntar la antena omnidireccional a Tierra | Minutos |
| **4. Activación de enlace** | Se activa el transceptor banda S, se envía un paquete de emergencia con el estado de la nave | Segundos |
| **5. Espera** | La nave entra en modo de bajo consumo, solo mantiene sistemas vitales y escucha comandos | Indefinido |

---

## Paquete de Emergencia (Beacon)

| Campo | Descripción | Tamaño |
|:---|:---|:---|
| ID de la nave | Identificador único | 32 bits |
| Timestamp | Tiempo del evento | 64 bits |
| Nivel de anomalía | 1-4 | 8 bits |
| Posición | Latitud, longitud, altitud | 3 × 64 bits |
| Velocidad | Vector de velocidad orbital | 3 × 64 bits |
| Estado de sistemas | Resumen de estado (batería, compresores, horno, etc.) | 256 bits |
| Mensaje de error | Código del error | 128 bits |
| Checksum | Verificación de integridad | 32 bits |

**Tamaño total:** ~ 1 kbit. Se transmite repetidamente en banda S hasta que se recibe confirmación.

---

## Recuperación desde Tierra

| Paso | Acción | Tiempo estimado |
|:---|:---|:---|
| **1. Recepción del beacon** | Estación terrestre recibe el paquete de emergencia | Segundos a minutos (depende de la posición) |
| **2. Análisis** | Operadores evalúan el estado de la nave | Minutos |
| **3. Decisión** | Se determina el curso de acción (reparación remota, reingreso, espera) | Minutos a horas |
| **4. Envío de comandos** | Se transmiten los comandos de recuperación vía banda S | Segundos |
| **5. Ejecución** | El cerebro de Goliat ejecuta los comandos | Segundos a minutos |

---

## Automatización del Failsafe

| Evento | Acción automática |
|:---|:---|
| **Pérdida de comunicación por banda X** | Conmutar a banda S, enviar beacon cada 10 minutos |
| **Pérdida total de comunicación (banda X y S)** | Entrar en modo seguro, orbitar pasivamente, reactivar enlace cada 24 horas para escuchar |
| **Sobrecalentamiento del horno** | Apagar horno, abrir compuertas de enfriamiento, reportar |
| **Atasco en compactador** | Detener compactador, revertir ciclo, reportar |
| **Colisión inminente** | Encender propulsores de hidracina para evasión, reportar |
| **Fallo de dos compresores** | Aislar las branquias afectadas, operar con las restantes, reportar |
| **Consumo energético anómalo** | Aislar sistemas no esenciales, priorizar comunicación y captura |

---

## Redundancia en el Failsafe

| Sistema | Redundancia | Función en modo seguro |
|:---|:---|:---|
| **Computador principal** | Computador secundario idéntico | Si el principal falla, el secundario toma el control |
| **Memoria** | Almacenamiento no volátil con copia del sistema base | Si la memoria se corrompe, se reinicia desde la copia |
| **Comunicaciones** | Banda X y banda S | Si falla banda X, banda S sigue operando |
| **Energía** | Baterías de respaldo | Si falla la generación, las baterías dan tiempo para entrar en modo seguro |
| **Actuadores** | Múltiples compresores, ruedas de reacción, propulsores | Si falla uno, los otros pueden mantener funciones básicas |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|:---|
| **Autonomía** | La nave detecta y responde a anomalías sin esperar instrucciones de Tierra |
| **Redundancia** | Múltiples sistemas de respaldo; no hay punto único de fallo |
| **Comunicación garantizada** | Banda S mantiene enlace incluso en emergencia |
| **Recuperación remota** | La mayoría de las anomalías se pueden resolver desde Tierra sin intervención física |

---

## Próximos Pasos

1. Definición de umbrales de anomalía para cada sistema
2. Programación del protocolo failsafe en el cerebro de Goliat
3. Simulación de fallos para validar respuestas
4. Pruebas de enlace de emergencia con estaciones terrestres

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
