## Algoritmos de predicción
*Dulce Alejandra Carrillo Carlos* 

### Optimización de cadenas laterales

Cuando la identidad de secuencia entre dos proteínas es alta, puede asumirse que el esqueleto peptídico permanece aproximadamente constante. Bajo esta premisa, se optimizan las cadenas laterales para:

- Mejorar estabilidad
- Ajustar especificidad
- Modificar actividad catalítica

Este enfoque supone que la geometría global de la interfaz no cambia significativamente.

### Interacciones no covalentes en interfaces

Las interfaces biomoleculares están estabilizadas principalmente por interacciones no covalentes, en especial:

- Puentes de hidrógeno
- Interacciones electrostáticas
- Contactos hidrofóbicos

La formación de puentes de hidrógeno depende de la naturaleza química de los residuos involucrados. Por ello, el análisis de interfaces modeladas requiere evaluar no solo complementariedad geométrica, sino también especificidad química.

### Interfaces proteína-DNA-RNA: sistemas CRISPR-Cas

Las endonucleasas CRISPR-Cas guiadas por RNA son un ejemplo de complejos proteína-ácido nucleico altamente específicos.

Para su funcionamiento:

- Se requiere una secuencia diana complementaria al RNA guía (sgRNA).
- Debe existir un motivo adyacente denominado PAM (protospacer adjacent motif).
- La arquitectura tridimensional del complejo condiciona la especificidad de corte.

Además del diseño in silico, es necesario evaluar experimentalmente posibles cortes fuera de objetivo y regiones sensibles del RNA guía. También se han empleado simulaciones de dinámica molecular para estudiar la estabilidad y mecánica de estos complejos.

### Docking

Cuando no se dispone de una estructura experimental del complejo, se recurre a métodos de docking.

Características principales:

- Exploran múltiples orientaciones relativas entre macromoléculas.
- Reducen el coste computacional usando aproximaciones matemáticas (por ejemplo, transformadas de Fourier).
- Generan múltiples modelos candidatos que deben evaluarse posteriormente.

El análisis de resultados requiere criterios estructurales y conocimiento biológico para identificar interacciones plausibles.
