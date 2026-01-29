# Documentación de Notebooks

Este repositorio contiene varios cuadernos de Jupyter que se utilizan para diferentes propósitos.

##  Web scraping /scraping

| Nombre del Cuaderno | Descripción |
|---------------------|-------------|
| `scraping_pccomponentes.ipynb` | Este cuaderno se utiliza para realizar scraping de datos de componentes de PC. |
| `scraping_processors.ipynb` | Este cuaderno se utiliza para realizar scraping de datos de procesadores. |
| `scraping_pcpartpicker.ipynb` | Este cuaderno se utiliza para realizar scraping de datos de PCPartPicker. |


## Dataset

| Nombre del Cuaderno | Descripción |
|---------------------|-------------|
| `dataset_01.ipynb` | Este cuaderno se utiliza para crear el conjunto de datos que se empleará para entrenar nuestro modelo. |
| `dataset_02.ipynb` | Este cuaderno se utiliza para descargar las imágenes y crear el conjunto de datos definitivo, incluyendo la ubicación de cada imagen. |

## 🐳 Ejecutar con Docker

### 1. Construir y levantar el contenedor

```bash
docker build -f notebooks/Dockerfile.jupyter -t jupyter-python .
```

```bash
docker run -p 8888:8888 -v ${PWD}:/app jupyter-python
```

### 2. Abrir en el navegador

```
http://localhost:8888/tree
```