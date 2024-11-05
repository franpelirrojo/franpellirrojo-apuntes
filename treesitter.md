# Tree-sitter

### ¿Cómo funciona y por qué es tan bueno en lo suyo?
Tree-sitter es una herramienta para construir parsers. Esta librería permite
construir arboles sintacticos de un codigo fuente y actualizar el arbol mientras
que se edita el código fuente.

Contra la creencia general, por su suso habitual por editores de código, no
tiene nada que ver con un LSP. Un LSP trata de comprender el código en un
ventana general de todo el proyecto a un nivel semantico, mientras que
tree-sitter atiende únicamante a un documento y se centra en dar información
incremental de ese docuemento, de ese texto. 

Tree-sitter no es un compilador, no conce absolutamente nada sobre tipos,
variables o funciones, unicamente atiende al texto. Con esta librería puedes
escribir una gramática y generar un parser, que luego puede ser usado por una
aplicación que embeba tree-sitter. Las dos características más importantes de
esta libreria son: la capacidad incremental de no reconstruir el arbol
continuamente, la capacidad de tener un control de errores controlado que no
rompe todo el arbol y la capacidad para realizar consultas al arbol sintáctico.

### ¿Cómo funciona?
1. Se escribe la gramática del lenguaje, Java por ejemplo
    - Se escribe en ese lenguaje (Java).
    - `Java.java`
2. Tree-sitter entonces genera un `parser.c`
    - *La unicadependencia que existe es un compilador de C.*
3. Una vez compilado este `parser.c` puede cargarse dentro de una programa que
   use Tree-sitter.
4. Podemos parsear cualquier documento java y obtener información compleja sobre
   su estructura. Preguntar a un arbol es más facil que hacer mágia con regex.

## References
1. [tree-sitter explained](https://www.youtube.com/watch?v=09-9LltqWLY) 
