# 📊 Gantt - Flujo de Procesos con SheetDB

## 📋 Descripción

Sistema de gestión de proyectos con diagrama de Gantt que permite crear, editar y visualizar tareas de manera interactiva. Incluye sincronización con Google Sheets a través de SheetDB para trabajo colaborativo en tiempo real.

## ✨ Características Principales

- **Diagrama de Gantt Interactivo**: Visualización temporal de tareas con arrastrar y soltar
- **Sincronización con Google Sheets**: Backup automático y colaboración en tiempo real
- **Gestión Completa de Tareas**: Crear, editar, duplicar y eliminar tareas
- **Estadísticas en Tiempo Real**: Monitoreo del progreso del proyecto
- **Exportación Múltiple**: PDF con diagrama completo y archivos JS
- **Personalización Visual**: Colores personalizables para cada tarea
- **Interfaz Responsiva**: Optimizada para escritorio y dispositivos móviles

## 🚀 Instalación

### Opción 1: Uso Directo
1. Descarga el archivo HTML
2. Abre el archivo en tu navegador web
3. ¡Listo para usar!

### Opción 2: Servidor Local
```bash
# Usar Python (recomendado)
python -m http.server 8000

# O usar Node.js
npx http-server
```

## 📊 Configuración de Google Sheets (Para Desarrollador)

### 1. Crear Hoja de Cálculo
- Crea una nueva hoja en Google Sheets
- Nombra las columnas: `id`, `name`, `responsible`, `weight`, `status`, `description`, `start`, `end`, `hue`

### 2. Configurar SheetDB
1. Ve a [SheetDB.io](https://sheetdb.io)
2. Registra tu cuenta
3. Conecta tu hoja de Google Sheets
4. Copia la API URL generada
5. Reemplaza `SHEETDB_API_URL` en el código

### 3. Configurar Permisos
- Asegúrate de que la hoja sea accesible (compartida con el enlace)
- Configura permisos de lectura/escritura según necesites

## 📖 Manual de Usuario

### 🎯 Interfaz Principal

#### Panel de Estadísticas
- **Total Tareas**: Número total de tareas activas
- **Completadas**: Tareas finalizadas
- **Progreso**: Porcentaje promedio de avance
- **Días Restantes**: Tiempo hasta la próxima fecha límite

#### Barra de Progreso Global
Muestra el progreso general del proyecto con colores dinámicos:
- 🔴 Rojo: < 30% (Atención requerida)
- 🟡 Amarillo: 30-70% (En progreso)
- 🔵 Azul: > 70% (Buen avance)

### 🛠️ Gestión de Tareas

#### Crear Nueva Tarea
1. Haz clic en **"➕ Agregar Paso"**
2. Completa los campos en la tabla:
   - **ID**: Identificador único (auto-generado)
   - **Etapa**: Nombre de la tarea
   - **Responsable**: Persona asignada
   - **% Avance**: Progreso actual (0-100)
   - **Estado**: Pendiente, En Curso, Completado, N/A
   - **Descripción**: Detalles adicionales
   - **Inicio/Fin**: Fechas del proyecto

#### Personalizar Colores
- Usa el **slider de color** para ajustar el matiz
- Ingresa valores específicos en el **campo numérico**
- Visualiza el cambio en tiempo real

#### Acciones Disponibles
- **📋 Duplicar**: Crea una copia de la tarea
- **🗑️ Eliminar**: Borra la tarea seleccionada
- **❌ Eliminar Último**: Quita la última tarea agregada
- **🗑️ Limpiar Todo**: Elimina todas las tareas (con confirmación)

### 📊 Diagrama de Gantt

#### Características del Diagrama
- **Visualización Temporal**: Barras horizontales que muestran duración
- **Progreso Visual**: Relleno de barra según % de avance
- **Colores Personalizados**: Cada tarea con su color único
- **Información Emergente**: Detalles al pasar el cursor
- **Edición Interactiva**: Arrastra para cambiar fechas y progreso

#### Modos de Vista
- **Quarter Day**: Vista detallada por cuarto de día
- **Half Day**: Vista por medio día
- **Day**: Vista diaria (por defecto)
- **Week**: Vista semanal
- **Month**: Vista mensual

#### Interacciones
- **Clic**: Ver descripción completa
- **Arrastrar barra**: Cambiar fechas de inicio/fin
- **Arrastrar progreso**: Ajustar % de avance
- **Hover**: Mostrar información detallada

### ☁️ Sincronización Online

#### Cargar Datos
1. Haz clic en **"📥 Cargar Data"**
2. Los datos se importarán desde Google Sheets
3. Las tareas locales serán reemplazadas

#### Sincronizar Cambios
1. Haz clic en **"☁️ Sincronizar Online"**
2. Los datos locales se subirán a Google Sheets
3. Confirmación visual del proceso

#### Estados de Sincronización
- **✅ Éxito**: Datos sincronizados correctamente
- **❌ Error**: Problema de conexión o permisos
- **ℹ️ Info**: Información del proceso

### 💾 Exportación y Backup

#### Descargar Archivo JS
- Exporta todas las tareas en formato JavaScript
- Útil para backup local o transferencia
- Archivo nombrado con fecha actual

#### Cargar Archivo JS
- Importa tareas desde archivo previamente exportado
- Reemplaza datos actuales (con confirmación)
- Valida formato antes de importar

#### Exportar PDF
- Genera documento profesional con:
  - Tabla completa de tareas
  - Diagrama de Gantt optimizado
  - Estadísticas del proyecto
  - Meses comprometidos destacados

### ⌨️ Atajos de Teclado

| Atajo | Acción |
|-------|--------|
| `Ctrl + N` | Agregar nueva tarea |
| `Ctrl + S` | Descargar archivo JS |
| `Ctrl + Shift + Backspace` | Eliminar última tarea |
| `Ctrl + Shift + L` | Cargar datos desde Google Sheets |
| `Ctrl + Shift + U` | Sincronizar con Google Sheets |

### 📱 Uso en Dispositivos Móviles

#### Adaptaciones Automáticas
- Interfaz responsiva que se adapta al tamaño de pantalla
- Botones y campos optimizados para touch
- Tabla con scroll horizontal en pantallas pequeñas
- Notificaciones adaptadas al viewport

#### Funcionalidades Táctiles
- Toca para editar campos
- Desliza para interactuar con controles
- Pellizca para hacer zoom en el diagrama

## 🔧 Personalización Avanzada

### Modificar Colores por Defecto
```javascript
// En la función addTask(), línea ~280
const hues = [200, 300, 120, 60, 0, 240, 180]; // Modifica estos valores
```

### Cambiar Configuración de Gantt
```javascript
// En la función renderGantt(), línea ~400
ganttChart = new Gantt('#gantt', ganttTasks, {
  header_height: 50,     // Altura del header
  column_width: 30,      // Ancho de columnas
  bar_height: 20,        // Altura de barras
  view_mode: 'Day',      // Modo de vista inicial
  // ... más opciones
});
```

### Personalizar Estados de Tarea
```javascript
// En createTableRow(), línea ~200
<option value="tu-estado">🔄 Tu Estado</option>
```

### Modificar Auto-guardado
```javascript
// Cambiar intervalo (línea ~800)
setInterval(() => {
  if (tasks.length > 0) {
    saveData();
  }
}, 30000); // 30 segundos (30000ms)
```

## 🐛 Solución de Problemas

### Problemas Comunes

#### Error de Sincronización
**Síntoma**: No se pueden cargar o sincronizar datos
**Solución**:
1. Verifica que la URL de SheetDB sea correcta
2. Confirma que la hoja de Google Sheets sea accesible
3. Revisa la conexión a internet
4. Comprueba los permisos de la hoja

#### Diagrama No Se Muestra
**Síntoma**: El área del Gantt aparece vacía
**Solución**:
1. Asegúrate de que las fechas estén en formato correcto (YYYY-MM-DD)
2. Verifica que las tareas no estén marcadas como "N/A"
3. Comprueba que la fecha de fin sea posterior a la de inicio
4. Revisa la consola del navegador para errores

#### Datos No Se Guardan
**Síntoma**: Los cambios se pierden al recargar
**Solución**:
1. Verifica que localStorage esté habilitado
2. Comprueba que no estés en modo incógnito
3. Asegúrate de que el dominio permita almacenamiento local
4. Usa la función de exportar JS como backup

#### Exportación PDF Falla
**Síntoma**: Error al generar PDF
**Solución**:
1. Verifica conexión a internet (librerías CDN)
2. Comprueba que el navegador soporte html2canvas
3. Reduce el número de tareas si es muy grande
4. Intenta en modo ventana normal (no pantalla completa)

### Limitaciones Conocidas

1. **Navegadores Antiguos**: Requiere navegador moderno con soporte ES6
2. **Almacenamiento Local**: Limitado a ~5MB por dominio
3. **SheetDB**: Límites de API según plan de suscripción
4. **Rendimiento**: Con >100 tareas puede haber lentitud

### Compatibilidad

#### Navegadores Soportados
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+
- ❌ Internet Explorer (no soportado)

#### Dispositivos Móviles
- ✅ Android 7+ (Chrome, Firefox)
- ✅ iOS 13+ (Safari, Chrome)
- ✅ Tablets (todos los tamaños)

## 🔐 Seguridad y Privacidad

### Datos Locales
- Los datos se almacenan en el navegador del usuario
- No se envían datos a servidores externos (excepto SheetDB)
- Uso de localStorage para persistencia

### Conexión SheetDB
- Conexión HTTPS segura
- API key protegida
- Datos encriptados en tránsito

### Recomendaciones
1. **Backup Regular**: Exporta tus datos periódicamente
2. **Acceso Controlado**: Configura permisos apropiados en Google Sheets
3. **URLs Privadas**: No compartas URLs de SheetDB públicamente
4. **Actualizaciones**: Mantén el código actualizado

## 🤝 Contribuciones

### Cómo Contribuir
1. Fork del proyecto
2. Crea una rama para tu feature
3. Implementa mejoras
4. Envía pull request

### Áreas de Mejora
- 🔄 Sincronización en tiempo real
- 📱 App móvil nativa
- 🎨 Más temas visuales
- 🔧 Configuración avanzada
- 📊 Más tipos de gráficos

## 📞 Soporte

### Contacto
- **Email**: 38514603@claro.com.co
- **GitHub**: [EstebanM007](https://github.com/EstebanM007)
- **Issues**: Reporta problemas en el repositorio

### Recursos Adicionales
- [Documentación de Frappe Gantt](https://frappe.io/gantt)
- [SheetDB API Documentation](https://sheetdb.io/docs)
- [Google Sheets API](https://developers.google.com/sheets/api)

---

## 📄 Licencia

© Todos los derechos reservados - Esteban Alberto Martinez Palacios

**Desarrollado por**: GEN XXI  
**Versión**: 1.0.0  
**Última actualización**: 2025

---

*¡Gracias por usar nuestro sistema de gestión de proyectos! Para más información y actualizaciones, visita nuestro repositorio en GitHub.*