CovidMaps
Proyecto final de telemática-2020. 

# Descripción 
La aplicación de covidMaps estará implementada mediante un
servidor de página web basada por contenedores la cual hará
una recolección de tiempo real acerca de los contagios que 
suceden a diario en el valle aburrá de covid-19. esto a su vez,
también permitirá ver la comunidad y el sector en los cuales se
encuentran las personas más contagiadas y por ende arrojará
por medio de grafos cuales son los lugares más peligroso y
cuales no tanto. por ende también tendrá una interfaz gráfica
la cual estará construida por medio de Appinventor. 

# Appinventor
El Appinventor tendrá 3 pantallas, en la primera pantalla
estará el menú, en la segunda el formulario  por el cual se 
obtendrá la información de los usuarios y en la tercera estará 
el mapa en el cual se hará evidente los casos y sectores más 
críticos por dicha patología. la información obtenida se actualizará 
por medio de una base de datos y se entregará un reporte actualizado 
a los usuarios. 

# Arquitectura
  #  Dockerfile
Este archivo está directamente relacionado con
el contenedor, el cual se encargará de ejecutar
las instrucciones que serán necesarias a la hora de
de configurar el servidor, además arrojará los servicios
necesarios y ejecutará el archivo .py. 

# Proyecto.py
Acá se contendrá el cuerpo del proyecto(se utilizará
la librería flask de python).En este archivo se
obtendrán los datos enviados por el Appinventor mediante 
la implementación de un método POST y a partir
de estos se buscará la información en una Base de datos   
de los casos actualizados del covid-19 de una localidad 
en específico con base en esto se realizará el gráfico
y el análisis de riesgo de cada sector. según los datos
ingresados por el usuario si este tiene o sospecha de 
presentar los síntomas de dicha patología dicha información 
será suministrada en la base de datos ya establecida.

# BaseDatos.db
Esta Base de datos tendrá la información de los casos 
que hayan sido confirmados de covid-19 en el valle de 
aburrá, incluyendo los datos de los usuarios que
presenten síntomas o en su defecto sean nuevos portadore,
dicha base de datos estará formada o estructurada mediante 
grafos construidos.

# Contenedor de docker.
El contenedor estará implementado en una máquina basada en 
ubuntu versión 18.04, dicho contenedor tendrá todos los archivos, 
es decir, el flash, la versión de python que se utilizará
el apache o servidor que vaya hacer montado, así al momento de establecer
una imagen lo único será presentar el servicio. 

# Tipo de servidor y Firewall. 
Para la seguridad se usará el Ufw como el firewall 
del sistema a su vez habilitando el puerto 80.
como dicho servicio se prestará por medio de servidores
en la nube (en su caso AWS) se activará el puerto 22 y 
se implementarán las configuraciones de los grupos de 
seguridad requeridos.   
