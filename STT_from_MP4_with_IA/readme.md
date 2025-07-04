# 🎙️ Transcriptor y Chat con IA

## Descripción

**Transcriptor y Chat con IA** es una aplicación de escritorio que convierte archivos de audio y video a texto utilizando reconocimiento de voz, y permite interactuar con una inteligencia artificial para resumir y analizar el contenido transcrito.

### Características principales:
- ✅ **Transcripción automática** de archivos multimedia
- ✅ **Chat inteligente** con IA para análisis del contenido
- ✅ **Soporte múltiples formatos** (.mp4, .mp3, .wav, .ogg)
- ✅ **Interfaz moderna** con formato Markdown
- ✅ **Procesamiento por segmentos** para archivos largos
- ✅ **Exportación de resultados** en archivos de texto

---

## 📋 Requisitos del Sistema

### Requisitos mínimos:
- **Sistema Operativo**: Windows 10 o superior
- **Conexión a Internet**: Requerida para transcripción y chat con IA
- **Memoria RAM**: 4 GB mínimo (8 GB recomendado)
- **Espacio en disco**: 100 MB libres
- **Tarjeta de sonido**: Para reproducir archivos de audio

### Formatos soportados:
- **Video**: .mp4
- **Audio**: .mp3, .wav, .ogg

---

## 🚀 Instalación y Configuración

### Paso 1: Descargar el archivo ejecutable
1. Descarga el archivo `TranscriptorIA.exe` desde el repositorio
2. Guarda el archivo en una carpeta de tu elección

### Paso 2: Ejecutar la aplicación
1. Haz doble clic en `TranscriptorIA.exe`
2. La aplicación se iniciará automáticamente
3. Aparecerá la interfaz principal con las instrucciones

---

## 📖 Manual de Uso

### Interfaz Principal

La aplicación se divide en **4 secciones principales**:

1. **Panel Superior**: Controles para seleccionar archivos y transcribir
2. **Panel Izquierdo**: Chat con IA (modo conversacional)
3. **Panel Derecho**: Registro de transcripción y progreso
4. **Panel Inferior**: Información del desarrollador

### Proceso de Transcripción

#### 1. Seleccionar archivo
- Haz clic en **"📁 Seleccionar Archivo"**
- Navega hasta tu archivo de audio o video
- Selecciona el archivo deseado (.mp4, .mp3, .wav, .ogg)
- El nombre del archivo aparecerá en pantalla

#### 2. Iniciar transcripción
- Haz clic en **"🎵 Transcribir Audio"**
- El proceso comenzará automáticamente:
  - **Conversión**: Si es necesario, convierte el archivo a WAV
  - **Segmentación**: Divide el audio en fragmentos de 60 segundos
  - **Transcripción**: Procesa cada segmento usando Google Speech Recognition
  - **Guardado**: Crea archivos `archivo.wav` y `transcripcion.txt`

#### 3. Monitorear progreso
- Observa el **Panel Derecho** para ver el progreso
- Se mostrará el progreso como "X/Y" segmentos procesados
- Puedes cancelar el proceso con **"❌ Cancelar Proceso"**

### Chat con IA

#### Funcionalidades del chat:
- **Resumen automático**: Tras completar la transcripción, la IA genera un resumen
- **Conversación libre**: Puedes hacer preguntas sobre el contenido
- **Formato Markdown**: Las respuestas incluyen formato rico (negrita, cursiva, listas, etc.)
- **Memoria conversacional**: Recuerda los últimos 5 mensajes

#### Cómo usar el chat:
1. **Automático**: Después de transcribir, recibirás un resumen automático
2. **Manual**: Escribe preguntas en el campo de texto inferior
3. **Enviar**: Presiona Enter o haz clic en **"➤ Enviar"**

#### Ejemplos de preguntas:
- "Resume los puntos principales"
- "¿Cuáles son las conclusiones más importantes?"
- "Explica el tema principal en términos simples"
- "¿Qué acciones se mencionan en el audio?"

---

## 📁 Archivos Generados

La aplicación crea los siguientes archivos en el directorio actual:

### Archivos permanentes:
- **`transcripcion.txt`**: Contiene el texto completo transcrito
- **`archivo.wav`**: Versión en WAV del archivo original (si fue convertido)

### Archivos temporales:
- **`segment_X_Y.wav`**: Fragmentos temporales del audio (se eliminan automáticamente)

---

## ⚠️ Limitaciones y Consideraciones

### Limitaciones técnicas:
- **Conexión a Internet**: Requerida para transcripción y chat
- **Idioma**: Transcripción optimizada para español (es-ES)
- **Calidad de audio**: La precisión depende de la claridad del audio
- **Tamaño de archivo**: Archivos muy grandes pueden tomar tiempo
- **Memoria del chat**: Solo recuerda los últimos 5 mensajes

### Consideraciones de uso:
- **Créditos de API**: El servicio gratuito de Groq tiene límites
- **Precisión**: La transcripción no es 100% perfecta
- **Archivos temporales**: Se crean archivos WAV temporales durante el proceso
- **Espacio en disco**: Asegúrate de tener suficiente espacio libre

---

## 🔧 Solución de Problemas

### Problemas comunes:

#### Error: "No se puede transcribir"
**Causa**: Problemas de conexión a Internet
**Solución**: Verifica tu conexión y vuelve a intentar

#### Error: "Error al inicializar modelo de chat"
**Causa**: API Key de Groq inválida o faltante
**Solución**: Configura correctamente la API Key

#### Error: "Formato no soportado"
**Causa**: Archivo en formato no compatible
**Solución**: Convierte el archivo a .mp4, .mp3, .wav o .ogg

#### La transcripción está incompleta
**Causa**: Audio de baja calidad o ruido de fondo
**Solución**: Usa archivos de audio más claros

#### El chat no responde
**Causa**: Límites de API agotados o problemas de red
**Solución**: Espera un tiempo o verifica la conexión

---

## 🛠️ Desarrollo y Personalización

### Tecnologías utilizadas:
- **Python**: Lenguaje principal
- **Tkinter**: Interfaz gráfica
- **SpeechRecognition**: Transcripción de audio
- **MoviePy**: Procesamiento de video
- **LangChain**: Integración con IA
- **Groq**: Servicio de IA

### Estructura del proyecto:
```
TranscriptorIA/
├── main.py              # Código principal
├── requirements.txt     # Dependencias
├── ffmpeg.exe          # Binario para conversión
└── README.md           # Este manual
```

### Para desarrolladores:
Si quieres modificar el código fuente:

1. **Instala dependencias**:
```bash
pip install -r requirements.txt
```

2. **Configura tu API Key**:
```python
os.environ["GROQ_API_KEY"] = "tu_clave_api_aqui"
```

3. **Ejecuta el script**:
```bash
python main.py
```

---

## 📞 Soporte y Contacto

### Información del desarrollador:
- **Autor**: Esteban Alberto Martinez Palacios
- **Organización**: Estrategia Digital y GEN XXI
- **Repositorio**: [https://github.com/EstebanM007/Media](https://github.com/EstebanM007/Media)

### Reportar problemas:
- Abre un issue en el repositorio de GitHub
- Incluye detalles del error y pasos para reproducirlo
- Adjunta capturas de pantalla si es necesario

### Solicitar características:
- Usa la sección "Issues" del repositorio
- Describe claramente la funcionalidad deseada
- Explica el caso de uso

---

## 📄 Licencia

Este software es de código abierto y está disponible bajo los términos especificados en el repositorio de GitHub.

---

## 🔄 Historial de Versiones

### Versión Actual
- ✅ Transcripción automática de múltiples formatos
- ✅ Chat conversacional con IA
- ✅ Interfaz moderna con Markdown
- ✅ Procesamiento por segmentos
- ✅ Exportación de resultados

---

**¡Gracias por usar Transcriptor y Chat con IA! 🎉**