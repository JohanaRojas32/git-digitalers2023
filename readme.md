# Clase 06 - Git intro

## Configuracion inicial

´´´sh
git config --global user.name "Johana Rojas"
git config --global user.email "joohanarojas96@gmail.com"
´´´´

## Verificando la configuracion inicial, si quedo todo piola!

´´´sh
git config --get-regexp user
´´´´

## Iniciando un repositorio de git 

´´sh
git init
´´


## Areas del repositorio de GIT

3 areas

* Working Directory (WD): directrorio de trabajo donde se van agregando o quitando los archivos durante el desarrollo (escritorio de trabajo)

* Starting Area (SA): Area de control de cambios. Area de confirmacion intermedia. Area temporal/intermedia

* Local Repo (LR): Una caja donde voy guardando las fotos que voy sacando.


## Estado de los archivos

* untracked: Archivos que estan en el WD pero GIT no les esta dando seguimiento

* unmodified: Archivo que GIT ya esta siguiendo y con respecto al WD no fueron modificados

* modified: Archivos que se encuentran en el repositorio (estan siendo seguidos por GIT) pero difieren con lo que se encuentra en el area de trabajo WD

* stateg: Archivos que estan en el area temporal intermedia



## ¿como chequeo el estado?

´´sh
git status
´´
