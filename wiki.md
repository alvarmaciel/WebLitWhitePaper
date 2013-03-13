Para empezar como traductor de la *wiki de estándares de alfabetizaciones web* de Mozilla, usá GitHub para mandar un mensaje solicitando ser agregado como colaborador en el repositorio `WebLitWhitePaper`. Lo que deberá hacer despuués dependerá de si el esfuerzo por la traducción en su idioma ya está en marcha. Puede averiguar si la traducción a su idioma ya ha empezó, mirando si hay una rama (branch) con el nombre de su idioma en la página [principal principal del repositorio] (https://github.com/alvarmaciel/WebLitWhitePaper/). Vaya al link "Switch Branches" para ver la lista de ramas (branchs).

## Traducción a un idioma nuevo

To translate the *Ruby on Rails Tutorial* book to a new language, first send a request to be added as a collaborator on the GitHub repository. Then clone the repository, create a new branch, and configure the remote branch before pushing the repository up:

para traducir la *wiki de estándares de alfabetizaciones web* a un idioma nuevo, primero envie un mensaje para ser agregado como colaborador en el repositorio GitHub. Después:
1. clone el repositorio
2. cree una nueva rama
3. configure la rama remota antes de publicar (push) al repositorio

```sh
$ git clone git@github.com:alvarmaciel/WebLitWhitePaper.git ## así clonan
$ cd WebLitWhitePaper ## entran el directorio de trabajo
$ git checkout -b español ## crean la nueva rama
$ git config branch.español.remote origin ## Configuran la rama
$ git config branch.master.merge refs/heads/español ## Configuran la rama
$ git push origin español # Publican - push - a la rama
```

## Contribuir a una traducción existente

Para contribuir a una traducción existene, primero envie una solicitud para ser agregado/a como colaborador en el repositorio de GitHub
Luego clone el repositorio y siga la rama (branch) de su idioma

```sh
$ git clone git@github.com:alvarmaciel/WebLitWhitePaper.git ## así clonan
$ cd WebLitWhitePaper ## entran el directorio de trabajo
$ git branch --track spanish origin/español ## Siguen la rama Español
$ git checkout espñol ## Eligen al rama para trabajar en ella
```

Ahora pueden publicar sus traducciones usando `git push`:


# Translating the book

La traducción la realizamos usando sintaxys MarkDown, en el directorio `weblitwiki` están los documentos fuentes para editar, vayan commiteando (commit) a medida que van traduciendo. Esto prepara los archivos para ser publicados (push) en la rama (branch):

    <make some changes>
    $ git add . ## Prepara los cambios en los archivos
    $ git commit -m "<describe changes>" #registra los cambios y registra el comentario a fin de hacer un seguimento de los mismos

Cuando quieren hacer que sus cambios estén disponibles para otros traductores, empujelos (push) hasta GitHub:


    $ git push origin español

Si está colaborando con otros traductores, primero tienen que hacer `pull` en sus cambios


```sh
$ git pull --rebase origin español ## Hace el pull
$ git push origin español ## Empuja los cambios
```


Fuente de este tutorial: https://github.com/mhartl/rails_tutorial_translation/wiki
