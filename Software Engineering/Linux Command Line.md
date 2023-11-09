### Comandos

*Cat:*  Muestra el contenido completo de un archivo -> `cat <file>`



### Paquetes y Utilidades

*Desinstalar paquete:*  Remover paquete -> `sudo apt remove <package>`

*Bat:*  Muestra el contenido completo de un archivo con resaltadores -> `batcat <file>`

*Tldr:*  Muestra una versión mejorada de la documentación o pagina de los diferentes comandos -> `tldr <comando>`

*Neofetch:*  Muestra información detallada de los componentes del computador y del sistema -> `neofetch`

*Cpufetch:*  Muestra información detallada del CPU del computador -> `cpufetch`

*Gdu:*  Muestra información detallado sobre el almacenamiento del disco -> `gdu`

*Gdu Help:*  Muestra documentación y detalles de gdu -> `gdu -h`

*Bpytop:*  Muestra información en tiempo real del consumo de recursos en los diferentes componentes del computador -> `bpytop`

*Speedtest:*  Realiza una prueba de velocidad del internet -> `speedtest`

*Speedtest Help:*  Muestra la documentación y detalles de speedtest -> `speedtest -h`

*Ranger:*  Gestor de archivos nativo en la terminal -> `ranger`

*Tmux:*  Permite tener multiples sesiones de shell a la vez -> `tmux`

### Tmux Hotkeys
#### Sesiones

*Version:*  Muestra la version actual de Tmux -> `tmux -V`

*Sesiones Activas:*  Muestra las sesiones activas en el sistema -> `tmux ls`

*Crear Nueva Sesión:*  Crea una nueva sesión con un nombre ingresado por el usuario en la terminal -> `tmux new -s <session name>`

*Renombrar una Sesión:*  Renombrar una sesión -> `tmux rename-session -t <old name> <new name>`

*Acceder a una Sesión:*  Accede a una determinada sesión -> `tmux a -t <session>`

*Salir de una Sesión:*  Ctrl + B D

*Cambiar a otra Sesión:*  Cambia a una sesión del server -> `tmux switch -t <session>`

*Eliminar una Sesión:*  Elimina una sesión del server -> `tmux kill-session -t <session name>`

*Eliminar el server:*  Elimina todo el servidor -> `tmux kill-server`
<br>
#### Ventanas y Paneles

*Abrir Panel Vertical:*  Ctrl + B %

*Abrir Panel Horizontal:*  Ctrl + B "

*Ir a Panel*  Ctrl + B LeftKey / RightKey / UpKey / DownKey

*Cerrar Panel:* Eliminar un panel de la ventana -> `exit` ó `tmux kill-pane`

*Crear una Ventana:*  Ctrl + B C

*Moverse a otra Ventana:*  Ctrl + B < Numero de Ventana >

*Renombrar una Ventana:*  Ctrl + B ,

*Eliminar una Ventana:*  Eliminar ventana -> `tmux kill-window -t <window name>`
<br>
### Instalar aplicaciones mediante .deb packages (64 bits)
#### Instalación Manual
1. Descargar el paquete .deb (64 bits)
2. Clickear el archivo e instalar con Software Installer.
3. Seguir los pasos de instalación.

#### Instalación mediante Terminal

Utilizar el comando `sudo apt install ./<file>.deb`
<br>
### Eliminar Aplicaciones del Sistema

1. Visualizar las aplicaciones o paquetes instalados:
	- **dpkg:**  Usar el comando `dpkg --list`
	- **snap:** Usar el comando `snap list`
	- **apt:** Usar el comando `sudo apt --installed list`
	- **flatpak:** Usar el comando `sudo flatpak uninstall <name>`
1. Utilizar el comando dependiendo del gestor de paquetes:
	- **snap:**  Usar el comando `sudo snap remove <name>`
	- **dpkg y apt:** Usar el comando `sudo apt-get --purge remove <name>`

##### Tags

#courses