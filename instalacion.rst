Documentación Instalación del Proyecto.
=======================================
Para la instalación de Tryton verificar la documentación oficial en:
http://doc.tryton.org/3.0/tryton/doc/installation.html

Para la instalación del módulo account_invoice_ar, leer INSTALL del módulo 
(https://github.com/tryton-ar/account_invoice_ar/blob/master/INSTALL) 

Documentación Funcional.
========================

Existe un [repositorio](https://github.com/tryton-ar/documentacion-tryton-ar) 
para documentación funcional y un sitio donde la misma puede 
consultarse en linea: [documentación funcional](http://tryton-ar.readthedocs.org/es/latest/).

Instalación.
============

Una cosa que confunde mucho a los usuarios es la instalación, sobre
todo a quienes no están familiarizados con los diversos modos de
instalación que hay en Linux.

Básicamente, podríamos decir que hay 3 formas de instalar Tryton. A
continuación expondremos los pro y las contras de cada uno de ellos:

Paquete de distribución.
------------------------

Este modo es, quizás el más sencillo, consiste en instalar tryton a
partir de los repositorios oficiales de la distribución. Tiene como
ventaja la facilidad, ya que con solo un 'apt-get install
tryton-server' (por ej.) se instala tryton con todas sus dependencias
incluyendo PostgreSQL y queda integrado con la distribución, por lo
que se funciona como demonio de sistema y toma la configuración de
/etc.

Como desventaja tenemos que suele ser una versión desactualizada y
solo están los módulos oficiales. A su vez, queda todo instalado como
usuario root y hace que haya que usar root para agregar módulos. Por
último, no es práctico para desarrolladores ya que no se pueden
modificar módulos para aportar con la comunidad.

Instalación con Pip.
--------------------

[Pip](http://lcaballero.wordpress.com/2013/03/20/instalacion-de-paquetes-python-con-distribute-y-pip/)
es un gestor de paquetes para python, siendo que tryton está
desarrollado en python. Usando pip podemos instalar la última version
(o cualquiera) y todos los módulos oficiales. Como desventaja tenemos
que hay que instalar manualmente todas las dependencias de librerías
no escritas en python. En Debian y derivados es instalar unos cuantos
paquetes que terminan con '-dev'. Adicionalmente, tendremos que
ocuparnos de arrancar y parar el servidor, así como también de
establecer un archivo de configuración. Al igual que el método
anterior instala todo como root y no nos facilita las cosas para
desarrollar módulos.

Instalación con Pip+Virtualenv.
-------------------------------

Consiste en instalar tryton dentro de un
[virtualenv](http://rukbottoland.com/blog/tutorial-de-python-virtualenv/). Virtualenv
es una herramienta de python que permite crear ambientes de python
aislados, todos independientes y con sus propias librerías. Estos
entornos virtuales que genera pueden usarse sin problemas en cualquier
carpeta de usuario común. Esta forma tiene como ventaja que se puede
trabajar fácilmente modificando módulos (se puede hacer con un usuario
común). Para contribuir con algún módulo no se va a poder
directamente, pero no es díficil hacerlo. De nuevo tenemos que
levantar el servidor manualmente y gestionar la configuración.

Instalación del Desarrollador.
------------------------------

Consiste en instalar tryton _clonando_ los repositorios de código
fuente. Un repositorio de código es un lugar donde se almacena el
código fuente de un programa así como el historial de cambios. De esta
manera, utilizaremos un
[software de control de versiones](http://es.wikipedia.org/wiki/Control_de_versiones)
para descargar Tryton y todos sus módulos. Este proceso es largo y
tedioso pero se puede simplificar usando scripts o combinándolo con el
método anterior. Un ejemplo de scripts que automatizan mucho del
trabajo e incluyen todos los módulos de la localización Argentina se
puede encontrar
[Aquí](http://braincoop.devecoop.com/es/posts/guia-agil-para-instalacion-de-tryton-con-localizacion-argentina.html).

De nuevo, esta opción implica instalar muchas cosas manualmente y
resolver ciertos problemas. Pero con una buena instalación se puede
tener un sistema con todos los módulos y listo para enviar nuestros
aportes directamente al repositorio principal. Puede parecer dificil,
pero ya se irán mejorando los scripts para que todos podamos
contribuir con Tryton.


