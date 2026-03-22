# Monitoreo Remoto - CCTV Interno y Externo

## Descripción

Goliat-Orbital cuenta con un sistema de videovigilancia interna y externa que permite a los operadores en Tierra supervisar visualmente el estado de la nave, diagnosticar fallos, y verificar operaciones críticas (captura, fundición, almacenamiento) sin necesidad de intervención física. Las cámaras están distribuidas en zonas estratégicas y transmiten imágenes comprimidas vía enlace banda X.

---

## Especificaciones Técnicas

| Parámetro | Valor |
|:---|:---|
| Resolución | 1080p (1920×1080) |
| Compresión | H.265 (alta eficiencia) |
| Frecuencia de imagen | 1-30 fps (ajustable según ancho de banda) |
| Sensibilidad | LUX 0.01 (luz estelar) |
| Campo de visión | 90° (cámaras fijas) / 360° (panorámicas) |
| Protección | Carcasa sellada, Space Armor en zonas expuestas |
| Iluminación | LEDs infrarrojos para visión nocturna |

---

## Ubicación de Cámaras

### Externas (6 unidades)

| Ubicación | Función |
|:---|:---|
| **Proa** | Visión frontal de la trayectoria, detección visual de fragmentos |
| **Popa** | Visión trasera, verificación de expulsión de residuos |
| **Lateral (4)** | Cobertura de las seis branquias (dos cámaras cubren tres branquias cada una) |

### Internas (10 unidades)

| Ubicación | Función |
|:---|:---|
| **Tolva de recepción (2)** | Verificar entrada de fragmentos, detectar atascos |
| **Compactador (2)** | Supervisar ciclo de compactación, estado de la prensa |
| **Módulo rotatorio (2)** | Monitorear rotación, estado del horno y crisol |
| **Bodega de lingotes (2)** | Control de inventario visual, estado de contenedores |
| **Sala de control (2)** | Supervisar computadores, sistemas eléctricos, estado general |

---

## Flujo de Datos

```
[CÁMARAS] → [COMPRESOR DE VIDEO] → [MEMORIA LOCAL] → [ENLACE BANDA X] → [TIERRA]
        ↓
[PROCESAMIENTO LOCAL] → [DETECCIÓN DE ANOMALÍAS] → [ALERTA AUTOMÁTICA]
```

---

## Modos de Transmisión

| Modo | Descripción | Ancho de banda |
|:---|:---|:---|
| **Continua** | Transmisión en vivo (baja resolución, 1 fps) | Bajo |
| **Bajo demanda** | Alta resolución cuando se solicita desde Tierra | Alto, puntual |
| **Evento** | Grabación de alta resolución cuando se detecta actividad (captura, fundición) | Local, se descarga después |
| **Alarma** | Transmisión inmediata de alta resolución ante anomalía | Prioritario |

---

## Procesamiento a Bordo

| Función | Descripción |
|:---|:---|
| **Detección de movimiento** | Identifica fragmentos en el campo de visión externo |
| **Reconocimiento de atascos** | Detecta obstrucciones en tolva, compactador, horno |
| **Control de inventario** | Cuenta lingotes en bodega mediante visión computacional |
| **Anomalías térmicas** | Cámaras infrarrojas detectan sobrecalentamiento |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo de cámara** | Áreas críticas con cobertura de al menos dos cámaras |
| **Pérdida de enlace** | Grabación local en memoria no volátil; transmisión diferida cuando se recupera |
| **Almacenamiento** | 1 TB de almacenamiento local (eventos de los últimos 30 días) |
| **Cifrado** | Video encriptado antes de transmisión; solo personal autorizado puede verlo |

---

## Integración con el Cerebro

El sistema de monitoreo está conectado al cerebro de Goliat (IA a bordo). Cuando se detecta una anomalía visual (atasco, fragmento inesperado, desalineación), el cerebro:

1. Prioriza la transmisión de video al operador en Tierra
2. Genera una alerta en el panel de control
3. Puede activar protocolos automáticos (ej: detener compactador si se detecta atasco)

---

## Interfaz en Tierra

| Elemento | Función |
|:---|:---|
| **Panel de 12 pantallas** | Visualización simultánea de todas las cámaras |
| **Zoom digital** | Ampliación de áreas de interés |
| **Marcado de anomalías** | El sistema resalta zonas donde detecta actividad inusual |
| **Grabación** | Archivo de video de todas las operaciones, disponible para revisión posterior |
| **Control de cámaras** | Ajuste de resolución, frecuencia, orientación (cámaras panorámicas) |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Diagnóstico remoto** | Los operadores en Tierra pueden ver el problema sin necesidad de telemetría compleja |
| **Seguridad** | Verificación visual de que los sistemas funcionan correctamente |
| **Auditoría** | Registro visual de todas las operaciones, útil para análisis post-misión |
| **Redundancia** | Si fallan los sensores, la imagen puede reemplazar datos perdidos |

---

## Próximos Pasos

1. Selección de cámaras comerciales calificadas para espacio (rad-hard, vacío, temperatura)
2. Diseño de la red de transmisión (cables, conectores, anillos deslizantes en módulo rotatorio)
3. Integración con el cerebro de Goliat (detección de anomalías visuales)
4. Desarrollo de la interfaz de visualización en Tierra

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
