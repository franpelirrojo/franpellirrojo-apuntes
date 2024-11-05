# Linux

### apt
El comando `apt` es una herramienta de gestión de paquetes fácil de usar para
distribuciones de Linux basadas en Debian, como Ubuntu. Simplifica tareas
comunes como instalar, eliminar y actualizar software, gestionar dependencias y
actualizar el sistema. Aquí tienes un resumen de sus características
principales:

1. Gestión de Paquetes
- **Instalación**: `sudo apt install nombre_paquete` – Instala nuevos paquetes
de software.
- **Eliminación**: `sudo apt remove nombre_paquete` – Elimina paquetes
instalados.
- **Actualización**: `sudo apt upgrade` – Actualiza todos los paquetes
instalados a las versiones más recientes.
- **Actualización del Sistema**: `sudo apt update` – Refresca el índice de
paquetes con las actualizaciones más recientes de los repositorios.
2. Comandos Adicionales
- **Buscar**: `apt search término_busqueda` – Encuentra paquetes mediante un
término de búsqueda.
- **Información**: `apt show nombre_paquete` – Muestra detalles del paquete.
3. Características Avanzadas
- Permite gestionar múltiples paquetes en un solo comando, resuelve dependencias
automáticamente, maneja archivos de configuración y guarda en caché los paquetes
descargados para una reinstalación más rápida.

apt vs. apt-get Aunque `apt-get` sigue siendo funcional, `apt` ofrece una
experiencia más intuitiva y simplificada, combinando funciones tanto de
`apt-get` como de `apt-cache`. Es la herramienta recomendada para la mayoría de
las tareas de gestión de paquetes en sistemas modernos basados en Debian.

### PS1
La parte izquierda del prompt del shell, conocida como la cadena de prompt o
`PS1`, muestra detalles sobre el usuario actual, el nombre del host y el
directorio de trabajo. En tu ejemplo:

- **Nombre de usuario**: `franpelirrojo`
- **Nombre del host**: `Thinkpad`
- **Directorio de trabajo**: `~/code/nvim-disc`

La variable `PS1` define este prompt en Bash y, por lo general, incluye:

- Nombre de usuario
- Nombre del host
- Directorio actual
- Indicador de privilegio (`$` para usuarios normales, `#` para root)

Para ver tu configuración actual de `PS1`, ejecuta:

```bash
echo $PS1
```

Puedes personalizarla modificando la variable `PS1` en `~/.bashrc`. Para un
prompt como el tuyo, usa:

```bash
PS1='\u@\h:\w\$ '
```

Donde:
- \u = nombre de usuario
- \h = nombre del host
- \w = directorio de trabajo
- $ = privilegio de usuario
