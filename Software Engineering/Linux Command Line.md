### Conceptos Básicos

*GUI:* Graphical User Interface - Interfaz grafica

*CLI:*  Command Line Interface - Terminal
<br>
### Comandos

*pwd:*  Print Working Directory - Muestra el directorio actual -> `pwd`

*exit:*  Salir de comandos, terminal o interfaces -> `exit`

*whoami:*  Muestra el usuario del sistema -> `whoami`

*hostname:*  Muestra el nombre del host del sistema -> `hostname`

*man:*  Muestra un manual de un comando enviado como parámetro -> `man <command>`

*ls:*  Lista todos los archivos del directorio -> `ls`

*ls -l:*  Lista de forma mas ordenada y detallada -> `ls -l`

*clear:*  Limpia toda la pantalla de la terminal -> `clear`

*cd:*  Cambia a un directorio indicado -> `cd <path/.../>`

*cd .. :*  Retorna al directorio anterior -> `cd ..`

*mkdir:*  Crea un nuevo directorio -> `mkdir <directory name>`

*touch:*  Crea un archivo vacío -> `touch <filename>`

*echo:*  Muestra strings en la terminal enviados como parámetro -> `echo <"string">`

*rm:*  Elimina un archivo -> `rm <filename>`

*rm -r:*  Elimina un directorio mediante recursión -> `rm -r <directory name>`

*rmdir:*  Elimina un directorio vacio -> `rmdir <directory name>`

*mv:*  Mueve un archivo a un path indicado -> `mv <file> <path/.../>`

*mv (renombrar):*  Renombrar un archivo -> `mv <file> <new file name>`

*cp:*  Crea una copia del archivo -> `cp <file> <copy file name>`

*head:*  Muestra el inicio de un archivo -> `head <filename>`

*tail:*  Muestra el final de un archivo -> `tail <filename>`

*cat:*  Muestra el contenido completo de un archivo -> `cat <file>`

*wget:*  Obtiene informacion de internet en un archivo -> `wget <link/.../filename>`

*curl:*  Parecido a wget, pero se le pasa a un archivo -> `curl <link> > <filename>`

*zip:*  Comprime un archivo -> `zip <file.zip> <file>`

*unzip:*  Descomprime un archivo -> `unzip <file.zip>`
<br>
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

*Tmux:*  Permite tener múltiples sesiones de shell a la vez -> `tmux`

*gnome-pomodoro:*  Permite el uso de Pomodoro -> `sudo apt-get install gnome-pomodoro`
<br>
### TMUX Hotkeys
#### Sesiones

*Version:*  Muestra la versión actual de Tmux -> `tmux -V`

*Sesiones Activas:*  Muestra las sesiones activas en el sistema -> `tmux ls`

*Crear Nueva Sesión:*  Crea una nueva sesión con un nombre ingresado por el usuario en la terminal -> `tmux new -s <session name>`

*Ejecutar tmux.conf:*  Activa plugins -> `tmux source ~/.config/tmux/tmux.conf`

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

*Minimizar o Maximizar Panel (Horizontal):*  Ctrl + B + LeftKey / RightKey

*Minimizar o Maximizar Panel (Vertical):*  Ctrl + B + DownKey / UpKey 

*Cerrar Panel:* Eliminar un panel de la ventana -> `exit` ó `tmux kill-pane`

*Crear una Ventana:*  Ctrl + B C

*Moverse a otra Ventana:*  Ctrl + B < Numero de Ventana >

*Renombrar una Ventana:*  Ctrl + B ,
 
*Hacer zoom a una ventana en especifico:*  Ctrl + B Z

*Eliminar una Ventana:*  Eliminar ventana -> `tmux kill-window -t <window name>`
<br>
### TMUX Plugins y Configuración
#### Instalar TPM (Tmux Plugin Manager)
1. Clonar el repositorio mediante el siguiente comando -> `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
2. Crear el directorio **tmux** en **$HOME**
3. Crear el archivo **tmux.conf** -> `touch ~/.config/tmux/tmux.conf`
4. Abrir **tmux.conf** con cualquier edito de texto.
5. Copiar:
~~~bash
set -g @plugin 'tmux-plugins/tpm'
set -g @plugin 'tmux-plugins/tmux-sensible'

# Esto siempre debe ir al final de tmux.conf
run '~/.tmux/plugins/tpm/tpm'
~~~
6. Abrir una sesión de tmux y usar el comando -> `tmux source ~/.config/tmux/tmux.conf`
7. Agregar el **tmux.conf** a **.bashrc** para que se guarde en sesiones globales (siempre se ejecutara) -> `echo "tmux source ~/.config/tmux/tmux.conf"`
<br>
#### Instalar Plugins

1. Colocar en **tmux.conf** -> `set -g @plugin "plugin-data"`
2. En tmux usar **Ctrl +B I**
<br>
### Instalar Temas, Fuentes e Iconos
#### Temas
1. Descargar el tema en internet.
2. Mover el tema descargado a `/ usr/share/themes`
3. Extraer el tema en dicho directorio (usar **sudo**)
4. En **Tweaks,** cambiar el tema del equipo con el descargado.

#### Fuentes
1. Descargar la fuente en internet.
2. Mover la fuente descargada a `/ usr/local/share/fonts`
3. Extraer la fuente en dicho directorio (usar **sudo**)
4. En **Tweaks,** cambiar la fuente del equipo y asignar su tamaño.
5. Para la terminal, ir a **Preferencias** y seleccionar la fuente deseada.

#### Iconos
1. Descargar el paquete de iconos en internet.
2. Mover los iconos a `/ usr/share/icons`
3. Extraer el paquete de iconos en dicho directorio (usar **sudo**)
4. En **Tweaks,** cambiar los iconos del equipo con el paquete descargado.
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