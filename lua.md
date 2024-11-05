# Lua

## ¿Qué es Lua?

Lua es un lenguaje ligero de scriptado, dinamicamnte tipado e interpretado
mediante una representación intermedia en bytecode, combina una sintaxis
procedural simple con una descripción de datos muy expresiva. Lua está
implementado cómo una biblioteca de C, el interprete de lua usa esta para
brindar un soporte completo e independiente, así Lua puede funcionar embebido.

# Conceptos básicos.

## Módulos

Lua funciona requeriendo otros ficheros, característica propia de su naturaleza
procedural. Usando `require( path )` busca en el sistema un documento que encaje
con el fichero dado o una carpeta que tenga el mismo nombre y contenga un
archivo llamado `init.lua`. La función require comprende tambien el concepto de
ficheros anidados y permite mediante el operador `.` apuntar a ficheros o
directorios dentro del mismo "espacio de nombres". *Es importante señalar que
require unicamente carga un fichero una vez*, un fichero lua es muy precido
conceptualmente a una unica gran función, para acceder a la función una vez
cargada usamos el método `print( require( path ) )` para escribir el resultado.
**Es muy importante entender el detalle semantico de require: carga un ficehro
una vez y guarda su resultado, es una tabla, no ejecuta el fichero cada vez.**
Esta tabla puede accederse para borrar la clave específica para volver a
ejecutar el fichero y cambiar el valor. Esto hace que por ejemplo en nvim,
cuando dos paquetes usan un mismo tercer plugin, lo que comaprten es una unica
ejecución del fichero.

## Bucles

Para iterar sobre una tabla en Lua podemos usar un buble `for`. Para iterar
sonbre una tabla usamos `ipairs` o `pairs`, el primero itera unicamente sobre
claves numéricas garantizando el orden, el segundo itera sobre todas las claves
pero no garantiza el orden.

```lua
for key, value in pairs(maps) do
    print(key, value)
end
```

## Referencias

1. [Lua reference manual](https://www.lua.org/manual/5.4/)
1. [Neovim Lua Plugin From Scratch - TJ](https://www.youtube.com/watch?v=n4Lp4cV8YR0&t=886s)
