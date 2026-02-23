# Protein Fold Recognition
*Dulce Alejandra Carrillo Carlos*

Problema clásico: tengo la secuencia de una proteína pero no sé cuál es su plegamiento ni su función.
Muchas veces la secuencia no se parece a casi nada en BLAST o FASTA, o solo a proteínas poco caracterizadas.

Idea clave: la estructura está más conservada que la secuencia.

Entonces lo que se hace es:
- Comparar la secuencia problema contra todos los plegamientos conocidos.
- Evaluar qué tan compatible es con cada uno.
- Obtener una lista ordenada de posibles folds.

Se usa especialmente cuando los métodos convencionales de búsqueda por secuencia fallan.

# Modelado por Homología

Se usa cuando:
- Tengo la secuencia de una proteína A.
- Quiero conocer (aunque sea de forma aproximada) su estructura tridimensional.
- Existe una proteína similar con estructura conocida (template).

Principio básico:
Si dos proteínas son similares en secuencia, probablemente también lo sean en estructura.

Dos enfoques principales:

1. Ensamblaje de fragmentos estructurales
   - Ejemplos: SWISS-MODEL, ROBETTA.
   - Se alinean secuencias y se copian fragmentos del esqueleto peptídico de estructuras conocidas.

2. Modelado por satisfacción de restricciones
   - Ejemplo: MODELLER.
   - Usa distancias y ángulos extraídos de templates.
   - Genera varios modelos compatibles con esas restricciones.

Muy útil para estudiar el efecto de mutaciones puntuales.

# Predicción de Contactos

En un alineamiento múltiple, si dos posiciones mutan de manera correlacionada, es probable que estén en contacto en la estructura 3D.

Se estudia:
- Información mutua.
- Información directa (DCA).

A partir de eso se construyen matrices de contacto que ayudan en el modelado estructural.

# Mutaciones Puntuales

El efecto de una mutación depende mucho del contexto estructural.

No es lo mismo cambiar un aminoácido:
- En el núcleo de una hélice.
- En la superficie.
- En un sitio de interacción proteína-proteína.

La estructura determina el impacto funcional de la mutación.

# AlphaFold

Surge gracias a:
- Gran cantidad de secuencias disponibles.
- Muchas estructuras experimentales.
- Alta capacidad de cómputo.
- Uso de redes neuronales profundas.

# CASP

Experimento bianual donde:
- Se publican secuencias sin estructura conocida.
- Diferentes grupos intentan predecirlas.
- Se comparan las predicciones con la estructura experimental.

Con AlphaFold hubo una mejora muy grande en la métrica GDT_TS.

# AlphaFold 2

Entrada:
- Secuencia problema.
- Alineamiento múltiple (MSA).

Pasos principales:

1. Extrae correlaciones evolutivas del MSA.
2. Predice distancias reales entre residuos (no solo contactos).
3. Predice ángulos diedros phi y psi.
4. Optimiza la estructura completa por minimización de gradientes.
5. Relaja el modelo con el campo de fuerzas AMBER.
6. Modela cadenas laterales completas.

Importante: predice distribuciones de distancias, no solo si dos residuos están en contacto o no.

# AlphaFold 3

- Menor dependencia del alineamiento múltiple.
- Usa modelos de difusión (similares a los usados en generación de imágenes).
- Permite modelar complejos proteína-proteína, proteína-ADN y proteína-ligando.

# Métricas de AlphaFold

## pLDDT

- Confianza por residuo.
- Toma valores de 0 a 100.
- Se guarda en el campo B-factor del archivo PDB.
- Valores mayores a 90 indican alta confianza.

Está relacionado con la métrica experimental lDDT.

## PAE (Predicted Aligned Error)

- Mide el error esperado entre residuos si se superpone el modelo con la estructura real.
- Se mide en angstroms.
- Es especialmente útil para evaluar la orientación relativa entre dominios.

Si el PAE entre dominios es alto, no se debe confiar en su orientación relativa.

# Otros Algoritmos

- RosettaFold.
- RFdiffusion (muy usado en diseño de proteínas).
- ESMFold (basado en modelos de lenguaje).