# Sensores de Proximidad - Detección de Fragmentos

## Descripción

Cada branquia de Goliat-Orbital tiene su propio sistema de sensores de proximidad. Su función es detectar fragmentos de basura espacial a cientos de metros de distancia, calcular su trayectoria y velocidad relativa, y enviar la información al computador de a bordo para activar la captura con antelación.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Radar / Lidar / Ópticos (combinación) | Redundancia tecnológica |
| Alcance | Hasta 500 m | Detecta fragmentos de 1 cm en adelante |
| Precisión | ±0.1 m en posición, ±0.1 m/s en velocidad | Suficiente para calcular trayectoria |
| Campo de visión | 90° (por branquia) | Cada sensor cubre su área asignada |
| Frecuencia de actualización | 10 Hz | Diez veces por segundo |
| Consumo | 50-100 W por unidad | Bajo, operación continua |
| Protección | Carcasa sellada, Space Armor en la base | Resistente a impacto y radiación |

---

## Tipos de Sensores

| Tipo | Función | Ventaja |
|:---|:---|:---|
| **Radar** | Detecta objetos metálicos a larga distancia | Robusto, no afectado por condiciones de iluminación |
| **Lidar** | Genera nube de puntos de alta precisión | Detalla forma y orientación del fragmento |
| **Óptico** | Cámara de alta resolución | Confirma visualmente el tipo de fragmento |

Los tres se usan en conjunto. El radar da la alerta inicial. El lidar refina la trayectoria. El óptico confirma antes de abrir la compuerta.

---

## Ciclo de Operación

| Fase | Acción | Sensor principal |
|:---|:---|:---|
| **1. Detección lejana** | Radar detecta fragmento a > 500 m | Radar |
| **2. Seguimiento** | Lidar mide trayectoria precisa a 500-200 m | Lidar |
| **3. Identificación** | Óptico confirma tipo y tamaño a 200-100 m | Óptico |
| **4. Preparación** | Computador calcula tiempo de llegada y activa compresores | Todos |
| **5. Captura** | Fragmento entra en zona de influencia (100-0 m) | Todos |
| **6. Verificación** | Sensores confirman entrada y cierran compuerta | Óptico + radar |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo de un sensor** | Tres tecnologías independientes. Si falla una, las otras dos siguen. |
| **Falso positivo** | Validación cruzada (radar + lidar + óptico) antes de activar captura. |
| **Falso negativo** | Cada sensor tiene su propio procesamiento; si uno no detecta, otro puede compensar. |
| **Interferencia** | Filtrado digital, frecuencias de radar separadas por branquia. |

---

## Integración con la Branquia

```
[SENSORES] → [PROCESADOR LOCAL] → [COMPUTADOR DE NAVEGACIÓN]
        ↓
[TIEMPO DE LLEGADA] → [ACTIVACIÓN DE COMPRESORES] → [APERTURA DE COMPUERTA]
```

---

## Datos de Entrada y Salida

| Entrada | Origen | Procesamiento | Salida |
|:---|:---|:---|:---|
| Distancia | Radar / Lidar | Filtro de Kalman | Posición 3D |
| Velocidad | Radar (efecto Doppler) | Cálculo vectorial | Velocidad relativa |
| Trayectoria | Lidar (nube de puntos) | Extrapolación lineal | Tiempo de llegada |
| Imagen | Óptico | Reconocimiento de patrones | Clasificación (tamaño, tipo) |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Redundancia tecnológica** | No hay punto único de fallo. Si un sensor falla, los otros siguen. |
| **Alcance suficiente** | 500 m da tiempo para activar compresores y establecer flujo antes de que llegue el fragmento. |
| **Precisión** | Posición y velocidad medidas con error despreciable para la captura. |
| **Bajo consumo** | Operación continua sin afectar el balance energético de la nave. |

---

## Próximos Pasos

1. Selección de sensores comerciales (radar, lidar, ópticos) calificados para espacio
2. Integración con sistema de procesamiento local (filtro de Kalman, predicción de trayectoria)
3. Pruebas en Tierra con fragmentos simulados
4. Calibración en órbita (fase de pruebas)

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
