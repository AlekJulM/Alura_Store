# AluraStoreLatam Analysis

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlekJulM/Alura_Store/blob/main/AluraStoreLatam.ipynb)

## Descripción General
AluraStoreLatam Analysis es un cuaderno de Jupyter (desarrollado en Google Colab) que ofrece un análisis exploratorio y descriptivo de las ventas, los costos de envío y los patrones de consumo en cuatro tiendas virtuales. A partir de datos almacenados en archivos CSV, el proyecto genera métricas clave (facturación total, ticket promedio, costo de envío medio), visualizaciones comparativas y tablas resumen para extraer insights accionables.

## Motivación del Proyecto
El comercio electrónico exige una comprensión detallada de los indicadores de venta y logística para optimizar decisiones estratégicas. Este proyecto nace de la necesidad de:

- Centralizar la evaluación de métricas de venta en múltiples tiendas.
- Identificar categorías de producto y regiones con mejor desempeño.
- Detectar oportunidades de mejora en costos de envío y eficiencia de ticket promedio.

## Tecnologías y Herramientas Utilizadas
- **Python 3.8+**
- **pandas**: Manipulación y análisis de datos tabulares.
- **NumPy**: Cálculos numéricos eficientes.
- **Matplotlib**: Generación de gráficos comparativos.
- **Jupyter Notebook / Google Colab**: Entorno interactivo.

## Instalación
Clona el repositorio y configura tu entorno local siguiendo estos pasos:

1. **Clonar el repositorio**
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd <NOMBRE_CARPETA>
   ```
2. **Crear y activar entorno virtual** (opcional pero recomendado):
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # macOS/Linux
   venv\\Scripts\\activate  # Windows
   ```
3. **Instalar dependencias**
   ```bash
   pip install --upgrade pip
   pip install pandas numpy matplotlib jupyter
   ```
4. **(Opcional) Generar `requirements.txt`**
   ```bash
   pip freeze > requirements.txt
   ```

## Uso
### Jupyter Local
1. Inicia el servidor:
   ```bash
   jupyter notebook AluraStoreLatam.ipynb
   ```
2. En la interfaz web, selecciona el notebook y ejecuta **Run All**.

### Google Colab
Haz clic en el badge "Abrir en Colab" al inicio de este README para iniciar el análisis sin configuración local.

> **Tip**: Verifica conexión a internet; los datos se obtienen desde GitHub.

## Estructura del Proyecto
```plaintext
base-de-datos-challenge1-latam/  # Directorio con los CSV de cada tienda
├── tienda_1.csv
├── tienda_2.csv
├── tienda_3.csv
└── tienda_4.csv

AluraStoreLatam.ipynb            # Notebook principal (Google Colab)
README.md                        # Documentación del proyecto
``` 

## Posibles Problemas y Soluciones Comunes
| Problema                                     | Solución                                                                    |
|----------------------------------------------|-----------------------------------------------------------------------------|
| `ModuleNotFoundError` al importar librerías  | Activa el entorno virtual y confirma instalación de `pandas`, `numpy`, `matplotlib`, `jupyter`. |
| Error de conexión al descargar CSV           | Verifica URLs o descarga manualmente los CSV al directorio `base-de-datos-challenge1-latam/`.   |
| Unidades de `Precio` incorrectas             | Confirma si `Precio` está en centavos o en moneda; ajusta o elimina la división `/100`.         |
| `Styler` no muestra tablas fuera de Jupyter  | Usa `df.to_markdown()` o exporta el notebook como HTML para conservar estilos. |
| Leyendas de gráficos solapadas               | Ajusta `figsize`, `plt.tight_layout()` o parámetros de la leyenda (ubicación, tamaño). |

## Pruebas
Actualmente no hay tests automatizados. Para validación manual:

1. Verifica la correcta suma de facturación.
2. Comprueba que las agrupaciones por categoría y región sean coherentes.
3. Asegura que los gráficos reflejen las métricas calculadas.

> **Recomendación**: Implementar `pytest` para cubrir funciones de cálculo y garantizar consistencia.

## Créditos
- **Autor**: Mikael – Estudiante de Ingeniería con enfoque en Machine Learning.
- **Datos**: Repositorio público de Alura Latam.
- **Inspiración**: Reto de análisis de datos de Alura Latam.

## Licencia
Este proyecto está bajo la licencia MIT. Consulta `LICENSE` para más información.

