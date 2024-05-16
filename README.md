# Pokédex Angular


Mi grupo esta conformado por Javier Teheran Magallanez  --- Sebastian Cuadro Zapata  --- Stiven Laurens Iriarte -- luis Castro --- Rafael Torres 




Primer paso para ejecutar la aplicación en local y verificar que funciona
 Abrimos el comprimido que se descargó en el repositorio de github.
 
 Recorremos los archivos 1 entramos a la carpeta pokedex-angular.
 




Después lo abrimos en visual estudio code.  Y en la terminal ponemos-  npm install.
Y esperamos que se instale.
 

Despeues ejecutamos el comando npm run build para que nos cree el archivo dist que es el que desplegaremos en azure .
 

Con npm run build 
Se crea la carpeta build se nos crea la carpeta dist que es la que luego comprimiremos en .zip y desplegaremos en azure.  

Esa carpeta la comprimimos en .zip y la desplegamos en azure.
 

Creamos una web app en azure llamada teheranPokedex

Y entramos a herramientas administrativas  
 
Entramos a debug  console  y seleccionaos cmd  

Arrastramos la carpeta comprimida en zip   y nos quedara asi 
 

Encontramos un error que no me cargan las imágenes  en la app desplegada—eso lo corregimos  metiendo la carpeta asset  dentro de una carpeta pokedex-angular y la subimos en el medio para que no se descomprimir  y se suba la carpeta tal , ya que esa carpeta tiene las imágenes. De esta manera ya desplegamos la app 
 

Para agregarle seguridad a la aplicación 
Debemos crear un archivo llamado web.config. y le agregamos las directivas de seguridad 
Dentro de la carpeta que ya está desplegada la app  <?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <system.webServer>
        <httpProtocol>
            <customHeaders>
                <add name="X-Frame-Options" value="DENY" />
                <add name="X-XSS-Protection" value="1; mode=block" />
                <add name="X-Content-Type-Options" value="nosniff" />
                <add name="Strict-Transport-Security" value="max-age=31536000; includeSubDomains" />
                <add name="Content-Security-Policy" value="default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com https://kit-free.fontawesome.com; img-src 'self' https://keilermora.github.io data: https://assets.pokemon.com; font-src 'self' https://fonts.gstatic.com https://beta.pokeapi.co https://kit-free.fontawesome.com; connect-src 'self' https://beta.pokeapi.co;" />
                <add name="Referrer-Policy" value="no-referrer" />
                <add name="Permissions-Policy" value="geolocation=(), microphone=()" />
            </customHeaders>
        </httpProtocol>
    </system.webServer>
</configuration>


Probamos la app web dentro de la herramienta brindada por el maestro .
 
Agregamos nuestro link 
https://teheranpokedex.azurewebsites.net/
 

Por el momento pude configurar hasta A ya que agrgue otras directivas, pero me subía a A+ pero me rodaba la vista el usuario podría no tener una buena visibilidad en la app web del pokedex.

Ahora subiré el código a git hub 
 Creamos un repositorio  llamado pokedex .
 
Seguimos los pasos de git para cargar nuestro repositorio 
 
echo "# pokedex." >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/jatemast/pokedex..git
git push -u origin main

 
Aquí están los portafolios de mis compañeros, igual también estarán  en el readme de mi  repositorio de git .
Ya  tengo mi repositorio creado y publico .
 

Este es el link .
https://github.com/jatemast/pokedex..git



más información en el readme   de   github.


















[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![codecov](https://codecov.io/gh/keilermora/pokedex-angular/branch/master/graph/badge.svg?token=9E0D28IOFT)](https://codecov.io/gh/keilermora/pokedex-angular)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

[https://keilermora.github.io/pokedex-angular/](https://keilermora.github.io/pokedex-angular/)

La aplicación muestra el listado y el detalle de los Pokémon de las primeras 3 generaciones.

La imagen que representa un Pokémon en el listado muestra las variaciones que estos tuvieron durante las primeras versiones, desde la versión Green (1996) hasta la version Emerald (2005).

Los detalles de un Pokémon individual muestra sus estadísticas base y los registros de la Pokédex de las diferentes versiones.

El proyecto fue desarrollado usando la librería de JavaScript [Angular](https://angular.io/) para crear la interfaz de usuario, en comunicación con la Api RESTful [PokéAPI](https://pokeapi.co/).

## Requisitos mínimos

- [Nodejs](https://nodejs.org) con soporte de largo plazo (LTS).
- Un navegador web

## Ambiente de pruebas

Ejecutar en la raíz del proyecto:

```
npm start
```

## Referencias

- [Angular](https://angular.io/): One framework.
- [Angular Folder Structure](https://angular-folder-structure.readthedocs.io/en/latest/): Create a skeleton structure which is flexible for projects big or small.
- [Font Awesome](https://fontawesome.com/): The web's most popular icon set and toolkit.
- [Normalize.css](https://necolas.github.io/normalize.css/): A modern, HTML5-ready alternative to CSS resets.
- [PokéAPI](https://pokeapi.co/): The RESTful Pokémon API.
