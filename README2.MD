PASOS PARA  DESPLEGAR PROYECTO  POKEDEX EN AZURE .

Primer paso -- iniciamos sesion en nuestra cuenta azure creada con nuestro correo institucional que nos genera un año gratis ..
paso 2 :  en la pagina principal de azure despues de iniciar sesion  hay  un icono llamado app service 
paso 3 : creamos una app web , verificamos que la subcripcion sea azure for student. y luego le ponemos un nuevo nombre ala instancia -- en la pila de entorno de aplicacion seleccionamos 
node 20 lts que fue el que nos funciono, luego de sistema operativo ponemos windows. la infraestructura gratis es la f1 que es para estudiantes, tenemos en cuenta que todo este correcto 


paso 4 : presionamos el boton azul en la parte izquierda inferior de la pantalla que dice revisar y crear  y esperamos y luego crear miramos  unos minutos hasta que nuestra instancia este creada  en pantalla dira implementacion en curso ..

paso 5 : iremos al recurso creado y luego verificamos el dominio  que este correctamente creado ese dominio lo copiamos y lo pegamos en el navegador.

paso 6 despliegue de aplicacion  .. Entramos a herramientas avanzadas y precionamos ir en la parte superior donde dice debug seleccionamos cmd , en la parte izquierda  ponemos el archivo dist que se genero al  abrir el proyecto en visual estudio code  e iniciar estos comandos ..  npm install  y despues que se intalara ponemos npm run buils  y estos nos genera una carpeta dist que comprimiremos los archivos de su interior en .zip  y luego lo desplegamos ala derecha de la pantalla y de esa manera  se desplegara la app en la instancia..

paso 7 . correccion de errores .. al subir la app nos pasa algo que  no salen las fotos de los pokemones y es por que la ruta de la simagenes esta en una carpeta que se llama pokedex-angular y no esta dentro de esta carpeta , lo que hacemos es crear la carpeta pokedex-angular y meterle la carpeta asset  dentro del proyecto . ya con esto  ya saldrian las imagenes de nuestro proyecto y estaria final mente desplegado ..

paso 8 implementacion de seguridad.. en este caso tendriamos que crear un archivo que se llama web.config y dentro de este en xml incluimos las directivas de seguridad y ya con eso  podriamos  incluirle seguridad a nuestra pagina, tenemos que tener en cuenta lo que incluimos en ese archivo ya que si se configura mal alteraria la app , 
en nuestro caso nos quedo con un nivel de seguridad A ya que cuando nos quedaba en A+  se nos corria las animaciones y despues de tanto intentar nos quedo en A , muchas gracias por la atencion , nuestros portafolios son  estos  ..  Rafael torres  https://zealous-plant-06f27420f.5.azurestaticapps.net/#habilidaes    javier teheran magallanez https://tecnoflow1994.blob.core.windows.net/tecnologico/portafolio.html  ,, sebastian cuadro zapata https://nextfaiz.blob.core.windows.net/kaixa/sebastiancuadro/hoja_de_vida.html y el de  stiven laurens https://tecnoaccount30.blob.core.windows.net/tecnologico/index%20portafolio.html  y luis castro https://tecnoaccountluis1.blob.core.windows.net/tecnologico/index.html 
