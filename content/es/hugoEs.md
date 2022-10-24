# Que es Hugo
Hugo es un moderno framework para creación de sitios web de propósito general. Se ubica en la categoría de los nuevos generadores de sitios estáticos, ​ basados en la arquitectura dinámica JAMstack y es escrito completamente en Go. Originalmente fue creado por Steve Francia en 2013.
# Instalacion
En este tutorial vamos a instalar Hugo 

Vamos a instalarlo en su version extended, que incluye su programa base y algunas funcionalidades extra que nos pueden venir bien
Instalación Hugo en Linux
Comprobar si tenemos instalado Snap

Para instalar Hugo en Linux vamos a utilizar el gestor de paquetes Snap. Por ello lo primero que vamos a hacer es comprobar si tenemos este gestor instalado, para ello utilizaremos el siguiente comando:

```snap version
```


Esto deberia respondernos con el siguiente mensaje:

```snap 2.55.3+22.04
snapd   2.55.3+22.04
series  16
ubuntu  22.04
kernel  5.15.0-48-generic
``` 

En ese caso significará que tenemos snap instalado. Entonces podemos empezar con la instalación.
Instalar el paquete hugo-extended

Utilizando el gestor Snap vamos a instalar el paquete hugo-extended.
```
snap install hugo --channel=extended
```
Instalación Hugo en Windows

Tendremos que acceder a la pagina de Hugo y iremos a descargas.

Una vez aquí descargaremos la ultima versión que tenga un nombre del formato hugo_extended_x.x.x_windows-amd64.zip donde x.x.x corresponderá a la versión.

Este zip contendrá el CMS, pero la instalación tendremos que realizarla manualmente.

Extraeremos el zip y para mayor facilidad moveremos el archivo Hugo.exe resultante a la ruta C:\Hugo\bin la cual crearemos.

Una vez lo tengamos, en el buscador de Windows, accederemos a Editar las variables de entorno del sistema buscando esto en el.

Se nos abrirá una ventana llamada Propiedades del sistema y en esta volveremos a pulsar en Variables de entorno.

En la lista que nos mostrará buscaremos la variable PATH, y al final de esta añadiremos ‘;C:\Hugo\bin’.

Con esto reiniciando el sistema tendremos hugo instalado y accesible en nuestro sistema.
Instalación Hugo en MacOS

Si no lo tenemos ya instalado, instalaremos el gestor de paquetes brew con el siguiente comando

```ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
Una vez instalado, usaremos este comando para instalar Hugo.
``` brew install hugo
```
Creación del sitio con Hugo
Creando el sitio

Siguiendo el tutorial anterior ya deberíamos tener instalado Hugo en nuestro sistema.

Ahora para crear un sitio con el CMS utilizaremos los comando:

# AVISO ESTOS COMANDOS DEBEN REALIZARSE DESDE NUESTRO USUARIO HABITUAL, NUNCA DESDE SUDO

```hugo new site nombredelsitio
cd nombredelsitio
```
Nuestro sitio ya esta creado, pero de momento no es funcional. Para que este pueda funcionar primero deberemos encontrar un tema que usar.
Instalando un tema en el sitio

Como ejemplo voy a usar el tema PaperMod, pero hay muchos por internet que podemos usar. Para instalar el tema lo que haremos en este caso (cada tema puede tener su propio método de instalación, pero la mayoría son de esta manera)

```echo "theme = 'hugo-PaperMod'" >> config.toml
cd themes
#Clonamos o descargamos en esta carpeta el tema que nos guste.
git clone https://github.com/adityatelange/hugo-PaperMod
# Entramos en la carpeta de nuestro tema
cd hugo-PaperMod
# Borramos de este tema la carpeta .git para que no nos cause problemas
#a la hora de subir nuestra pagina
rm -rf .git
```
 

Con esto ya tendremos el tema instalado y podremos arrancar nuestro sitio usando

```hugo-server
```
Después de arrancarlo el comando nos devolverá una URL en la cual podremos ver nuestro sitio mientras este servidor este encendido.
Creación de artículos en Hugo

Para crear artículos en Hugo deberemos dirigirnos a la carpeta content, y dentro en la carpeta post podremos empezar a escribir estos en formato MarkDown o MD para abreviar.

Mientras nosotros escribimos este se ira añadiendo al sitio y sera visible en nuestro servidor local.
a continuacion dejo un enlace de un video para entender mejor como es la instalacion
{{<youtube tPP-P289BbY>}}