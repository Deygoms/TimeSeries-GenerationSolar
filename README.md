# Análisis de Series de Tiempo - Parque Solar

Análisis de series temporales aplicado a datos de generación de un parque solar equipado con paneles Jinko Solar Tiger Neo JKM565N-72HL4.

## Descripción del Proyecto

Este proyecto implementa técnicas de análisis de series de tiempo en Python para estudiar y caracterizar el comportamiento de un sistema fotovoltaico. El análisis se centra en la identificación de patrones de generación, ciclos dominantes y características espectrales de la radiación solar y la potencia generada.

## Tecnologías Utilizadas

- **Python 3.12**
- **NumPy**: Procesamiento numérico y análisis matemático
- **Pandas**: Manipulación y análisis de datos
- **Matplotlib**: Visualización de datos
- **SciPy**: Análisis de señales y transformada de Fourier

## Estructura de Datos

Los datos de entrada se encuentran en formato CSV con la siguiente estructura:

| Timestamp | Generación [kW] | Radiación [W/m²] |
|-----------|----------------|------------------|
| 1/08/2025 0:00 | 0 | 0 |
| 1/08/2025 1:00 | 0 | 0 |
| 1/08/2025 7:00 | 91.788 | 63.123 |
| 1/08/2025 8:00 | 268.735 | 189.837 |
| ... | ... | ... |

**Características:**
- Resolución temporal: 1 hora
- Variables: Generación eléctrica (kW) y Radiación solar (W/m²)
- Formato de fecha: DD/MM/YYYY HH:MM

## Objetivos del Análisis

1. **Análisis Espectral**: Identificación de frecuencias dominantes mediante FFT (Fast Fourier Transform)
2. **Caracterización Temporal**: Estudio de patrones diarios, semanales y estacionales

### Requisitos Previos
```bash
pip install numpy pandas matplotlib scipy
```

### Ejecución
```python
# Cargar el notebook de Jupyter
jupyter notebook TrabajoF_seriesT.ipynb
```

O ejecutar directamente el script:
```python
python analisis_solar.py
```

## Estructura del Proyecto
```
.
├── TrabajoF_seriesT.ipynb    # Notebook principal con el análisis
├── datos/
│   └── datos_solar.csv       # Datos de generación y radiación
├── resultados/
│   ├── graficas/             # Visualizaciones generadas
│   └── reportes/             # Informes de análisis
└── README.md                 # Este archivo
```

## Metodología

### 1. Preprocesamiento de Datos
- Carga y limpieza de datos
- Conversión de timestamps
- Manejo de valores faltantes
- Normalización de series temporales

### 2. Análisis en el Dominio del Tiempo
- Estadísticas descriptivas
- Análisis de tendencias
- Detección de estacionalidad

### 3. Análisis en el Dominio de la Frecuencia
- Transformada rápida de Fourier (FFT)
- Identificación de ciclos dominantes
- Análisis de espectro de potencia
- Densidad espectral de potencia (PSD)

### 4. Visualización
- Gráficas de series temporales
- Espectros de frecuencia
- Diagramas de correlación

## Resultados Esperados

El análisis proporciona:
- **Frecuencias dominantes** en los datos de radiación y generación
- **Períodos característicos** del sistema (ciclo diario, patrones semanales)
- **Relación funcional** entre radiación y generación
- **Indicadores de desempeño** del sistema fotovoltaico

## Especificaciones del Sistema

**Paneles Solares**: Jinko Solar Tiger Neo JKM565N-72HL4

- Potencia nominal: 565 W
- Tecnología: Monocristalino PERC
- Eficiencia del módulo: ~21.8%

## Autor

**EquipoUTB**
- Universidad Tecnológica de Bolívar
- Maestría en Ingeniería Eléctrica
- Línea de investigación: Sistemas de energía renovable y optimización

## Licencia

Este proyecto está bajo las politicas de divulgación dadas por la Universidad Tecnológica de Bolivar

## Contacto

Para preguntas o colaboraciones, por favor abra un issue en el repositorio.

---

**Nota**: Este proyecto forma parte de la investigación en optimización de sistemas fotovoltaicos y aplicaciones de inteligencia artificial en sistemas energéticos.
