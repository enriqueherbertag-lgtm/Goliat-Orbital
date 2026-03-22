# Enlace de Comunicaciones - Voz y Datos con Tierra

## Descripción

El sistema de comunicaciones de Goliat-Orbital es el puente con Tierra. Permite recibir comandos, enviar telemetría, transmitir video de las cámaras de monitoreo, y en caso de emergencia, mantener un enlace de baja velocidad pero altamente confiable. Está diseñado para operar con las estaciones terrestres existentes (Deep Space Network, ESA, redes comerciales) y con antenas propias.

---

## Especificaciones Técnicas

| Parámetro | Banda X (Principal) | Banda S (Respaldo) |
|:---|:---|:---|
| Frecuencia | 8-12 GHz | 2-4 GHz |
| Velocidad de datos | Hasta 100 Mbps | 1-10 kbps |
| Antena | Direccional, alta ganancia (1.5 m diámetro) | Omnidireccional, baja ganancia |
| Potencia de transmisión | 20-100 W | 5-10 W |
| Alcance | Tierra (órbita baja) | Tierra (órbita baja) |
| Uso principal | Telemetría, video, comandos complejos | Emergencia, telemetría básica |

---

## Componentes

| Componente | Función | Tecnología |
|:---|:---|:---|
| **Antena de alta ganancia** | Enlace principal | Reflector de 1.5 m, desplegable |
| **Antena omnidireccional** | Enlace de respaldo | Monopolo o parche |
| **Transceptor banda X** | Modulación y demodulación | Tecnología comercial calificada para espacio |
| **Transceptor banda S** | Respaldo | Tecnología madura, bajo consumo |
| **Amplificadores de potencia** | Aumentan la señal de salida | TWTA (tubo de onda viajera) o SSPA (estado sólido) |
| **Sistema de apuntado** | Orienta la antena de alta ganancia hacia Tierra | Control de actitud (ruedas de reacción) |

---

## Flujo de Datos

```
[CEREBRO DE GOLIAT] → [DATOS] → [MODULADOR] → [TRANSMISOR] → [ANTENA] → [TIERRA]
        ↓
[ANTENA] → [RECEPTOR] → [DEMODULADOR] → [COMANDOS] → [CEREBRO DE GOLIAT]
```

---

## Modos de Operación

| Modo | Descripción | Enlace utilizado |
|:---|:---|:---|
| **Nominal** | Telemetría completa, video ocasional, comandos complejos | Banda X |
| **Supervisado** | Telemetría continua, video bajo demanda | Banda X |
| **Emergencia** | Solo estado básico de la nave, comandos de seguridad | Banda S |
| **Modo seguro** | Latido (heartbeat), espera de instrucciones | Banda S |

---

## Telemetría Transmitida

| Dato | Frecuencia | Uso |
|:---|:---|:---|
| Posición y velocidad | 1 Hz | Navegación, seguimiento |
| Estado de los sistemas | 1 Hz | Diagnóstico |
| Inventario de lingotes | 1/minuto | Comercial |
| Video de cámaras clave | Bajo demanda | Inspección visual |
| Alertas de anomalías | Inmediato | Emergencias |

---

## Enlace con Estaciones Terrestres

Goliat puede usar:

| Red | Operador | Cobertura | Costo |
|:---|:---|:---|:---|
| Deep Space Network (DSN) | NASA | Global | Por uso |
| Estaciones de ESA | ESA | Global | Por uso |
| Red comercial (KSAT, SSC) | Varios | Global | Por contrato |
| Estaciones propias | Goliat (opcional) | Limitada | Inversión inicial |

---

## Redundancia y Seguridad

| Aspecto | Estrategia |
|:---|:---|:---|
| **Fallo de antena de alta ganancia** | Antena omnidireccional mantiene enlace básico |
| **Fallo de transceptor banda X** | Transceptor banda S mantiene enlace de emergencia |
| **Pérdida de apuntado** | Antena omnidireccional no requiere apuntado |
| **Interferencia** | Múltiples frecuencias, modulación robusta (BPSK, QPSK) |
| **Cifrado** | Enlace encriptado para evitar comandos maliciosos |

---

## Ventajas del Diseño

| Ventaja | Implicación |
|:---|:---|:---|
| **Redundancia** | Dos sistemas independientes. Si falla uno, el otro sigue funcionando. |
| **Alta velocidad** | Banda X permite transmitir video y grandes volúmenes de datos. |
| **Robustez** | Banda S garantiza comunicación incluso en emergencia. |
| **Compatibilidad** | Utiliza estándares de la industria (CCSDS, GMR-1). |

---

## Próximos Pasos

1. Selección de antenas comerciales (telescópicas, desplegables)
2. Selección de transceptores banda X y banda S
3. Diseño del sistema de apuntado (integrado con control de actitud)
4. Contratación de servicios de estaciones terrestres
5. Pruebas de enlace con satélites en órbita (simulación)

---

*Documento v1.0 - Marzo 2026*
*Goliat-Orbital - Mackiber Labs*
