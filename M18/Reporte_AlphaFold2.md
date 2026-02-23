# Reporte de Actividad
*Dulce Alejandra Carrillo Carlos*

## 1. Predicción de Estructura con AlphaFold2

El objetivo de esta actividad fue predecir la **estructura terciaria de la proteína p53**, una proteína supresora de tumores clave que desempeña un papel fundamental en la regulación del ciclo celular, la reparación del ADN y la apoptosis. Debido a su relevancia biológica y clínica, comprender su estructura tridimensional resulta esencial para estudiar su función y dinámica molecular.

### Metodología

**Obtención de la secuencia:**
La secuencia aminoacídica de p53 fue descargada desde la base de datos UniProt.

Archivo utilizado:
`p53.fasta`

**Predicción estructural:**
La secuencia fue utilizada como entrada en **AlphaFold2** mediante la implementación accesible en **ColabFold**.

Directorio de resultados:
`alpha_fold2/p53_7c637/p53_7c637_env`

El modelo generado corresponde a:

`p53_7c637_unrelaxed_rank_001_alphafold2_ptm_model_3_seed_000.pdb`

Este modelo representa la predicción estructural con mayor puntuación de confianza dentro del conjunto generado.

## 2. Validación de la Estructura

Para evaluar la calidad del modelo predicho, se realizó un análisis estructural utilizando herramientas estándar de validación.

### Herramientas utilizadas

**SAVES (Structure Analysis and Verification Server):**
Este metaservidor permite evaluar la calidad estructural de modelos proteicos mediante múltiples métricas, incluyendo:

* Geometría estereoquímica
* Energía estructural
* Compatibilidad secuencia-estructura

Resultados almacenados en:
`SAVES_results/`


**Swiss-Model (Structure Assessment):**
Se utilizó el módulo de evaluación estructural para analizar:

- Calidad global del modelo
- Consistencia estructural
- Posibles regiones problemáticas

Resultados en:
`swiss_results/`

## 3. Interpretación de Resultados

El análisis conjunto de las herramientas de validación permitió evaluar la confiabilidad del modelo predicho por AlphaFold2.

En términos generales:

- La estructura mostró una **geometría adecuada**, consistente con proteínas globulares.
- Se observaron **regiones bien definidas**, particularmente en dominios funcionales estructurados.
- Algunas zonas presentaron **menor confianza estructural**, lo cual es esperable en regiones intrínsecamente desordenadas de p53.

Esto concuerda con el conocimiento previo de que p53 contiene:

- Dominios estructurados (ej. dominio de unión al ADN)
- Regiones flexibles o desordenadas (ej. extremos N y C terminales)

El análisis detallado de métricas específicas y su interpretación se encuentra documentado en:

`Resultados.md`


