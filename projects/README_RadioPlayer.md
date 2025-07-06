# 📻 Radio Player - Ficha Técnica

### Desarrollado por **JuanitoSoftware&Games** – 2025  
Licencia: [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.html)

---

## 🧾 Descripción

**Radio Player** es una aplicación de escritorio desarrollada en Python con interfaz gráfica basada en **Tkinter**. Permite reproducir emisoras de radio por streaming usando **VLC**, con una interfaz intuitiva, compatible con modo día/noche, e integrada con un efecto visual estilo "Matrix" previo a la ejecución del reproductor.

---

## 🛠️ Características principales

- 🎧 Reproductor de radio streaming con motor **python-vlc**.
- 📋 Lista de emisoras cargadas desde archivo CSV (`Radios.csv`).
- 🌓 Alternancia de **modo claro / modo noche**.
- 🖱️ Reproducción mediante doble clic, botón o teclas (`Space`/`Enter`).
- 🟩 Efecto inicial `matrix_effect.exe` (estilo consola Matrix).
- ❌ Botón de detener reproducción.
- 🪟 Interfaz gráfica multiplataforma basada en `tkinter`.

---

## 🗃️ Estructura de archivos

```
📁 Proyecto/
├── matrix_effect.exe         # Efecto visual Matrix (opcional pero recomendado)
├── Radios.csv                # Archivo con lista de emisoras (nombre,url)
├── radio_player.py           # Código fuente principal
```

---

## 📝 Formato del archivo `Radios.csv`

```csv
Nombre,URL
Radio Nacional,http://stream.radio1.com
Rock FM,http://stream.rockfm.com
...
```

---

## 🚀 Requisitos del sistema

- Python 3.7 o superior  
- VLC Media Player instalado (para soporte de `python-vlc`)  
- Sistema operativo: Windows, macOS o Linux  
- Paquetes Python:

```bash
pip install python-vlc
```

---

## ▶️ Cómo usar

1. Asegúrate de tener `matrix_effect.exe` en la misma carpeta (opcional).
2. Asegúrate de tener un archivo válido `Radios.csv`.
3. Ejecuta el script:

```bash
python radio_player.py
```

---

## 🔧 Atajos y controles

- **Doble clic** en una emisora → Reproduce
- **Enter o Barra espaciadora** → Reproducir / Pausar
- **Botón "Detener"** → Detiene la reproducción
- **Botón "🌙"** → Alternar modo claro/noche

---

## ⚙️ Compilación a ejecutable (opcional)

Si deseas generar un `.exe` para Windows con PyInstaller:

```bash
pyinstaller --noconsole --add-data "Radios.csv;." radio_player.py
```

_Asegúrate de incluir `matrix_effect.exe` en el mismo directorio que el `.exe` resultante._

---

## 📃 Licencia

Este programa es software libre: puedes redistribuirlo y/o modificarlo bajo los términos de la Licencia Pública General de GNU, versión 3 o cualquier versión posterior.

Consulta la licencia completa para más detalles.
Más información: [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html)

© 2025 JuanitoSoftware

---

## 📬 Contacto

📧 bernaldezperedaj@gmail.com
