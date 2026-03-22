# Compresores - Generación de Flujo para Captura

## Descripción

Cada branquia de Goliat-Orbital tiene su propio compresor. Su función es generar un flujo continuo de gas desde el exterior hacia el interior de la nave, que arrastra los fragmentos de basura espacial sin necesidad de contacto físico ni impactos.

---

## Especificaciones Técnicas

| Parámetro | Valor | Observación |
|:---|:---|:---|
| Cantidad | 6 (uno por branquia) | Independientes, con redundancia |
| Tipo | Turbocompresor de flujo axial | Optimizado para gases de baja densidad |
| Caudal | Variable (0-500 m³/min) | Ajustable según tamaño de fragmento |
| Presión diferencial | Hasta 10 kPa | Suficiente para arrastrar fragmentos de hasta 2.5 m |
| Consumo energético | 5-50 kW por compresor | Varía según demanda |
| Alimentación | Red eléctrica de la nave | Paneles solares + baterías |
| Control | Velocidad variable | Regulación fina del flujo |

---

## Principio de Funcionamiento

El compresor aspira el gas de la atmósfera residual (presente en órbita baja) y lo acelera hacia el interior de la nave. El flujo generado arrastra los fragmentos que están en la zona de influencia de la branquia.

La clave es la **anticipación**: los sensores detectan el fragmento a cientos de metros, y el compresor se enciende antes de que llegue. Cuando el fragmento entra en la zona de influencia, el flujo ya está estable.

---

## Modos de Operación

| Modo | Función | Consumo |
|:---|:---|:---|
| **Espera** | Apagado (compuerta cerrada) | 0 kW |
| **Detección** | Encendido progresivo, flujo bajo | 1-5 kW |
| **Captura** | Flujo nominal | 5-50 kW |
| **Mantenimiento** | Flujo bajo continuo para limpieza | 1-5 kW |

---

## Diseño

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Motor** | Impulsa el rotor | Motor eléctrico de alta velocidad |
| **Rotor** | Genera el flujo | Geometría optimizada para gases de baja densidad |
| **Estator** | Dirige el flujo | Diseño aerodinámico |
| **Carcasa** | Contiene el conjunto | Material ligero, resistente a corrosión |
| **Controlador** | Regula velocidad | Electrónica de potencia, redundante |

---

## Integración con la Branquia

```
[BRANQUIA]
    ↓
[SENSORES] detectan fragmento a 500 m
    ↓
[COMPRESOR] se activa con antelación (T-10 s)
    ↓
[FLUJO DE GAS] se establece en la tobera saxofón
    ↓
[FRAGMENTO] es arrastrado hacia el interior
```

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|
| **Fallos** | Cada compresor es independiente. Si falla uno, las otras cinco branquias siguen operando. |
| **Sobrecarga** | Control de velocidad, limitación electrónica de corriente |
| **Temperatura** | Refrigeración por radiadores, sensores térmicos de corte |
| **Atascos** | Detección de bloqueo, inversión de flujo para despejar |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|
| **Independencia** | Un compresor por branquia, sin dependencias cruzadas |
| **Eficiencia** | Solo se activan los compresores necesarios |
| **Anticipación** | Flujo estable, sin picos de consumo |
| **Redundancia** | Falla uno, los otros compensan |

---

## Próximos Pasos

1. Selección de compresores comerciales (o diseño propio)
2. Pruebas en cámara de vacío con gas de baja densidad
3. Simulación de flujo con fragmentos de distintos tamaños
4. Integración con sistema de sensores y control

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
