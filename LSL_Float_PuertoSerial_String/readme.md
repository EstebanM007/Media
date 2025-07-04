# Interfaz de Configuración LSL y COM

## Descripción

Esta aplicación permite conectar streams de Lab Streaming Layer (LSL) con puertos seriales COM, facilitando la transmisión de datos en tiempo real desde dispositivos de adquisición de señales (como EEG, EMG, etc.) hacia otros sistemas o dispositivos a través de comunicación serial.

## Características principales

- **Conexión LSL**: Detección automática y conexión a streams LSL disponibles
- **Comunicación Serial**: Envío de comandos a puertos COM basado en condiciones de los datos
- **Configuración flexible**: Definición de umbrales y condiciones personalizadas
- **Modo simulación**: Visualización en pantalla sin necesidad de hardware serial
- **Gestión de configuraciones**: Guardado y carga de configuraciones en formato JSON
- **Monitoreo en tiempo real**: Consola serial para visualizar datos transmitidos

## Requisitos del sistema

### Hardware
- Dispositivo compatible con LSL (opcional para simulación)
- Puerto COM/Serial (opcional para simulación)

### Software
- Windows 10/11 (recomendado)
- El ejecutable incluye todas las dependencias necesarias

## Instalación

1. Descarga el archivo ejecutable `LSL_COM_Interface.exe`
2. Ejecuta el archivo (no requiere instalación)
3. Si Windows Defender o antivirus bloquea la ejecución, añade el archivo a las excepciones

## Guía de uso

### 1. Configuración inicial

#### Puerto Serial
1. **Seleccionar Puerto**: Usa el menú desplegable para seleccionar el puerto COM deseado
2. **Actualizar Puertos**: Haz clic en "Actualizar Puertos" para refrescar la lista
3. **Modo Simulación**: Activa esta opción para probar sin hardware real
4. **Consola Serial**: Habilita para ver los datos transmitidos en tiempo real

#### Streams LSL
1. Los streams disponibles se actualizan automáticamente
2. Asegúrate de que tu dispositivo LSL esté transmitiendo datos
3. Los streams aparecen en formato: `Nombre (Tipo)`

### 2. Configuración de condiciones

#### Agregar condiciones
1. Haz clic en "Agregar Stream" para crear una nueva condición
2. Selecciona el stream LSL de la lista desplegable
3. Configura los parámetros según tus necesidades:

#### Parámetros de configuración

**Condiciones Positivas (+):**
- **Lim Inf (+)**: Límite inferior para valores positivos
- **Lim Sup (+)**: Límite superior para valores positivos  
- **Letra (+)**: Carácter a enviar cuando el valor esté en este rango

**Condiciones Negativas (-):**
- **Lim Inf (-)**: Límite inferior para valores negativos
- **Lim Sup (-)**: Límite superior para valores negativos
- **Letra (-)**: Carácter a enviar cuando el valor esté en este rango

#### Ejemplo de configuración
```
Stream: EEG_Stream (EEG)
Lim Inf (+): 50     Lim Sup (+): 100    Letra (+): A
Lim Inf (-): -100   Lim Sup (-): -50    Letra (-): B
```

### 3. Operación

#### Inicio de conexión
1. Configura al menos una condición válida
2. Haz clic en "Conectar"
3. La aplicación iniciará la monitorización automática
4. El estado cambiará a "Conectado"

#### Durante la operación
- Los datos se procesan en tiempo real
- Se envían caracteres por el puerto serial cuando se cumplen las condiciones
- En modo simulación, los eventos se muestran en los cuadros de log
- La consola serial muestra los caracteres transmitidos

#### Detener la conexión
- Haz clic en "Desconectar" para finalizar la sesión
- Todos los recursos se liberan automáticamente

### 4. Gestión de configuraciones

#### Guardar configuración
1. Configura todas las condiciones deseadas
2. Haz clic en "Guardar configuración"
3. Selecciona la ubicación y nombre del archivo JSON
4. La configuración se guarda para uso futuro

#### Cargar configuración
1. Haz clic en "Cargar configuración"
2. Selecciona el archivo JSON previamente guardado
3. Las condiciones se cargan automáticamente

## Casos de uso comunes

### Neurofeedback
- Monitorea ondas cerebrales específicas
- Envía comandos para activar estímulos visuales/auditivos
- Configura umbrales para diferentes estados mentales

### Control de dispositivos
- Utiliza señales EMG para controlar actuadores
- Envía comandos basados en intensidad muscular
- Interfaz con sistemas de rehabilitación

### Investigación científica
- Sincronización de eventos con equipos de laboratorio
- Trigger automático basado en condiciones fisiológicas
- Logging de eventos para análisis posterior

## Solución de problemas

### Problemas comunes

**No se detectan streams LSL:**
- Verifica que el dispositivo LSL esté transmitiendo
- Haz clic en "Actualizar Puertos" para refrescar
- Comprueba la conexión de red (LSL usa red local)

**Error de conexión COM:**
- Verifica que el puerto esté disponible
- Cierra otros programas que puedan usar el puerto
- Usa el modo simulación para probar la configuración

**Caracteres no se envían:**
- Revisa que los umbrales estén correctamente configurados
- Verifica que los valores del stream estén en el rango esperado
- Comprueba la consola serial para ver la actividad

**La aplicación no responde:**
- Cierra y reinicia la aplicación
- Verifica que no haya múltiples instancias ejecutándose
- Comprueba los recursos del sistema

### Códigos de error

- **"Seleccione un stream para cada fila"**: Falta seleccionar un stream LSL
- **"Debe definir al menos un límite superior"**: Falta configurar umbrales
- **"Debe definir una sola letra"**: El campo de letra está vacío o tiene múltiples caracteres
- **"No se pudo conectar al puerto"**: Problema con la conexión COM
- **"Error al resolver streams"**: Problema con la detección LSL

## Especificaciones técnicas

### Formatos soportados
- Streams LSL: Todos los tipos estándar
- Puertos COM: RS-232, USB-Serial, Bluetooth Serial
- Configuración: JSON

### Rendimiento
- Frecuencia de muestreo: Hasta 1000 Hz
- Latencia: < 10 ms
- Múltiples streams simultáneos: Sí
- Historial de muestras: 500 valores por stream

### Limitaciones
- Máximo 1 carácter por condición
- Umbrales fijos durante la sesión
- Comunicación serial unidireccional (solo envío)

## Contacto y soporte

Para reportar problemas o sugerencias:
- Incluye la configuración utilizada
- Describe los pasos para reproducir el problema
- Adjunta capturas de pantalla si es relevante

## Licencia

Esta aplicación es distribuida como software propietario. El uso está sujeto a los términos de licencia correspondientes.

---

**Versión**: 1.0  
**Fecha**: 2025  
**Compatibilidad**: Windows 10/11