# cookiecutter-sphinx-js-docs
Cookiecutter template for generating documentattion for javascript/TypeScript projects with sphinx-js, 
wich also works with [readthedocs](https://readthedocs.org/)

## Prerequirements
For the documentation to be generated you need 
[node.js](https://nodejs.org/en/)
and
[Python](https://www.anaconda.com/download/)

1. Install javascript/TypeScript documentation generator (`jsdoc/typedoc`)
    * javascript

    `npm install -g jsdoc`
    * TypeScript

    `npm install -g typedoc`

2. Install the python dependencies to generate the documentation

    `pip install -r docs/requirenets.txt` 
    
## Usage

1. Initializing the docs
    Open a terminal/git-bash in the root folder of your project and run:

        `cookiecutter gh:s-weigand/cookiecutter-sphinx-js-docs`

    This will create the `.readthedocs.yml` for the documentation to work with 
    [readthedocs](https://readthedocs.org/) 
    and `docs` forlder which holds some boilerplate documentation for your project.

2. Generating docs
    
    Change in the docs folder (`cd docs`) and run:    
    * Linux/OsX/MinGW
    
        `make html`
        
    * Windows
    
        `make.bat html`


## Credits

This cookiecutter template is based on [cookiecutter-pypackage](https://github.com/audreyr/cookiecutter-pypackage)