# 🖥️ SystemInfoApp

**SystemInfoApp** es una aplicación de escritorio desarrollada en Python con interfaz gráfica (Tkinter) que permite visualizar en tiempo real información avanzada del sistema operativo, procesador, memoria RAM, tarjeta gráfica, almacenamiento y otros componentes clave del equipo. 

Combina múltiples fuentes (WMI, XML, psutil, CPU-Z, etc.) y presenta la información de forma organizada y visual, incluyendo gráficos en tiempo real de uso y temperatura de CPU y GPU.

## 📦 Características principales

- Información detallada del sistema operativo (versión, build).
- Datos del procesador (nombre, núcleos, subprocesos, frecuencia).
- Lectura de temperatura y uso del CPU (WMI).
- Detección de tarjetas gráficas (GPU) con estadísticas de carga y temperatura.
- Visualización del uso y capacidad de la memoria RAM.
- Detalles del almacenamiento total, usado y libre.
- Identificación de la placa base (mediante XML y WMI).
- Interfaz gráfica elegante y en tiempo real con soporte para gráficos (`matplotlib`).
- Barra de progreso animada de carga inicial (`progress_bar_utils`).
- Manejo de múltiples hilos con `ThreadPoolExecutor`.
- Mecanismos de limpieza segura y control de señales del sistema (`SIGINT`, `SIGTERM`).
- Logging detallado en archivo (`log_ejecucion.txt`).

## 🔧 Requisitos

### Python
- Python 3.8 o superior

### Dependencias principales

| Módulo | Descripción |
|--------|-------------|
| `tkinter` | Interfaz gráfica |
| `psutil` | Estadísticas de CPU, RAM, procesos |
| `wmi` | Consulta avanzada del sistema (solo Windows) |
| `GPUtil` | Información de la GPU |
| `matplotlib` | Gráficos de uso/temperatura |
| `cpuinfo` | Información del procesador |
| `tabulate` | Formato de salida tabular (si se utiliza en consola) |
| `progress_bar_utils` | Utilidad personalizada para mostrar barra de progreso animada |
| `xml.etree.ElementTree` | Lectura de archivos XML de CPU-Z y otros |
| `concurrent.futures` | Manejo de tareas en segundo plano |
| `logging` | Registro de actividad del sistema |

## 🚀 Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/tuusuario/SystemInfoApp.git
cd SystemInfoApp
```

2. Instala las dependencias:

```bash
pip install -r requirements.txt
```

## ▶️ Ejecución

```bash
python main.py
```

---

## 📃 Licencia

Este programa es software libre: puedes redistribuirlo y/o modificarlo bajo los términos de la Licencia Pública General de GNU, versión 3 o cualquier versión posterior.

Consulta la licencia completa para más detalles.

© 2025 JuanitoSoftware
