# 🧾 GPTDevTeam - Ficha Técnica

## 🧠 Descripción General

**Juanito Software 2025** es un sistema automatizado de generación, validación, ejecución y documentación de código Python utilizando modelos de lenguaje basados en LLMs como **CodeLlama-GPTQ** y **CodeGemma**. Está diseñado para crear scripts funcionales, corregir errores automáticamente, validar su ejecución y documentar el código generado.

## 👨‍💻 Desarrollador

**GPTDevTeam**

---

## 🧱 Componentes Principales

- **CodeLlama-7B-GPTQ**: Modelo LLM cuantizado para generación de código.
- **CodeGemma (Ollama)**: LLM para documentación automática vía API local.
- **Transformers** (HuggingFace): Tokenización y manipulación del modelo.
- **Triton / Torch / CUDA**: Infraestructura para ejecución en GPU.
- **Subprocess / threading**: Control de ejecución del código generado.

---

## ⚙️ Requisitos del Sistema

### Dependencias de Python:

```bash
transformers
torch
triton
requests
textwrap
huggingface_hub
```

### Requisitos del sistema:

- Python 3.8+
- GPU compatible con CUDA
- [Ollama](https://ollama.com/) corriendo localmente en `localhost:11434`
- Memoria recomendada: 16 GB RAM / 12 GB VRAM
- Acceso a internet (opcional, si se usan modelos locales ya descargados)

---

## 🧩 Estructura del Programa

- `main()`: Orquestador general del flujo de trabajo.
- `codellama_generate(prompt)`: Generación de código a partir de una instrucción.
- `build_codellama_prompt(code)`: Generación de prompts de refactorización.
- `ejecutar_codigo_py(path)`: Ejecuta el código generado y verifica su funcionamiento.
- `extraer_codigo_puro(texto)`: Limpia la salida de los LLMs para extraer solo el código.
- `documentar_codigo(codigo)`: Usa CodeGemma para comentar el código.
- `limpiar_docstring_inicial(codigo)`: Elimina docstrings incorrectos o mal formateados.

---

## 🔁 Flujo de Ejecución

1. Se genera un script Python a partir de una descripción en lenguaje natural.
2. El código se limpia y formatea.
3. Se corrige iterativamente con un máximo de 4 intentos si contiene errores.
4. Se ejecuta en tiempo real y se monitorea por errores.
5. Si la ejecución es exitosa, se documenta automáticamente.
6. El código final se guarda como `CodigoFinal.py`.

---

## 📦 Salidas

- `codigo_actual.py`: Código intermedio a ejecutar/testear.
- `CodigoFinal.py`: Código funcional y documentado.
- Logs en consola: estado de cada intento de ejecución y errores detectados.

---

## 🛡️ Validación de Ejecución

El código generado se ejecuta automáticamente. Si contiene errores, se depura con ayuda del propio modelo, reutilizando el mensaje de error como parte del nuevo prompt.

---

## 🌐 Conectividad

- Ollama debe estar corriendo localmente.
- El modelo "codegemma:7b-instruct" debe estar disponible para generar documentación.

---

## 📚 Licencias y Créditos

- Modelos LLM proporcionados por [TheBloke](https://huggingface.co/TheBloke) y [Google](https://github.com/google/codegemma).
- Uso de Transformers y HuggingFace Hub bajo licencia Apache 2.0.
- Este software es de uso experimental/educativo y no garantiza código seguro en entornos de producción.

---

## 🏁 Ejecución

```bash
python main.py
```

---

## 🚨 Notas de Seguridad

- **No ejecutar el código generado sin revisión manual previa en entornos sensibles.**
- **El sistema puede generar código no seguro si el prompt lo induce.**

---

## 📃 Licencia

Este programa es software libre: puedes redistribuirlo y/o modificarlo bajo los términos de la Licencia Pública General de GNU, versión 3 o cualquier versión posterior.

Consulta la licencia completa para más detalles.
Más información: [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html)

© 2025 JuanitoSoftware

---

## 📬 Contacto

📧 bernaldezperedaj@gmail.com
