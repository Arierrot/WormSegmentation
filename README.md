# WormSegmentation
Desarrollé un método automatizado para segmentar C. elegans en imágenes del repositorio BBBC012v1 y detectar la expresión del gen clec-60. Utilicé imágenes multicanal y técnicas de procesamiento con OpenCV y tifffile para extraer los individuos, identificar la expresión en el canal GFP, la faringe en el canal mCherry y relacionar estas estructuras.

## Descripción

Se trabaja con imágenes multicanal en las que cada canal representa una información específica:
- **w1 (Campo claro)**: Imagen base de los individuos.
- **w2 (GFP)**: Canal fluorescente que indica la expresión del gen **clec-60**.
- **w3 (mCherry)**: Canal fluorescente que resalta la faringe del gusano.

A partir de estas imágenes, se implementa un pipeline de procesamiento de imágenes para:

1. **Segmentación de individuos**: Extracción automática de gusanos del fondo de la imagen.
2. **Detección de expresión génica**: Identificación de la expresión del gen **clec-60** en el canal GFP.
3. **Segmentación de la faringe**: Identificación de la faringe en el canal mCherry.
4. **Asociación de estructuras**: Relación de cada gusano con su expresión génica y faringe.

## Requisitos

Instala las dependencias necesarias ejecutando:
```
pip install -r requirements.txt
```

## Uso

Ejecuta celda por celda el notebook y observa las salidas.

## Datos

Las imágenes utilizadas provienen del conjunto **BBBC012v1**, disponible en la [Broad Bioimage Benchmark Collection](https://bbbc.broadinstitute.org/BBBC012).

## Tecnologías utilizadas

- **Python**  
- **OpenCV**  
- **tifffile**  
- **NumPy**  
- **Matplotlib**  

## Resultados

Se obtiene una estructura de datos que asocia a cada individuo con la ubicación de su faringe y la expresión génica detectada en el canal GFP.  
