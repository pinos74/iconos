
# Objetivos del curso Gitlab de IPAP
## Objetivo general
Promover el trabajo ordenado y colaborativo para el desarrollo de sistemas dentro de los equipos de
las diferentes áreas de tecnologías de los organismos, a través del aprendizaje en el uso de software
libre que permite el control de versiones de las aplicaciones.
# herramientas web para aprender ramas en Git
## Learn Git Branching
Esta aplicación está diseñada para ayudar a los principiantes a manejar los poderosos conceptos que hay detrás del trabajo con ramas (branches) en Git. Esperamos que disfrutes la aplicación y tal vez incluso ¡que aprendas algo!
https://learngitbranching.js.org/?locale=es_AR

# Hello Git
Git is a software that allows you to keep track of changes made to a project over time. Git works by recording the changes you make to a project, storing those changes, then allowing you to reference them as needed.
https://www.codecademy.com/courses/learn-git/lessons/git-workflow/exercises/hello-git

![Poncho](docs/node_modules/ar-poncho/img/poncho.gif)

### [Ver listado de íconos](//argob.github.io/iconos)

# Uso

Para utilizar los iconos son necesarios los archivos de la carpeta **dist**.
En el html hay que llamar al archivo *icono-arg.css*.

```html
<link href="path/to/css/icono-arg.css" rel="stylesheet">
```

Algo importante, es que la relación de las carpetas css y fonts deben quedar como están para que funcionen las rutas relativas.

# Desarrollo

El archivo editable con todos los íconos es [src/Iconos.ai](src/Iconos.ai).
Los iconos exportados en svg van en **src/_icons/**

### Instalación de ambiente de desarrollo

En caso de necesitar ver en local el resultado, tener en cuenta que requiere algunas librerías adicionales, por lo que es necesario instalarlas previamente.

```sh
npm install
```

Para compilar la tipografía se utiliza [Font Custom](https://github.com/FontCustom/fontcustom). 
La instalación requiere **Ruby 1.9.3+**, **WOFF2** y **FontForge** con las funciones de consola para Python.

```sh
# En Mac (requiere tener instalado [Homebrew](https://brew.sh/index_es)
brew tap bramstein/webfonttools
brew update
brew install woff2
brew install sfnt2woff
brew install fontforge
brew install eot-utils
gem install fontcustom
bundle install

# En Linux
sudo apt-get install libjpeg-dev libtiff5-dev libpng-dev libfreetype6-dev libgif-dev libgtk-3-dev libxml2-dev libpango1.0-dev libcairo2-dev libspiro-dev python3-dev ninja-build cmake build-essential gettext
sudo apt-get install zlib1g-dev
git clone https://github.com/fontforge/fontforge.git fontforge && cd fontforge && mkdir build && cd build && cmake -GNinja .. && ninja && ninja install
cd ../../
git clone https://github.com/bramstein/sfnt2woff-zopfli.git sfnt2woff-zopfli && cd sfnt2woff-zopfli && make && mv sfnt2woff-zopfli /usr/local/bin/sfnt2woff
cd ../
git clone --recursive https://github.com/google/woff2.git && cd woff2 && make clean all && sudo mv woff2_compress /usr/local/bin/ && sudo mv woff2_decompress /usr/local/bin/
cd ../../
gem install fontcustom
bundle install
```

### Para compilar

```sh
bundle exec fontcustom compile -F     # Compila la tipografía y templates
bundle exec fontcustom watch          # Compila cuando las imágenes svg se cambian / agregan / eliminan
```

# iconos
Repo para actividad integradora del IPAP

