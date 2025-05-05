
# Repositorio `Ejercicios-ABD`

Repositorio con los ejercicios de la asignatura “Análisis Bayesiano de
Datos”

# Licencia

[Repository Ejercicios-ABD](https://github.com/DV-Morillo/Ejercicios-ABD)
© 2025 by [Daniel Morillo](https://github.com/DaniMori), todos los
derechos reservados.

## Attributions

### Rstudio project template

This project makes use of the
[rproj-template](https://github.com/DaniMori/rproj-template) Github
template created by [Daniel Morillo](https://github.com/DaniMori) and
licensed under the [Creative Commons Attribution 4.0 International
license](https://creativecommons.org/licenses/by/4.0).

# Project installation

## Software components

Start by installing the following software components:

- [R version
  4.4.3](https://cran.rstudio.com/bin/windows/base/old/4.4.3/): In
  Windows, using the [binary
  installer](https://cran.rstudio.com/bin/windows/base/old/4.4.3/R-4.4.3-win.exe)
  is recommended.

<!-- -->

- [Rstudio Desktop](https://posit.co/download/rstudio-desktop/):
  Although not strictly necessary, it is recommended to install the
  Rstudio IDE; for strict reproducibility, use build [2024.12.1+563 for
  Windows
  10/11](https://download1.rstudio.org/electron/windows/RStudio-2024.12.1-563.exe).

<!-- -->

- [Git client](https://git-scm.com/download): Install the Git client in
  order to be able to clone locally the project repository. On Windows,
  use [the 64-bit Windows
  installer](https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/Git-2.48.1-64-bit.exe).

## Installing the project locally

This project is hosted as a GitHub repository. It can be cloned as a
local Git repository following [these
instructions](https://book.cds101.com/using-rstudio-server-to-clone-a-github-repo-as-a-new-project.html#step---2)
(steps 2 through 7). Note that this will create a local copy of
(‘clone’) the GitHub repository as an Rstudio project in the folder
specified. The URL that must be entered into the `Repository URL` text
box is:

    https://github.com/DV-Morillo/Ejercicios-ABD.git

**IMPORTANT:** It is totally unrecommended to clone a git repository
inside a cloud storage folder (e.g., Dropbox, OneDrive). Please note
that GitHub serves the purpose of backing up the repository, so no cloud
storage is necessary. Similarly, cloning the repository in a network
folder may cause problems with the `renv` environment (see below); do it
at your own risk!

After cloning the repository, the Rstudio project will open
automatically in the Rstudio IDE. If it doesn’t, or you want to return
later to the project in Rstudio, you can do so by double clicking on the
file `rstudio_project.Rproj` that has been created in the project folder
when cloning the repository.

**NOTE:** It is common practice to avoid using and versioning
`.Rprofile` files. However, this project uses [package
`renv`](https://cran.r-project.org/package=renv) to create a
reproducible environment, which needs the `.Rprofile` file that lives in
the root directory of the project. **Please DO NOT delete or edit this
file**; it will install and activate the `renv` package and make it
ready for restoring the environment.

## Restoring the environment

The reproducible environment created by `renv` must be restored to
install all the packages this project needs to be built properly. If
`renv` does not initialize automatically (check the console for messages
about this), you will need to manually install the package first:

``` r
install.packages("renv")
```

Once it is successfully installed, use the “renv” -\> “Restore library…”
button in Rstudio’s “Packages” tab to restore the environment.
Alternatively, you can type in the console:

``` r
renv::restore(prompt = FALSE)
```

# Repository structure

The file structure of this repository is as follows:

    Ejercicios-ABD
    |
    |--- notebooks (The exercise notebooks will be in this folder)
    |
    |--- R         (R functions created for this project live here)
    |
    |--- renv      (System library necesssary for `renv` to work. DON'T TOUCH)
    |
    |--- src       (Source scripts that implement the main processes)
    |
    |--- www       (Project assets, e.g., images, bibliography files, etc.)

Use the folders as indicated to store the different files and generate
the outputs of the processes.
