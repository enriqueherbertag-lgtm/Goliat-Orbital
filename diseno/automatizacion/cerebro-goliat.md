# Cerebro de Goliat - IA a Bordo

## Descripción

El cerebro de Goliat-Orbital es un modelo de inteligencia artificial basado en DeepSeek, adaptado para la toma de decisiones autónoma en órbita. Es el sistema que integra los datos de los sensores, prioriza objetivos, gestiona los recursos energéticos, controla los actuadores, y reporta solo lo relevante a Tierra.

No es un sistema de control tradicional. Es un sistema que **aprende, anticipa, y decide** en tiempo real.

---

## Arquitectura Funcional

```
[SENSORES] → [PROCESAMIENTO LOCAL] → [MODELO DEEPSEEK] → [ACTUADORES]
        ↓                                    ↓
[FILTRO DE KALMAN]                      [DECISIONES]
        ↓                                    ↓
[PREDICCIÓN DE TRAYECTORIA]             [COMANDOS]
        ↓                                    ↓
[GESTIÓN DE ENERGÍA]                    [REPORTE A TIERRA]
```

---

## Capacidades

| Capacidad | Descripción |
|:---|:---|
| **Detección de fragmentos** | Integra datos de radar, lidar y ópticos para localizar objetos a hasta 500 m |
| **Predicción de trayectoria** | Calcula tiempo de llegada a cada branquia, con precisión de décimas de segundo |
| **Priorización** | Decide qué fragmento capturar primero según tamaño, peligrosidad y valor comercial |
| **Gestión de energía** | Distribuye potencia entre compresores, horno, motores y sistemas de soporte según demanda |
| **Control de actuadores** | Abre y cierra compuertas, activa compresores, maneja el horno, controla el molde |
| **Reporte a Tierra** | Envía telemetría compacta (estado, inventario, anomalías) con priorización de datos |
| **Modo seguro** | Ante fallo, apaga sistemas no esenciales, activa enlace de emergencia y espera instrucciones |

---

## Fuentes de Datos

| Fuente | Datos | Frecuencia |
|:---|:---|:---|
| Radar | Distancia, velocidad radial | 10 Hz |
| Lidar | Posición 3D, forma | 10 Hz |
| Óptico | Imagen, clasificación | 1 Hz |
| GPS | Posición orbital | 1 Hz |
| Sensores estelares | Actitud (orientación) | 10 Hz |
| Giroscopios | Movimiento relativo | 100 Hz |
| Sensores de presión | Estado de compuertas, fugas | 10 Hz |
| Sensores de temperatura | Estado del horno, sistemas | 1 Hz |
| Sensores de potencia | Consumo energético | 10 Hz |

---

## Algoritmos Clave

| Algoritmo | Función |
|:---|:---|
| **Filtro de Kalman** | Fusiona datos de múltiples sensores para estimar posición y velocidad con precisión |
| **Predictor de trayectoria** | Extrapola movimiento del fragmento para calcular tiempo de llegada a cada branquia |
| **Gestor de recursos** | Asigna energía según prioridad: captura > procesamiento > propulsión > reporte |
| **Sistema de reglas** | Define cuándo capturar, cuándo procesar, cuándo almacenar, cuándo reportar |
| **Protocolo failsafe** | Monitoriza estado de todos los sistemas; si algo falla, entra en modo seguro |

---

## Modos de Operación

| Modo | Descripción |
|:---|:---|
| **Autónomo** | El cerebro toma todas las decisiones. Solo reporta estado. Modo por defecto. |
| **Supervisado** | El cerebro opera solo, pero envía datos en tiempo real. Tierra puede intervenir si lo considera necesario. |
| **Remoto** | Tierra toma el control total. El cerebro solo ejecuta comandos. Usado en pruebas o emergencias complejas. |
| **Modo seguro** | Ante una anomalía (fallo de sensor, pérdida de comunicación, consumo anómalo), el cerebro apaga todo, activa el enlace de emergencia (banda S) y espera instrucciones. |

---

## Integración con la Nave

| Componente | Conexión |
|:---|:---|
| **Sensores** | Entrada de datos (radar, lidar, ópticos, GPS, sensores estelares, giroscopios) |
| **Computador de navegación** | Comparte información de órbita y actitud para predicción de trayectoria |
| **Sistema de control** | Salida de comandos a compresores, compuertas, horno, motores, sistema de almacenamiento |
| **Comunicaciones** | Envía telemetría a Tierra vía banda X; recibe comandos remotos vía banda S |
| **Sistema eléctrico** | Monitorea consumo y controla distribución de energía |

---

## Actualizaciones y Mantenimiento

El cerebro puede recibir actualizaciones desde Tierra vía enlace banda X. Los nuevos modelos se cargan en vuelo sin necesidad de reiniciar la nave. Los parámetros de decisión (umbrales de prioridad, límites de consumo) se ajustan de forma remota.

| Tipo de actualización | Método | Riesgo |
|:---|:---|:---|
| Parámetros | Comando remoto | Bajo |
| Algoritmos | Carga de nuevo modelo (banda X) | Medio (requiere validación en vuelo) |
| Sistema completo | Reemplazo de módulo de cómputo (solo en mantenimiento) | Alto (requiere acople humano o robótico) |

---

## Redundancia

| Nivel | Descripción |
|:---|:---|
| **Hardware** | Dos computadores principales (principal + respaldo). Si falla uno, el otro toma el control en milisegundos. |
| **Almacenamiento** | Memoria no volátil con copia del sistema base. Si el sistema operativo se corrompe, se reinicia desde el backup. |
| **Comunicaciones** | El cerebro puede operar con pérdida de enlace. Si se recupera, sincroniza los datos pendientes. |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Basado en DeepSeek** | Aprovecha un modelo probado en procesamiento de lenguaje y toma de decisiones, adaptado al espacio. |
| **Autonomía total** | Reduce dependencia de enlace con Tierra. La nave opera sola el 99% del tiempo. |
| **Flexibilidad** | Se puede actualizar en vuelo sin cambiar hardware. |
| **Redundancia** | Dos computadores, memoria backup, múltiples sensores. Sin punto único de fallo. |

---

## Próximos Pasos

1. Adaptación del modelo DeepSeek para procesamiento de datos de sensores (radar, lidar, etc.)
2. Entrenamiento con simulaciones de captura orbital
3. Validación en Tierra con datos reales de basura espacial (NASA, ESA)
4. Integración con hardware de vuelo (computadores a bordo)
5. Prueba en órbita (fase 1 de Goliat)

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
