# 🇨🇴 Calendario Colombia Interactivo

Una aplicación web completa para gestionar tu calendario anual con festivos oficiales de Colombia, notas personales, técnica Pomodoro y reproductor de música integrado.

## 🌟 Características Principales

### 📅 Calendario Inteligente
- **Festivos automáticos**: Calcula automáticamente todos los festivos oficiales de Colombia según la legislación vigente
- **Vista flexible**: Alterna entre vista de año completo (12 meses) y vista de mes individual ampliada
- **Navegación intuitiva**: Cambia fácilmente entre años y meses
- **Indicadores visuales**: Diferencia fines de semana, festivos, día actual y días con notas

### 📝 Sistema de Notas
- **Notas por fecha**: Agrega notas personales a cualquier día del año
- **Interfaz modal**: Editor de notas con ventana emergente elegante
- **Exportación/Importación**: Guarda y comparte tus notas en formato JSON
- **Persistencia**: Las notas se mantienen durante la sesión actual

### 🍅 Técnica Pomodoro
- **Temporizador profesional**: 25 minutos de trabajo, 5 minutos de descanso
- **Modos alternos**: Cambia entre modo trabajo y descanso
- **Contador de sesiones**: Rastrea tu productividad
- **Controles completos**: Iniciar, pausar y reiniciar

### 🎵 Reproductor de Música
- **Archivos locales**: Carga y reproduce tu música personal
- **Controles estándar**: Play, pause, stop y control de volumen
- **Información de pista**: Muestra el nombre del archivo actual

### 📄 Exportación PDF
- **Diseño profesional**: Genera calendarios en PDF con diseño elegante
- **Tamaño automático**: Ajusta automáticamente el tamaño de página (A4/A3)
- **Contenido completo**: Incluye calendario, notas y lista de festivos
- **Codificación de colores**: Diferentes colores para festivos, notas y día actual

## 🚀 Cómo Usar

### Instalación
1. Descarga el archivo HTML
2. Abre el archivo en cualquier navegador web moderno
3. ¡Listo! No requiere instalación adicional

### Navegación del Calendario

#### Vista de Año Completo
- **Botón "Ver Año Completo"**: Muestra los 12 meses del año en una grilla
- **Cada mes**: Calendario compacto con todos los días visibles
- **Clic en cualquier día**: Abre el editor de notas

#### Vista de Mes Individual
- **Selector de mes**: Dropdown para elegir un mes específico
- **Vista ampliada**: Celdas más grandes para mejor visibilidad
- **Más detalles**: Tooltips con información completa

#### Cambio de Año
- **Selector de año**: Dropdown con rango de años (5 años atrás a 10 años adelante)
- **Actualización automática**: Recalcula festivos y actualiza todo el calendario

### Gestión de Notas

#### Crear/Editar Notas
1. **Clic en cualquier día** del calendario
2. Se abre el **modal de notas** con:
   - Fecha formateada en español
   - Área de texto para la nota
   - Botones de acción
3. **Escribir la nota** y hacer clic en "Guardar"

#### Indicadores Visuales
- **Punto azul**: Días con notas tienen un indicador circular
- **Tooltip**: Hover sobre el día muestra preview de la nota
- **Fondo especial**: Días con notas tienen fondo azul claro

#### Exportar/Importar Notas
- **Exportar**: Botón "💾 Exportar Notas" descarga archivo JSON
- **Importar**: Botón "📂 Importar Notas" carga archivo JSON previo
- **Formato**: Las notas se guardan con metadatos (fecha, cantidad, etc.)

### Técnica Pomodoro

#### Configuración Básica
- **Trabajo**: 25 minutos de concentración
- **Descanso**: 5 minutos de pausa
- **Contador**: Rastrea sesiones completadas

#### Controles
- **Iniciar**: Comienza el temporizador
- **Pausar**: Pausa/reanuda el conteo
- **Reiniciar**: Vuelve al tiempo inicial del modo actual
- **Cambiar modo**: Alterna entre trabajo y descanso

#### Notificaciones
- **Alertas automáticas**: Notifica cuando termina cada sesión
- **Cambio de modo**: Sugiere cuándo cambiar entre trabajo y descanso

### Reproductor de Música

#### Cargar Música
1. **Clic en "Elegir archivo"**
2. Seleccionar archivo de audio (MP3, WAV, etc.)
3. El nombre del archivo aparece en la interfaz

#### Controles de Reproducción
- **▶️ Reproducir**: Inicia la reproducción
- **⏸️ Pausar**: Pausa la música
- **⏹️ Detener**: Detiene y vuelve al inicio
- **Control de volumen**: Deslizador de 0 a 100%

### Exportación PDF

#### Generar PDF
1. **Clic en "📅 Descargar PDF"**
2. **Procesamiento automático**: La aplicación:
   - Calcula el tamaño óptimo de página
   - Genera el calendario completo
   - Incluye todas las notas
   - Lista todos los festivos

#### Contenido del PDF
- **Página 1**: Calendario visual completo del año
- **Página 2**: Lista detallada de notas y festivos
- **Diseño profesional**: Colores y formato elegantes

## 🎨 Elementos Visuales

### Código de Colores
- **🟢 Verde**: Día actual
- **🟠 Naranja**: Días festivos
- **🔵 Azul**: Días con notas
- **🟡 Amarillo**: Fines de semana
- **⚪ Blanco**: Días normales

### Efectos Interactivos
- **Hover**: Los días se amplían al pasar el cursor
- **Tooltips**: Información adicional en hover
- **Animaciones**: Transiciones suaves en botones y elementos

## 📱 Compatibilidad

### Navegadores Soportados
- ✅ Chrome 70+
- ✅ Firefox 65+
- ✅ Safari 12+
- ✅ Edge 79+

### Dispositivos
- 🖥️ **Desktop**: Experiencia completa
- 📱 **Mobile**: Diseño responsivo adaptado
- 📱 **Tablet**: Interfaz optimizada

### Funcionalidades por Dispositivo
| Función | Desktop | Mobile | Tablet |
|---------|---------|---------|---------|
| Calendario | ✅ | ✅ | ✅ |
| Notas | ✅ | ✅ | ✅ |
| Pomodoro | ✅ | ✅ | ✅ |
| Música | ✅ | ✅ | ✅ |
| PDF | ✅ | ✅ | ✅ |

## 🔧 Características Técnicas

### Festivos Colombianos
La aplicación calcula automáticamente:

#### Festivos Fijos
- 🎉 Año Nuevo (1 enero)
- 👷 Día del Trabajo (1 mayo)
- 🇨🇴 Independencia (20 julio)
- ⚔️ Batalla de Boyacá (7 agosto)
- 👼 Inmaculada Concepción (8 diciembre)
- 🎄 Navidad (25 diciembre)

#### Festivos Móviles (Ley Emiliani)
- 👑 Reyes Magos
- 🔨 San José
- ⛪ Ascensión del Señor
- 🍞 Corpus Christi
- ❤️ Sagrado Corazón
- 👨‍👩‍👧‍👦 San Pedro y San Pablo
- 🌟 Asunción de la Virgen
- 🌍 Día de la Raza
- 👥 Todos los Santos
- 🏛️ Independencia de Cartagena

#### Festivos de Semana Santa
- 🌿 Jueves Santo
- ✝️ Viernes Santo

### Algoritmo de Cálculo
- **Pascua**: Usa el algoritmo gregoriano preciso
- **Traslados**: Aplica la Ley Emiliani correctamente
- **Actualización**: Se recalcula automáticamente cada año

### Almacenamiento
- **Notas**: Se mantienen en memoria durante la sesión
- **Configuración**: Estados de Pomodoro y reproductor
- **Exportación**: Formato JSON estándar

## 🛠️ Tecnologías Utilizadas

### Frontend
- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos con gradientes y animaciones
- **JavaScript ES6+**: Lógica interactiva

### Librerías Externas
- **jsPDF**: Generación de documentos PDF
- **CDN**: Carga desde Cloudflare para máxima velocidad

### Características Modernas
- **Responsive Design**: Adaptable a todos los tamaños
- **Progressive Enhancement**: Funciona sin JavaScript básico
- **Accessibility**: Semántica y navegación por teclado

## 📋 Casos de Uso

### 👩‍💼 Profesionales
- **Planificación**: Organizar reuniones y proyectos
- **Productividad**: Usar Pomodoro para tareas concentradas
- **Exportación**: Compartir calendarios con equipo

### 🎓 Estudiantes
- **Estudios**: Planificar fechas de exámenes y entregas
- **Técnica Pomodoro**: Sesiones de estudio efectivas
- **Notas**: Recordatorios de tareas y eventos

### 🏠 Uso Personal
- **Familia**: Planificar vacaciones y eventos familiares
- **Recordatorios**: Cumpleaños, citas médicas, etc.
- **Música**: Ambiente relajante mientras planificas

## 🎯 Consejos de Uso

### Maximizar Productividad
1. **Combina herramientas**: Usa Pomodoro mientras planificas
2. **Música de fondo**: Carga música instrumental para concentración
3. **Notas detalladas**: Incluye horarios y contactos en las notas
4. **Exporta regularmente**: Mantén respaldos de tus notas

### Mejores Prácticas
- **Revisión semanal**: Verifica notas y planes upcoming
- **Códigos de color**: Usa las diferenciaciones visuales
- **Sincronización**: Exporta antes de cerrar el navegador
- **Accesibilidad**: Usa navegación por teclado cuando sea posible

## 🤝 Soporte y Contribución

### Reportar Problemas
Si encuentras algún error o tienes sugerencias:
1. Verifica la compatibilidad de tu navegador
2. Intenta recargar la página
3. Contacta al desarrollador con detalles específicos

### Características Futuras
- 📱 Aplicación móvil nativa
- ☁️ Sincronización en la nube
- 🔔 Notificaciones push
- 🎨 Temas personalizables
- 📊 Estadísticas de productividad

## 📄 Licencia y Créditos

### Desarrollo
- **Autor**: Esteban Alberto Martinez Palacios
- **Organización**: Claro
- **Contacto**: 38514603@claro.com.co
- **GitHub**: [EstebanM007](https://github.com/EstebanM007)

### Derechos
© Todos los derechos reservados

---

## 🚀 ¡Comienza Ahora!

1. **Descarga** el archivo HTML
2. **Abre** en tu navegador favorito
3. **Explora** las diferentes funcionalidades
4. **Personaliza** con tus notas y música
5. **Exporta** tu primer calendario PDF

¡Disfruta de una experiencia de planificación completa y productiva! 🎉