# Seminario de Algoritmos de Optimización (03MIAR)

Trabajo práctico de la asignatura. Problema elegido: **3. Combinar cifras y operaciones**.

Se trata de combinar las nueve cifras del 1 al 9 y los cuatro operadores básicos (`+`, `-`, `*`, `/`),
de forma alternada y sin repetir ninguno, para obtener una cantidad dada. Toda expresión válida tiene
la forma `c1 op1 c2 op2 c3 op3 c4 op4 c5`, con cinco cifras distintas y los cuatro operadores usados
una vez cada uno. El ejemplo del enunciado, para obtener el 4, es `4+2-6/3*1`.

## Por qué este problema

De los tres propuestos es el que permite una entrega más completa:

- El espacio de soluciones tiene 362.880 expresiones, así que la fuerza bruta **cabe entera** en unos
  segundos. Eso da una referencia exacta contra la que verificar el algoritmo mejorado, cosa que en
  los problemas 1 y 2 no es posible.
- Las dos preguntas de análisis del enunciado (valor máximo y mínimo, y si se alcanzan todos los
  enteros intermedios) tienen respuesta exacta y demostrable, no aproximada.
- Los datos están en el propio enunciado. El problema 1 depende de un fichero externo alojado en un
  acortador de enlaces, y en el problema 2 las tablas de audiencia y de coincidencias vienen como
  imágenes incompletas en el PDF.

## Reparto del trabajo

El notebook `Seminario_Algoritmos.ipynb` está dividido en dos mitades. Cada apartado marcado con
`(*)` es de respuesta obligatoria según el enunciado, y hay tres en cada mitad.

| Apartado | Responsable |
| --- | --- |
| Utilidades comunes: representación y evaluador de expresiones | Carlos |
| (\*) Número de posibilidades sin y con restricciones | Carlos |
| (\*) Estructura de datos y justificación | Carlos |
| Algoritmo por fuerza bruta | Carlos |
| Complejidad de la fuerza bruta | Carlos |
| (\*) Algoritmo mejorado (vuelta atrás con poda) | Carlos |
| (\*) Complejidad del algoritmo mejorado | Carlos |
| (\*) Función objetivo | Irune |
| (\*) Maximización o minimización | Irune |
| Análisis: valor máximo, mínimo y enteros alcanzables | Irune |
| Juego de datos de entrada aleatorio | Irune |
| Aplicación del algoritmo al juego de datos | Irune |
| Referencias | Irune |
| Líneas de avance y variaciones del problema | Irune |

El criterio del reparto ha sido equilibrar carga, no número de apartados. La mitad de Carlos son dos
bloques de código densos (la enumeración exhaustiva y el algoritmo con poda, que es la parte más
larga del trabajo). La mitad de Irune tiene más apartados pero varios se responden en un párrafo, y
los tres que llevan código (análisis de valores, generador de datos y comparativa) se apoyan en las
funciones que ya deja preparadas la otra mitad: `evaluar`, `texto`, `formatea`, `fuerza_bruta`,
`resolver` y el diccionario `TODAS` con todos los valores alcanzables.

## Cómo trabajamos

`main` contiene el esqueleto: cabecera, enunciado, hipótesis de modelado y los títulos de todos los
apartados, con un marcador donde va cada respuesta pendiente. Nadie escribe directamente en `main`.

1. Sal de `main` con una rama propia: `git checkout -b tu-nombre/lo-que-haces`
2. Rellena solo los apartados de tu mitad, dejando intactos los marcadores de la otra.
3. Abre una pull request contra `main` para que la otra persona la revise antes de fusionar.

Las salidas de las celdas se suben al repositorio a propósito: la entrega exige mostrar el resultado
de ejecución, y así la revisión de cada pull request se puede hacer sobre los resultados reales sin
tener que ejecutar nada.

Antes de fusionar la segunda mitad hay que ejecutar el notebook entero de arriba abajo (en Colab,
`Entorno de ejecución > Ejecutar todo`) para que la numeración de las celdas quede correlativa y las
mediciones de tiempo salgan todas de la misma máquina.

## Ejecución

El notebook solo usa la biblioteca estándar de Python y `matplotlib`, así que funciona en Colab sin
instalar nada. En local:

```bash
pip install notebook matplotlib
jupyter notebook Seminario_Algoritmos.ipynb
```

Tarda alrededor de un minuto en ejecutarse entero. La mayor parte se va en las pasadas de fuerza
bruta, que son intencionadamente lentas porque sirven de término de comparación.

## Entrega

- `Seminario_Algoritmos.ipynb` con las salidas de ejecución visibles.
- El mismo notebook exportado a HTML o PDF.
- En las observaciones del aula virtual, el enlace a este repositorio.
