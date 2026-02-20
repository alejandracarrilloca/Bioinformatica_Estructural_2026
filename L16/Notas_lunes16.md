# Fundamentos estructurales de proteínas 
** Dulce Alejandra Carrillo Carlos **

## 1. Estructuras de proteínas

- El ADN guarda la información.
- Las proteínas ejecutan esa información.
- Lo importante no es solo la secuencia, sino la **forma tridimensional**.

Idea central:
> La función biológica depende directamente de la conformación 3D.

Si la proteína pierde su estructura (desnaturalización), pierde su función.

Excepción importante:

- **Proteínas intrínsecamente desordenadas (IDPs)**: no tienen estructura fija, pueden plegarse al unirse a un ligando o funcionar gracias a su flexibilidad.

## 2. Cómo se construyen las proteínas

### Componentes básicos

Las proteínas están hechas de 20 aminoácidos estándar.
Cada uno tiene:

- Grupo amino
- Grupo carboxilo
- Carbono alfa (Cα)
- Cadena lateral R (define propiedades)

### Cómo se conectan

Se unen mediante **enlaces peptídicos**:

- Reacción de condensación (libera agua)
- El enlace tiene carácter parcial de doble enlace
- Es rígido y plano
- Generalmente en configuración trans (prolina puede ser cis)

## 3. Qué fuerzas estabilizan la estructura

El plegamiento no depende de enlaces fuertes nuevos, sino de interacciones débiles acumulativas:

- Hidrofóbicas → principal motor (formación de núcleo interno)
- Van der Waals → empaquetamiento fino
- Electroestáticas → cargas opuestas (dependen de pH)
- Puentes de hidrógeno → estabilizan estructura secundaria

Son débiles individualmente, pero cooperativas en conjunto.

## 4. Organización estructural

### Estructura primaria

- Cadena lineal N → C
- La secuencia contiene la información para plegarse

### Estructura secundaria

Se estabiliza por puentes de hidrógeno del backbone:

- α-hélice → patrón i a i+4
- β plegada → paralela o antiparalela
- Loops y giros → conectan elementos

### Estructura terciaria

- Estructura tridimensional completa
- Núcleo hidrofóbico interno
- Regiones polares externas
- Combinación específica de hélices y láminas

- Dominios → unidades estructurales que pueden plegarse de manera independiente
- Matrices de contacto → muestran qué residuos están cerca en el espacio

### Estructura cuaternaria

- Varias cadenas polipeptídicas
- Forman un complejo funcional

## 5. Relación entre secuencia y estructura
- Mayor identidad de secuencia → menor divergencia estructural
- La estructura suele conservarse más que la secuencia

### RMSD

- Mide desviación promedio entre átomos equivalentes (Cα)
- RMSD bajo → estructuras similares
- RMSD alto → mayor diferencia

Comparaciones posibles:
- Alineamiento de secuencia → compara primaria
- Superposición estructural → compara coordenadas 3D

## 6. Cómo se determinan las estructuras

- Cristalografía de rayos X → alta resolución, estructura estática
- Crio-EM → útil en complejos grandes
- NMR → dinámica en solución
- SAXS → forma global
- Dicroísmo circular → contenido secundario
- Entrecruzamiento + MS → restricciones espaciales

## 7. Repositorio estructural

El **Protein Data Bank (PDB)** almacena estructuras 3D.

Esta base de datos contiene:
- Coordenadas atómicas
- Método experimental
- Indicadores de calidad

Formato actual:
- mmCIF (más completo que el antiguo formato PDB)

Visualización:

- PyMOL
- Chimera
- Jmol