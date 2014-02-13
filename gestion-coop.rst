Gestión Cooperativa
===================

El Módulo copperative_ar contiene una serie de módulos para llevar adelante la gestión de una Cooperativa de Trabajo:

 * Socios
 * Reuniones
 * Sanciones
 * Vacaciones / licencias
 * Recibos

Socios
------

Este módulo permite la carga de datos útiles del socio. Primero que nada el socio debe ser creado como Entidad, dado que ahi se cargarán los datos contables necesarios para que se opere en el sistema. 
Desde el módulo Socio se selecciona al Socio (ya cargado como Entidad) y se cargan los datos complementarios de utilidad legal (legajo, estado, fecha de ingreso, etc.).

.. image:: img/socio.png
   :width: 750 px

Este módulo permitirá entonces tener el legaajo del socio dentro del sistema. Este módulo está relacionado con el resto en tanto pueden visualizarse: las reuniones en las que el socio participó, sus recibos de Adelanto de Excedentes, las Sanciones y las vacaciones del mismo.

Vacaciones
----------

El módulo puede utilizarsecreando nuevos registros desde el módulo o desde la pestaña de "vacaciones y licencias" que se visualiza en la edición de cada Socio.   

.. image:: img/vacaciones.png
   :width: 750 px
   
Permite cargar los días que tiene asignados ese socio (Días de vacaciones) y luego permite cargar un registro por cada licencia o vacación que el socio se tome. 

.. image:: img/cargavacacion.png
   :width: 750 px

Sanciones
---------

Este módulo permite cargar sanciones a un socio con los Tipos que figuran en el Estatuto base de una Cooperativa de Trabajo: Llamado de Atención, Apercibimiento y Exclusión con el causante yel descargo presentado por el socio.
  
.. image:: img/sancion.png
   :width: 750 px

Reuniones
---------

Aqui se podrán cargar las Reuniones de Consejo y Asambleas que realiza la cooperativa, señalando los socios presentes y los temas tratados como área de texto o archivo adjunto (Tipos de Reunión: reunión de consejo, Asamblea 
Ordinaria o Extraordinaria).

.. image:: img/reuniones.png
   :width: 750 px

Desde el socio se puede buscar una REunión para señalar que el socio participó en la misma.

Recibos
-------

Permite crear el "Recibo de Anticipo de Retornos a Cuenta de Excedentes" que los socios de las cooperativas de trabajo reciben como prestación del trabajo que realizan.
Este módulo permite cargar el importe y la fecha del retiro y genera un Recibo con validez que pasa a estar inmutado una vez que está confirmado (tiene una secuencia propia de Recibos). El sistema toma los datos de al Cooperativa y del 
socio de forma automática para generar la impresión del recibo de forma correcta.
Al momento de confirmarse el Recibo, el mismo se inmuta y se generan los asientos contables necesarios. El recibo queda pendiente de pago (similar al workflow de factura). Una vez que el mismo se paga queda terminado el proceso y se realiza el Asiento correspondiente. 
