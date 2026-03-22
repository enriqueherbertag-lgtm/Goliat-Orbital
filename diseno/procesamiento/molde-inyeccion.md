# Molde por Inyección - Producción de Lingotes

## Descripción

El molde por inyección es el sistema que da forma final al metal fundido, produciendo lingotes estandarizados de aluminio, cobre, hierro-tungsteno o plata. Opera dentro del módulo rotatorio, aprovechando la gravedad artificial (0.1-0.3 g) para que el metal fluya por gravedad o por presión hacia la cavidad del molde.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Tipo | Molde de dos mitades, inyección por presión o gravedad | Tecnología existente, adaptada al espacio |
| Capacidad por lingote | 5-10 kg | Escalable según demanda |
| Material del molde | Acero templado, con recubrimiento antiadherente | Resistente a altas temperaturas |
| Tiempo de ciclo | 5-10 minutos | Incluye vertido, solidificación, eyección |
| Temperatura de operación | Hasta 600°C (depende del metal) | Refrigeración activa |
| Sistema de cierre | Hidráulico o eléctrico | Asegura hermeticidad durante la inyección |

---

## Componentes

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Molde (dos mitades)** | Define la forma del lingote | Acero templado, cavidad con geometría estandarizada |
| **Sistema de cierre** | Mantiene las mitades unidas durante la inyección | Actuadores hidráulicos o eléctricos |
| **Sistema de inyección** | Introduce el metal fundido en el molde | Presión (0.1-0.5 MPa) o gravedad |
| **Sistema de eyección** | Expulsa el lingote solidificado | Pistones o levas |
| **Refrigeración** | Acelera la solidificación | Conductos internos con fluido refrigerante |
| **Revestimiento** | Evita que el metal se adhiera al molde | Nitruro de titanio o recubrimiento cerámico |

---

## Ciclo de Operación

| Fase | Acción | Duración |
|:---|:---|:---|
| **1. Preparación** | Molde cerrado, sistema de refrigeración activo | 30 s |
| **2. Vertido** | Metal fundido del horno se vierte en la cámara de inyección | 30 s |
| **3. Inyección** | Metal es presionado hacia la cavidad del molde | 10-30 s |
| **4. Solidificación** | Metal se enfría y solidifica dentro del molde | 3-5 min |
| **5. Apertura** | Molde se abre, lingote es expulsado | 30 s |
| **6. Extracción** | Brazo robótico retira el lingote y lo lleva a la bodega | 30 s |

---

## Tipos de Lingotes

| Formato | Dimensiones | Uso |
|:---|:---|:---|
| Lingote rectangular estándar | 20×10×5 cm | Fácil almacenamiento, apilable |
| Barra larga | 50×5×5 cm | Para aplicaciones estructurales |
| Plancha delgada | 30×20×1 cm | Para paneles solares o blindaje |

El formato se selecciona según el cliente y la aplicación.

---

## Integración con el Horno

```
[HORNO] → [MOLDE POR INYECCIÓN] → [BODEGA]
    ↓              ↓                  ↓
[METAL FUNDIDO] [LINGOTE]       [INVENTARIO]
```

La gravedad artificial facilita el vertido desde el crisol hacia la cámara de inyección, eliminando la necesidad de bombas complejas.

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallo de cierre** | Sensores de posición; si las mitades no cierran completamente, se detiene la inyección |
| **Lingote adherido** | Revestimiento antiadherente + sistema de eyección reforzado |
| **Solidificación incompleta** | Control de temperatura en el molde; si se detecta temperatura anómala, se extiende el ciclo |
| **Fuga de metal** | Cámara de inyección con doble pared, sistema de contención |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Tecnología probada** | La inyección en molde existe desde hace siglos. No hay riesgo de desarrollo. |
| **Lingotes estandarizados** | Producto listo para vender, sin procesamiento adicional |
| **Escalable** | Tamaño y forma ajustables según demanda |
| **Bajo consumo** | Solo requiere energía para cierre, eyección y refrigeración |

---

## Producción Estimada

| Configuración | Ciclos por día | Lingotes por día | Masa por día |
|:---|:---|:---|:---|
| Un molde, ciclo de 10 min | 144 | 144 | 720-1440 kg |
| Dos moldes en paralelo | 288 | 288 | 1.4-2.9 toneladas |

La producción se ajusta según la cantidad de fragmentos capturados.

---

## Próximos Pasos

1. Diseño del molde (geometría, material, revestimiento)
2. Selección de sistema de cierre y eyección
3. Integración con el horno (sistema de vertido)
4. Pruebas en Tierra con metales fundidos

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
