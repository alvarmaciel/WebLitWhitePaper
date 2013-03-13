Para empezar como traductor de la *wiki de estándares de alfabetizaciones web* de Mozilla, usá GitHub para mandar un mensaje solicitando ser agregado como colaborador en el repositorio `WebLitWhitePaper`. Lo que deberá hacer despuués dependerá de si el esfuerzo por la traducción en su idioma ya está en marcha. Puede averiguar si la traducción a su idioma ya ha empezó, mirando si hay una rama (branch) con el nombre de su idioma en la página [principal principal del repositorio] (https://github.com/alvarmaciel/WebLitWhitePaper/). Vaya al link "Switch Branches" para ver la lista de ramas (branchs).

## Traducción a un idioma nuevo

To translate the *Ruby on Rails Tutorial* book to a new language, first send a request to be added as a collaborator on the GitHub repository. Then clone the repository, create a new branch, and configure the remote branch before pushing the repository up:

para traducir la *wiki de estándares de alfabetizaciones web* a un idioma nuevo, primero envie un mensaje para ser agregado como colaborador en el repositorio GitHub. Después:
1. clone el repositorio
2. cree una nueva rama
3. configure la rama remota antes de publicar (push) al repositorio

```sh
$ git clone git@github.com:alvarmaciel/WebLitWhitePaper.git ## así clonan
$ cd rails_tutorial_translation ## entran el directorio de trabajo
$ git checkout -b spanish ## crean la nueva rama
$ git config branch.spanish.remote origin ## Configuran la rama
$ git config branch.master.merge refs/heads/spanish ## Configuran la rama
$ git push origin spanish # Publican - push - a la r
```

## Contributing to an existing translation

To contribute to an existing translation, first send a request to be added as a collaborator on the GitHub repository. Then clone the repository and track the language's branch:

```sh
$ git clone git@github.com:mhartl/rails_tutorial_translation.git
$ cd rails_tutorial_translation
$ git branch --track spanish origin/spanish
$ git checkout spanish
```
Once you have a tracking branch, send me a message through GitHub requesting to be added as a collaborator on the Heroku project for your language. After receiving a message that you have been added, you should configure your local repository as follows:

```sh
$ git remote add heroku git@heroku.com:rails-tutorial-spanish.git
```

You will then be able to deploy your translation using a `git push`:

```sh
$ git push heroku spanish:master
```

## Running the app

The HTML source of the *Ruby on Rails Tutorial* is distributed along with a minimal Rails app. To run it, install the necessary gems and then run the server:

```sh
$ bundle install
$ rails server
```

The book will now be running on `http://localhost:3000`.

# Translating the book

The HTML source of the book is in the directory `public/book`. You should make your edits directly on these HTML files, making commits as you go along:

    <make some changes>
    $ git add .
    $ git commit -m "<describe changes>"

When you want to make your changes available to other translators, push them up to GitHub:

    $ git push origin spanish

If you are collaborating with other translators, you should first pull in their changes:

```sh
$ git pull --rebase origin spanish
$ git push origin spanish
```

(The `--rebase` option makes it possible to abandon the pull if there are too many conflicts.)

Once you are satisfied with a set of changes, deploy them to the public site:

```sh
$ git push heroku spanish:master
```

Your translation will now be available at <tt>spanish.railstutorial.org</tt>.

## Site design

Please feel free to customize the design of the translated site to match your needs. (I do ask that you retain the links to the Rails Tutorial home page, the screencasts, and the print edition.)

## License

The HTML source of the Rails Tutorial book is available under the [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-nc-sa/3.0/), which allows translation for noncommercial purposes.

# Math

There's no reason to have any math here, but I think it's cool that GitHub lets you. For example, here's the time-independent Schr&ouml;dinger equation for hydrogen: \[ -\frac{\hbar^2}{2m}\nabla^2\psi - \frac{e^2}{2\tau r}\psi = E\psi, \]
where \( \tau = 2\pi \). (Why set \( \tau = 2\pi \)? [Here's why](http://tauday.com/).)

Fuente: https://github.com/mhartl/rails_tutorial_translation/wiki
