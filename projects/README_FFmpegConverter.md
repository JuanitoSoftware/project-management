# Ficha Técnica - FFmpeg Audio Converter GUI

## 🧾 Información General

- **Nombre del Proyecto:** FFmpeg Audio Converter GUI
- **Versión:** 1.0.0
- **Autor:** Juanito Software
- **Licencia:** [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.html)
- **Lenguaje:** Python 3
- **Interfaz Gráfica:** PyQt5
- **Dependencias Externas:** FFmpeg (GPLv3)
- **Fecha de Publicación:** 2025-07-06

## 📝 Descripción

Aplicación de escritorio con interfaz gráfica para convertir archivos de audio entre distintos formatos usando FFmpeg. Permite seleccionar carpetas de origen y destino, elegir formatos de entrada/salida y visualizar un log de progreso.

## 🎯 Funcionalidades Principales

- Selección de carpeta de origen y carpeta de destino.
- Conversión masiva de archivos de audio entre múltiples formatos.
- Interfaz amigable y responsiva desarrollada con PyQt5.
- Detección automática de FFmpeg en el sistema o uso de binarios embebidos.
- Log interactivo de operaciones realizadas y errores.

## 🔧 Tecnologías Utilizadas

| Tecnología | Descripción |
|------------|-------------|
| Python 3   | Lenguaje principal de desarrollo. |
| PyQt5      | Framework para la interfaz gráfica (GUI). |
| FFmpeg     | Backend para la conversión de audio. |

## 📦 Estructura del Proyecto

```
FFmpegConverter/
│
├── converter.ui             # Archivo de diseño de la interfaz (Qt Designer)
├── main.py                  # Código fuente principal
├── ffmpeg/ffmpeg.exe        # Binario embebido (opcional)
├── README.md                # Documentación general
└── LICENSE                  # Licencia GPLv3
```

## 🗂️ Formatos de Audio Soportados

Incluye, pero no se limita a:
aac, mp3, flac, wav, ogg, wma, alac, amr, opus, aiff, ac3, ra, tak, m4a, gsm, tta, w64, ape, atrac, mid, midi, entre muchos otros.

> Se pueden listar dinámicamente desde FFmpeg si se desea personalizar.

## ▶️ Requisitos de Ejecución

- **Sistema Operativo:** Windows, Linux o macOS
- **Python:** 3.6 o superior
- **Dependencias:**
  - `PyQt5`
  - `FFmpeg` (instalado en el sistema o incluido en la ruta local)

### Instalación de dependencias

```bash
pip install PyQt5
```

### Ejecución

```bash
python main.py
```

## 📌 Notas Adicionales

- Este software **no garantiza** la calidad de la conversión, depende de los códecs disponibles en FFmpeg.
- Si FFmpeg no está en el PATH del sistema, se puede incluir una versión local en el directorio `ffmpeg/`.

## ⚖️ 📃 Licencia
Este programa es software libre: puedes redistribuirlo y/o modificarlo bajo los términos de la Licencia Pública General de GNU, versión 3 o cualquier versión posterior.

Consulta la licencia completa para más detalles.

© 2025 JuanitoSoftware

Contacto: bernaldezperedaj@gmail.com
