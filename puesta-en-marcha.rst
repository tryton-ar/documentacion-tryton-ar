Puesta en marcha
================

Para poder completar estas operaciones el sistema requiere la configuración de diversas cuentas de imputación de los movimientos que genera el sistema, como se detalla a continuación. 
Se realizó un video tutorial donde pueden seguirse los pasos básicos de configuración del sistema para su uso: 
http://www.youtube.com/watch?v=nnJIJFD7lrc

Alta Período Fiscal
-------------------

Crear Período Fiscal: Contabilidad → Ejercicios Fiscales.
Permite crear el anual, las secuencias y hacer meses o trimestres, de forma 
manual o con wizard.
Es necesario porque toda imputación se realiza a un período fiscal. Es necesario cargar todas las secuencias aunque luego se configuren secuencias para cada tipo de factura en los puntos de venta.

.. image:: img/periodofiscal.png
   :width: 750 px

Plan de Cuentas
---------------

El plan de cuentas se selecciona con el Asistente de Configuración que se corre la primera vez que se ingresa al sistema. 
Es por eso que es importante tener  el módulo account_ar o account_coop_ar en la instalación para poder seleccionarlo. De todas formas desde Contabilidad → Configuración → Planes Contables se puede cargar un plan contable desde plantilla o agregar - modificar las cuentas que se desee. 

.. image:: img/plandecuenta.png
   :width: 750 px

Alta de Empresa
---------------

El alta de empresa se realiza desde el Asistente que corré la primera vez que se confiugura el sistema y puede agregarse y modificarse información desde Entidades -> Configuración -> Empresas.

Con el módulo account_invoice_ar se podrá observar una pestaña dentro de Empresa que permite la carga de los certificados para interactuar con los Webservcices de la AFIP.

.. image:: img/empresa.png
   :width: 750 px

Por otro lado es imporatnte notar que una empresa es una entidad, por lo que se podrán cargar datos de la entidad necesarios para el armado de las facturas y otros usos dentro del sistema. En la entidad se puede visualizar una pestaña Empresa que permite cargar información fiscal e impositiva. 
Además en la pestaña Contabilidad será necesario cargar la condición frente al IVA. Tryton ya trae por default la validación del CUIT de Argentina.

.. image:: img/entidadesconfig.png
   :width: 750 px 
   
Al realizar el alta de un cliente / proveedor también será necesario cargar el CUIT y la condición ante el IVA para poder generar facturas.    

