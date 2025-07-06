
# 🔁 EasyBatcher Core - `batch_processor.py`

### Núcleo reutilizable para procesamiento en lote de entidades Python

**Versión:** 1.0  
**Autor:** Juanito Software  
**Correo de contacto:** [bernaldezperedaj@gmail.com](mailto:bernaldezperedaj@gmail.com)  
**Licencia:** Uso No Comercial (ver [LICENSE.txt](./LICENSE.txt))

---

## 📄 Descripción

`batch_processor.py` es un módulo central genérico y extensible para flujos de procesamiento de datos en lote. Está diseñado para funcionar con clases definidas por el usuario (usando `@dataclass`) y permite ejecutar un pipeline configurable desde múltiples fuentes (CSV, API REST o base de datos) hacia múltiples destinos, aplicando funciones transformadoras intermedias.

Este núcleo es ideal para construir ETLs livianas, migraciones de datos, sincronización entre sistemas, validaciones y transformaciones por lotes.

---

## 🚀 Características

- ✅ **Entrada y salida versátil**: trabaja con CSV, APIs o bases de datos.
- 🔄 **Pipeline genérico**: define funciones que transformen objetos de forma modular.
- 🧠 **Conversión automática** entre `pandas.DataFrame` y objetos Python (`dataclass`).
- 🔧 **Orquestador interactivo**: configura el flujo completo desde la terminal.
- 🧪 **Procesamiento de prueba**: incluye funciones de ejemplo (`strip_whitespace`, `noop`).
- 🧩 **Modularidad completa**: fácilmente extensible con más fuentes, destinos o pasos.

---

## 🧰 Requisitos

- Python 3.9 o superior
- Bibliotecas:
  - `pandas`
  - `requests`
  - `sqlalchemy`
  - `psycopg2` (para bases de datos PostgreSQL)

Instalación recomendada:

```bash
pip install pandas requests sqlalchemy psycopg2
```

---

## 🧠 Estructura de uso

### 1. Define tu clase de entidad

Ejemplo:
```python
from dataclasses import dataclass

@dataclass
class Persona:
    id: int
    first_name: str
    last_name: str
```
### 2. Ejecuta el pipeline

```python
from batch_processor import run_pipeline

run_pipeline(Persona)
```

El script pedirá en consola:

- Tipo de entrada (`csv`, `api`, `db`)
- Ruta de entrada (archivo CSV, URL o string de conexión SQLAlchemy)
- Tipo de salida
- Ruta de salida (formato similar al anterior)
- Si se selecciona base de datos, se pedirá el nombre de la tabla

---

## 🔂 Flujo general del proceso

1. **Lectura**: Se cargan los datos desde la fuente elegida.
2. **Conversión**: Se transforman en objetos `dataclass`.
3. **Procesamiento**: Se ejecutan funciones tipo `T → T` en un pipeline.
4. **Salida**: Se escriben los resultados en el destino configurado.

---

## 🔧 Personalización

### ➕ Añadir pasos al pipeline

Puedes definir funciones como:

```python
def to_uppercase(obj: Persona) -> Persona:
    obj.first_name = obj.first_name.upper()
    return obj
```

Y agregarlas:

```python
proc = Processor[Persona]()
proc.add(strip_whitespace)
proc.add(to_uppercase)
```

### ➕ Cambiar origen/destino por defecto

Modifica los valores en la sección `# CONFIGURACIÓN` del script:

```python
INPUT_TYPE = 'api'
OUTPUT_TYPE = 'db'
```

---

## 📦 Estructura de Archivos Recomendada

```
/EasyBatcher/
│
├── batch_processor.py         # Este script
├── LICENSE.txt                # Condiciones de uso
├── input_personas.csv         # (Ejemplo de entrada)
├── output_personas.csv        # (Archivo de salida)
├── main.py                    # Tu punto de entrada con una clase concreta
└── README.md                  # Esta ficha técnica
```

---

## ⚠️ Licencia

Este programa está protegido por una **Licencia de Uso No Comercial**:

- ✅ Se permite su uso gratuito en contextos personales, académicos o de investigación.
- 🚫 No se permite el uso comercial, redistribución modificada ni ingeniería inversa.
- 🧾 Este aviso debe mantenerse intacto.

Más detalles en el archivo `LICENSE.txt`.

---

## 🗃️ Posibles mejoras futuras

- Agregar validación automática de esquemas con `pydantic`
- Interfaz gráfica mínima con `Tkinter` o `PyQt`
- Logging estructurado en lugar de `print`
- CLI con `argparse` o `Typer`
- Compatibilidad con más bases de datos (MySQL, SQLite, etc.)

---

## 📬 Contacto

Para dudas, colaboraciones o sugerencias:

📧 **bernaldezperedaj@gmail.com**

---
