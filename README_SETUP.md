# 🚀 ETL UNICOS - Configuración Completa

## ✅ Estado del Entorno

Tu entorno está completamente configurado. Todo está listo para usar.

### Ubicaciones clave:

```
Virtual Environment: /home/codevars/Projects/etl_env/
Notebook: /home/codevars/Projects/ETL_EXCEL APUS/ETL_UNICOS_XLSX.ipynb
Script activación: /home/codevars/Projects/activate_etl.sh
```

---

## 🎯 Cómo usar desde VSCode

### Opción 1: VSCode + Extension Jupyter (Recomendado)

1. **Abre el notebook** en VSCode:
   - Click derecho en `ETL_UNICOS_XLSX.ipynb`
   - "Open with... Jupyter Notebook"

2. **Selecciona el kernel**:
   - Arriba a la derecha verás "Select Kernel"
   - Elige: **"Python ETL (venv)"** (el que acabamos de crear)
   - Si no aparece, presiona `Ctrl+Shift+P` y busca "Jupyter: Select Kernel"

3. **Ejecuta las celdas**:
   - Ctrl+Enter: ejecuta una celda
   - Ctrl+Shift+Enter: ejecuta y va a la siguiente
   - O usa el botón ▶ en cada celda

---

### Opción 2: Terminal + JupyterLab (Alternativa)

```bash
# Abre una terminal en el directorio del proyecto
cd /home/codevars/Projects/ETL_EXCEL\ APUS

# Activa el entorno
source ../activate_etl.sh

# O manualmente:
source ../etl_env/bin/activate

# Inicia JupyterLab
jupyter lab

# O Jupyter Notebook
jupyter notebook
```

Luego se abrirá en el navegador. Selecciona el kernel "Python ETL (venv)" al abrir el notebook.

---

## 📦 Dependencias Instaladas

| Librería | Versión | Propósito |
|----------|---------|----------|
| `pandas` | 3.0.0 | Manipulación de datos |
| `numpy` | 2.4.2 | Operaciones numéricas |
| `openpyxl` | 3.1.5 | Lectura/escritura Excel |
| `ipywidgets` | 8.1.8 | UI interactiva en notebook |
| `jupyter` | 1.1.1 | Entorno Jupyter |
| `python-calamine` | 0.6.1 | ⚡ Lectura ultra-rápida de Excel |
| `itables` | 2.7.0 | 📊 Tablas interactivas |
| `ipykernel` | 7.1.0 | Kernel para VSCode/Jupyter |

---

## 🔧 Resolución de Problemas

### ❌ "Kernel not found" o "ipykernel not installed"

**Solución:**
```bash
# Activa el entorno manualmente
source /home/codevars/Projects/etl_env/bin/activate

# Reinstala ipykernel
pip install ipykernel --force-reinstall

# Registra el kernel
python -m ipykernel install --user --name etl_env --display-name "Python ETL (venv)"
```

### ❌ "ipywidgets not working" en VSCode

**Solución:**
Asegúrate de usar el kernel **"Python ETL (venv)"**. VSCode a veces requiere recargar la ventana después de cambiar kernel.

### ❌ "pandas/openpyxl not found"

**Solución:**
```bash
# Verifica que el entorno esté activado
source /home/codevars/Projects/etl_env/bin/activate

# Instala específicamente
pip install pandas openpyxl
```

### ❌ "python-calamine import error"

**Solución (opcional):**
El notebook funciona sin `python-calamine` usando `openpyxl`. Si quieres instalarlo:

```bash
source /home/codevars/Projects/etl_env/bin/activate
pip install python-calamine
```

---

## 🎬 Quick Start (en VSCode)

1. **Abre**: `ETL_UNICOS_XLSX.ipynb`
2. **Selecciona kernel**: "Python ETL (venv)" (arriba a la derecha)
3. **Ejecuta todas las celdas**: Ctrl+Shift+Enter en cada una o usa el ▶ "Run All"
4. **Sube tu archivo Excel** en el widget
5. **Configura parámetros** (opcional)
6. **Click en "Ejecutar ETL"** (botón verde)
7. **Visualiza resultados**: Ejecuta la celda con `display_results()`
8. **Exporta**: Ejecuta `export_results()`

---

## 📚 Documentación del Notebook

El notebook incluye:

- **Celda 1-2**: Setup e introducción
- **Celda 3**: Configuración global
- **Celda 4**: Panel de controles (UI)
- **Celda 5-9**: Funciones ETL
- **Celda 10-11**: Ejecución y resultados
- **Celda 12-13**: Visor e exportación

---

## 🚨 Importante

- **No modifiques** el directorio `/home/codevars/Projects/etl_env/` manualmente
- Para instalar más paquetes: primero activa el entorno (`source .../etl_env/bin/activate`), luego `pip install ...`
- El notebook es **completamente independiente**: todas las dependencias están dentro del venv

---

## 💡 Tips

### Ver versiones instaladas:
```bash
source /home/codevars/Projects/etl_env/bin/activate
pip list
```

### Salir del entorno:
```bash
deactivate
```

### Eliminar el entorno (si necesitas empezar de cero):
```bash
rm -rf /home/codevars/Projects/etl_env
```

---

**¡Todo está listo! 🎉** Abre el notebook y empieza a procesar tus archivos Excel.
