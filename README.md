# Seminario de Algoritmos de Optimización (03MIAR)

Trabajo práctico de la asignatura. Problema elegido: 3, combinar cifras y operaciones.

Hay que combinar las nueve cifras del 1 al 9 con los cuatro operadores básicos (`+`, `-`, `*`, `/`),
alternando cifra y operador y sin repetir ninguno, para obtener una cantidad dada. Todas las
expresiones tienen la forma `c1 op1 c2 op2 c3 op3 c4 op4 c5`, con cinco cifras distintas y los
cuatro operadores usados una vez cada uno. El ejemplo del enunciado, para obtener el 4, es
`4+2-6/3*1`.

Aparte de resolver el problema, el notebook responde a las dos preguntas que plantea el enunciado:
qué valor máximo y mínimo se pueden obtener, y si se alcanzan todos los enteros que hay entre ambos.

## Contenido

`Seminario_Algoritmos.ipynb`, con los apartados del guion y las salidas de ejecución ya guardadas,
para poder leerlo sin tener que ejecutar nada.

## Ejecución

Solo usa la biblioteca estándar de Python, así que en Colab funciona sin instalar nada. En local:

```bash
pip install notebook
jupyter notebook Seminario_Algoritmos.ipynb
```

Ejecutarlo entero tarda unos 30 segundos. Casi todo el tiempo se va en la fuerza bruta y en la celda
que mide cómo crece el coste, que son lentas a propósito porque sirven de comparación.

## Autores

Carlos Jurado Zalaya e Irune Urrutia.
