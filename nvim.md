# NeoVim

## Desarrollo

El entorno de ejecución de nvim busca ciertas carpetas relevantes, una de esos
tipos de carpetas es `lua/` o `plugin/`. En nuestr plugin necesitamos tener los
archivos lua en una carptea que nvim pueda identificar.
- Todo lo que se encuentra en la carpeta `plugin/` se carga antes de llegar a la
pantalla de inicio de nvim. antes de llegar a la pantalla de inicio de nvim.
Perfecto para lanzar comandos o crear atajos de teclado.
- Por otro lado el código dentro de la carpte `lua/` no se ejecuta
automáticamente pero está disponible para el programa.


