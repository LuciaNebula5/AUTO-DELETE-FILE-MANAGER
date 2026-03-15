# 🗑️ Auto-Delete Manager

Gestor automático de archivos temporales para Windows. Detecta archivos nuevos en carpetas específicas y los elimina automáticamente después del tiempo que configures.

## ✨ Características

- 📁 Monitoreo automático de carpetas (Downloads, Desktop, etc.)
- ⏰ Eliminación programada de archivos (1 hora, 24 horas, 7 días, 30 días)
- 🎯 Reglas automáticas por extensión de archivo
- 🗑️ Opción de papelera de reciclaje o eliminación permanente
- 📊 Estadísticas de espacio liberado
- 🚀 Inicio automático con Windows
- 💾 Interfaz sencilla y fácil de usar

## 📥 Instalación

### Opción 1: Ejecutable (.exe)
1. Descarga `AutoDeleteManager.exe` desde [Releases](../../releases)
2. Ejecuta el archivo
3. ¡Listo!

### Opción 2: Desde código fuente
```bash
# Clonar repositorio
git clone https://github.com/tu-usuario/auto-delete-manager.git
cd auto-delete-manager

# Instalar dependencias (opcional, para papelera de reciclaje)
pip install send2trash

# Ejecutar
python auto_delete_manager.py
```

## 🚀 Uso

1. **Primera vez:**
   - Abre la app
   - Ve a Configuración → Carpetas
   - Agrega las carpetas que quieres monitorear (ej: Downloads)

2. **Cuando descargas un archivo:**
   - Aparece un popup preguntando cuándo eliminarlo
   - Selecciona el tiempo: 1 hora, 24 horas, 7 días, 30 días, o Nunca
   - El archivo se eliminará automáticamente

3. **Reglas automáticas:**
   - Ve a Configuración → Reglas
   - Crea reglas por extensión (ej: `.tmp` → 1 hora)
   - Los archivos con esas extensiones se procesarán automáticamente sin popup

## ⚙️ Configuración

### Carpetas Monitoreadas
- Agrega/elimina carpetas a monitorear
- Por defecto: Downloads y Desktop

### Comportamiento
- Intervalo de revisión: 30 min / 1 hora / 4 horas
- Modo de eliminación: Papelera o Permanente
- Inicio automático con Windows

### Reglas Automáticas
- Define tiempos de eliminación por extensión
- Ejemplo: `.zip` → 3 días, `.tmp` → 1 hora

## 📋 Requisitos

- Windows 10/11
- Python 3.8+ (solo si ejecutas desde código fuente)
- `send2trash` (opcional, para papelera de reciclaje)

## 🛠️ Crear ejecutable
```bash
pip install pyinstaller
pyinstaller --onefile --windowed --name="AutoDeleteManager" auto_delete_manager.py
```

El ejecutable estará en `dist/AutoDeleteManager.exe`

## 📝 Notas

- **La app debe estar abierta** para monitorear archivos nuevos
- Marca "Inicio automático con Windows" para que se abra al encender el PC
- Si no instalas `send2trash`, los archivos se eliminarán permanentemente

## 🐛 Problemas comunes

**No detecta archivos nuevos:**
- Asegúrate de que la app está abierta
- Verifica que la carpeta está en Configuración → Carpetas

**Error con send2trash:**
- Instala: `pip install send2trash`
- O usa "Eliminar permanentemente" en Configuración

## 📄 Licencia

MIT License - Siéntete libre de usar y modificar. Pero menciona al autor siempre.

## 👤 Autor

@Lucix
Nebula Studios

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Abre un issue o pull request.
