# Bioinformática estructural (Martes 17 de febrero)
*Dulce Alejandra Carrillo Carlos* 

## Enlaces peptídicos y geometría

El enlace peptídico es un enlace covalente entre el grupo carboxilo de un aminoácido y el grupo amino del siguiente. Tiene carácter parcial de doble enlace, lo que le da:
- Rigidez
- Cierta restricción en la rotación

Esto limita los grados de libertad conformacionales de la cadena polipeptídica. La rotación queda principalmente restringida a los ángulos φ (phi) y ψ (psi).

En ácidos nucleicos, el enlace equivalente que une nucleótidos es el fosfodiéster.

## Niveles estructurales

### 1. Estructura primaria

Corresponde a la secuencia lineal de aminoácidos (o nucleótidos en ácidos nucleicos).

- Representación frecuente en código de una letra
- Determina el potencial de plegamiento

### 2. Estructura secundaria

Surge para maximizar la formación de puentes de hidrógeno entre los grupos del esqueleto peptídico.

Elementos:

- α-hélices (generalmente dextrógiras)
- Láminas β (paralelas o antiparalelas)
- Giros y loops

Los residuos adoptan conformaciones características descritas por los ángulos φ y ψ, estos se pueden ver en Ramachandran plots.

### 3. Estructura terciaria

Organización tridimensional completa de una cadena polipeptídica.

- Formación de un glóbulo estable
- Interacción entre elementos secundarios
- Conexión mediante loops

### 4. Estructura cuaternaria

Asociación de múltiples cadenas polipeptídicas en un complejo funcional.

## Dominios y bases de datos

Un dominio es una unidad estructural y funcional relativamente independiente.

Características:

- Núcleo hidrofóbico
- Puede plegarse de manera autónoma
- Suele tener función específica
- Puede repetirse en distintas proteínas

Bases de datos: 

- CATH: clasificación jerárquica estructural.
- Pfam: familias basadas en alineamientos de secuencia.
- TED: integración de dominios experimentales y predichos.

## Conservación estructura-secuencia

- La estructura suele conservarse más que la secuencia.
- Pequeñas diferencias estructurales pueden surgir tras pérdida significativa de identidad de secuencia.
- La inferencia funcional suele basarse más en estructura que en secuencia aislada.

## Algoritmos de alineamiento estructural

### Métodos basados en representación simplificada

- Foldseek
- FoldMason

Convierten la información estructural en alfabetos discretos para acelerar comparaciones.

## MAMMOTH

Algoritmo heurístico en Fortran para comparación estructural.

- Devuelve un E-value similar al de BLAST.
- Supera limitaciones del RMSD.
- Permite evaluar similitud parcial entre regiones análogas.

El RMSD asigna el mismo peso a regiones conservadas y divergentes, lo que puede distorsionar comparaciones.

## Métricas de comparación estructural

### 1. RMSD

Desviación cuadrática media entre posiciones atómicas superpuestas.

Limitación: sensibilidad a regiones divergentes.

### 2. E-value

Valor esperado que estima la probabilidad de observar una similitud por azar.

### 3. TM-score

Normaliza por longitud de secuencia.

- Rango típico: 0–1
- >0.5 sugiere topología similar
- Menos sensible a diferencias locales que RMSD

### 4. lDDT / IDDT

Métrica independiente de superposición.

- Evalúa distancias locales entre átomos vecinos.
- Rango 0–1.
- Valores altos indican alta similitud local.

Puede calcularse considerando todos los átomos o solo el esqueleto peptídico.

## Protein Data Bank (PDB)

Base de datos de estructuras tridimensionales de macromoléculas.

Características del formato PDB:

- Coordenadas cartesianas atómicas
- Identificadores de 4 caracteres
- Representación estándar para proteínas y complejos biológicos