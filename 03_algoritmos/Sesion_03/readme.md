# Análisis de Algoritmos y Estructuras para Datos Masivos 2020
### 3. Búsqueda 
#### Profesor: Eric S. Tellez <eric.tellez@infotec.mx>
***
Autor: Edgar Rios Linares  
<erlinares@gmail.com>  
Fecha: 25-Sep-2020  
Versión: 1
***

### Actividad

Dado un corpus de 50,000 tweets públicos y reales, de contenido político, [politicos.json](politicos.json), se genera un indice invertido con las 100 listas de posteo más pobladas, es decir, los términos (palabras) que aparecen en una mayor cantidad de documentos, considerando cada tweet como un documento.

Estas listas de posteo se guardan en un archivo de nombre [listas-posteo-100.json](listas-posteo-100.json)

El anterior proceso de generación del indice invertido está explicado y ejecutado en el notebook hecho en Julia [invertedindex.ipynb](invertedindex.ipynb)

 
1. Seleccionar 1000 identificadores de documentos al azar, entre $1$ y $n$, recuerde que $n=50,000$.
  - Acumular el tiempo de _buscar_ los 1000 identificadores en cada una de las listas (un solo número que represente las $100\times 1000$ búsquedas). Nota: lo que determinará al buscar es la _posición de inserción_ que se define como el lugar donde debería estar el identificador si se encontrara en la lista.
  - Los algoritmos que se caracterizarán son los siguientes (nombres con referencia a [@Bentley76]):
      - Búsqueda secuencial $B_0$
      - Búsqueda binaria $B_1$
      - Búsqueda doblada $B_2$
      - Búsqueda casí optima $B_k$

  - ¿Cómo podría encontrar aquellos documentos que contengan lo siguientes?
    - Un termino dado, e.g., `mexico`
    - Que contengan dos términos, e.g., `mexico` y `empresarios`
    - Bozqueje un algoritmo que realice la operación anterior y bozqueje el costo en comparaciones con respecto a los tamaños de las dos listas de posteo, $m$ y $n$.
