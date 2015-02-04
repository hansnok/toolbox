﻿Archivo de ayuda y consideraciones para el uso correcto del bloque Toolbox. 

1.- Lo primero que se debe hacer es instalar el bloque Toolbox a su Moodle, esto lo hace por medio de descomprimir o descargar la carpeta "Toolbox"
y la tiene que pegar o mover en la carpeta donde tenga su Moodle (comunmente htdocs o www) y coloque la carpeta Toolbox dentro de la carpeta "blocks"
2.- Una vez copiado el bloque, ingrese a su moodle por medio de su browser y se le abrir� la p�gina de administraci�n de Moodle, donde se le instalar� el 
bloque a su Moodle.  
3.- Una vez instalado el bloque, se tiene que configurar, esto se realiza por medio del sitio de administraci�n (Administraci�n del Sitio/Extensiones/Bloques/Toolbox). Dentro de la configuraci�n ya tiene valores predeterminados, 
lo que debe hacer es elegir cuando si quiere que se actualice (Activaci�n del Cron), la hora de comienzo y la hora de termino (con esto se define el 
rango en el cual el Cron va a ejecutarse) y por �ltimo se define el intervalo en el que se quiere activar el Cron (esto realiza cada cuando tiempo se quiere
ejecutar el procedimiento). 
4.- Para que el bloque logre funcionar, se tiene que configurar un CronTab para el bloque. El c�digo para la configuraci�n del Crontab es el siguiente: 

crontab -e 
Add the following line: 
*/5 * * * * /usr/bin/wget -O /dev/null http://localhost/mymoodle/admin/cron.php 
(change the URL as appropriate for your site)
 
Esto se debe hacer por medio de Linux, un programa recomendable es PuTTY. 

Para m�s informaci�n se puede revisar el sitio de Moodle (http://docs.moodle.org/22/en/RedHat_Linux_installation)

Por �ltimo se puede obtener informaci�n acerca del funcionamiento del Crontab en las siguentes p�ginas: 

http://platea.pntic.mec.es/curso20/48_edicionhtml-profundizacion/html2/plataforma/moodle.html
http://dns.bdat.net/documentos/cron/x50.html
 




