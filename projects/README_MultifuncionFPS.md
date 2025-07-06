# MultifuncionFPS - Ficha Técnica

## Información General

**Nombre del programa:** MultifuncionFPS  
**Autor:** JuanitoSoftware&Games  
**Año:** 2025  
**Licencia:** GNU GPL v3 o superior  
**Lenguaje:** Python 3.x  
**Plataforma:** Windows (requiere módulos y utilidades específicas para Windows)  
**Dependencias principales:**  
- Python estándar: `configparser`, `tkinter`, `threading`, `subprocess`, `os`, `sys`, `ctypes`  
- Paquetes externos: `Pillow (PIL)`, `win32gui`, `win32con`, `winreg`, `ultralytics` (YOLO), `cv2` (OpenCV), `numpy`, `mss`, `keyboard`  

---

## Descripción

MultifuncionFPS es una herramienta avanzada para jugadores y usuarios que buscan mejorar su experiencia en juegos FPS y aplicaciones relacionadas con la detección visual y la personalización del cursor (crosshair). Combina funcionalidades de:

- **Overlay de mira (crosshair) personalizable** con opciones de transparencia, escala y selección entre varias imágenes.
- **Detección de movimiento** en pantalla, con dos modos: estático (detección básica por diferencia de frames) y avanzado con inteligencia artificial (modelo YOLO para detección de personas en tiempo real).
- **Control y ajuste de aceleración y sensibilidad del ratón** a nivel de sistema operativo Windows.
- **Integración de efectos visuales externos**, como la ejecución de un efecto "Matrix" en consola.
- **Soporte para hotkeys globales** (`Ctrl+I`, `Ctrl+O`, `Ctrl+P`) para control sin ventana.
- **Overlays transparentes y click-through** para mostrar elementos sobre otras ventanas sin bloquear interacción.

---

## Arquitectura y Componentes

### Clases principales

- `App`: Controla interfaz, configuración, eventos y overlays.
- `CrosshairOverlay`: Overlay transparente para mostrar la mira.
- `MotionOverlay`: Overlay para la detección de movimiento visual.

### Funcionalidad clave

- Configuración por archivo `.ini`
- Detección de movimiento por diferencias de imagen o con IA (YOLOv8)
- Overlays interactivos con click-through
- Hilos para hotkeys y procesamiento en segundo plano
- Modificación del registro de Windows

---

## Requisitos de instalación

- Python 3.8 o superior  
- Instalación de dependencias:

```bash
pip install pillow pywin32 opencv-python numpy mss keyboard ultralytics
```

- Archivos necesarios:
  - Carpeta `crosshairs/` con imágenes `.png`
  - Ejecutable `matrix_effect.exe`
  - Carpeta `FloatTrans/` con `FloatTrans.exe` y `config.ini`
  - Modelo YOLOv8 (`yolov8s.pt`)

---

## Uso

1. Ejecutar el script principal.
2. Controlar funciones desde la interfaz o usar los siguientes **atajos globales**:
   - `Ctrl+I`: Activar detección de movimiento
   - `Ctrl+O`: Activar/ocultar mira
   - `Ctrl+P`: Cambiar a siguiente mira

---

## Estructura de Carpetas

```
/MultifuncionFPS
│
├── crosshairs/
├── FloatTrans/
├── matrix_effect.exe
├── multifuncionfps.py
└── yolov8s.pt
```

---

## Contacto

**Autor:** JuanitoSoftware&Games  
**Ubicación:** Santa Maria de Cayon, Cantabria, España  

---

## Opinión personal

Este software es un ejemplo sobresaliente de herramientas gamer con superposición visual avanzada, personalización total, y visión por computador. Su arquitectura modular permite ampliaciones futuras (grabación de clips, integración con OBS, IA contextual, etc.). Está optimizado para entornos Windows y es ideal para jugadores.

---

## 📃 Licencia

Este programa es software libre: puedes redistribuirlo y/o modificarlo bajo los términos de la Licencia Pública General de GNU, versión 3 o cualquier versión posterior.

Consulta la licencia completa para más detalles.
Más información: [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html)

© 2025 JuanitoSoftware

---

## 📬 Contacto

📧 bernaldezperedaj@gmail.com
