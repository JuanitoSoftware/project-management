
# 📦 Transferencia de Archivos - Versión TCP - Ficha Técnica

**Autor:** JuanitoSoftware&Games  
**Licencia:** [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.html)  
**Versión:** 1.0  
**Lenguaje:** Python 3.x  
**Interfaz:** GUI (Tkinter)  
**Última actualización:** 2025

---

## 🧾 Descripción

Aplicación de escritorio en Python con interfaz gráfica basada en `Tkinter` que permite la **transferencia de archivos punto a punto (P2P)** a través del protocolo **TCP/IP** en red local.  
Incorpora medidas básicas de seguridad utilizando un sistema de direcciones hash personalizadas basadas en el nombre del usuario, como autenticación del destinatario.

---

## 🎯 Funcionalidades principales

- 🌐 **Obtención automática de IP local**
- 🧠 **Generación de dirección única** por usuario (hash SHA-256)
- 🔐 **Validación del receptor** mediante coincidencia de hash
- 📤 **Envío de archivos** a una IP y dirección hash específicas
- 📥 **Recepción automática** de archivos
- 🪄 **Efecto visual opcional** `matrix_effect.exe` al iniciar
- 🧾 Interfaz intuitiva y fácil de usar basada en `Tkinter`

---

## 🚀 Cómo ejecutar

1. Asegúrate de tener Python 3 instalado en tu sistema.
2. Coloca `matrix_effect.exe` (opcional) en el mismo directorio que el script.
3. Ejecuta el script con:

```bash
python archivo_transferencia.py
```

---

## 📁 Estructura de carpetas

```plaintext
proyecto/
├── archivo_transferencia.py
├── matrix_effect.exe         # (opcional)
└── received_files/           # Carpeta donde se guardan los archivos recibidos
```

---

## 🔒 Seguridad básica

- Cada usuario genera su "dirección" mediante:
  - Nombre introducido ➡️ caracteres aleatorios intercalados ➡️ hash SHA-256.
- Solo se aceptan archivos si el hash del remitente coincide con el propio.

---

## 🛠️ Requisitos

### Python
- `tkinter`
- `socket`
- `hashlib`
- `json`
- `threading`
- `subprocess`
- `os`
- `sys`
- `random`
- `string`

(Todos estos módulos son estándar en Python, no se requieren dependencias externas)

---

## 🧪 Detalles técnicos

- **Puerto usado:** `5001` TCP
- **Tamaño de buffer:** `4096 bytes`
- **Formato del header:** JSON serializado con tamaño prefijado (4 bytes)
- **Transmisión:** Se realiza por bloques hasta completar el archivo

---

## ❗ Posibles errores

- Si `matrix_effect.exe` no está disponible, se omite sin afectar la funcionalidad.
- Si se introduce un hash incorrecto, el archivo será rechazado silenciosamente.
- El sistema no incluye cifrado; se recomienda usar en entornos de confianza.

---

## 📃 Licencia

Este programa es software libre: puedes redistribuirlo y/o modificarlo bajo los términos de la Licencia Pública General de GNU, versión 3 o cualquier versión posterior.

Consulta la licencia completa para más detalles.
Más información: [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html)

© 2025 JuanitoSoftware

---

## 📬 Contacto

📧 bernaldezperedaj@gmail.com
