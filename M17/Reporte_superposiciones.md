# Reporte
**Dulce Alejandra Carrillo Carlos**

El análisis estructural de proteínas es una herramienta que permite evaluar relaciones evolutivas, funcionales y conformacionales más allá de la simple comparación de secuencias. Aunque la secuencia primaria puede variar considerablemente entre proteínas, su estructura tridimensional tiende a estar más conservada, lo que convierte a la superposición estructural en una estrategia clave para estudiar similitudes biológicas.

En este ejercicio se realizó un análisis comparativo de dominios proteicos pertenecientes a una misma superfamilia en la base de datos CATH. A partir de la selección de un dominios, se identificaron similitudes estructurales mediante Foldseek y posteriormente se calcularon dos métricas fundamentales: el porcentaje de identidad de secuencia y el RMSD (Root Mean Square Deviation).

Para ello, se modificó un script en Python con el objetivo de automatizar el cálculo de ambas métricas y evaluar cuantitativamente el grado de similitud entre pares de estructuras seleccionadas. Este enfoque permitió relacionar directamente la conservación de secuencia con la similitud estructural observada.

## 1. Selección de dominios

CATH (https://www.cathdb.info), se escogió un clúster perteneciente a una superfamilia CATH que contiene 12 dominios.

## 2. Búsqueda de similitudes estructurales

Se alinearon los dominios seleccionados utilizando Foldseek (https://search.foldseek.com/foldmason). 
Los resultados obtenidos con Foldseek (foldmason) se encuentran en: [Foldmason](./Foldmason/)

## 3. Selección de estructuras 

Para calcular el porcentaje de identidad y el RMSD seleccionamos aleatoriamente dos estructuras en el Guide Tree generado por Foldseek y se descargaron us PDB corespondientes

- 3BD4cif_A
- 3BDBcif_F

## 4. Resultados

Los resultados numéricos del análisis se encuentran en la carpeta:

- [results](./results/)

En la misma carpeta se incluye, además, un [archivo Markdown](./results/results.md) con la interpretación de dichos resultados.
