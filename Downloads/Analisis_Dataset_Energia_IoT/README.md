# Análisis de Dataset: Consumo de Energía y Servicios Públicos Inteligentes

Proyecto académico en Python y Jupyter Notebook para resolver los ejercicios de Pandas del taller de Energía de Occidente.

## Estructura

- `AnalisisDatos.ipynb`: notebook con explicaciones, código y resultados de los ejercicios.
- `datos/consumo_energia_iot.csv`: dataset en CSV, sin columna de índice adicional.
- `datos/consumo_energia_iot_original.xlsx`: archivo Excel fuente entregado.
- `documentacion/Primeros_Pasos_configuracion.pdf`: guía de configuración inicial entregada.
- `requirements.txt`: dependencias del proyecto.
- `.gitignore`: excluye preferencias locales, entornos virtuales y archivos temporales.

## Requisitos

Tener Python instalado y la extensión **Python** y **Jupyter** de Microsoft en Visual Studio Code.

## Configuración en Windows (PowerShell)

Abre esta carpeta en Visual Studio Code y ejecuta en la terminal:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Si PowerShell bloquea la activación, puedes usar temporalmente:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
.\.venv\Scripts\Activate.ps1
```

Después, abre `AnalisisDatos.ipynb`, selecciona como kernel el Python del entorno `.venv` y pulsa **Ejecutar todo**.

## Configuración en macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Nota sobre el dataset fuente

El Excel recibido contiene **1.012 filas**, **1.000 identificadores de medidor únicos** y **12 filas duplicadas exactas** (es decir, 12 filas excedentes por duplicación). El enunciado menciona 1.000 lecturas; el notebook muestra esta diferencia y la comprueba antes y después de `drop_duplicates()`, sin borrar datos silenciosamente del archivo fuente.

Además, `Horas_Pico_kWh` venía almacenada como texto en el Excel. El CSV se exportó convirtiendo esa columna a valores numéricos, sin añadir una columna de índice. Los datos originales siguen disponibles en el archivo Excel.

## GitHub público

1. Crea un repositorio público en GitHub.
2. En la terminal, desde esta carpeta:

```bash
git init
git add .
git commit -m "Añade análisis de consumo energético con Pandas"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/TU-REPOSITORIO.git
git push -u origin main
```

Reemplaza la URL de ejemplo por la URL real de tu repositorio. No subas `.venv/` ni `.vscode/`.
