# cookiecutter-sphinx-js-docs
Cookiecutter template for generating documentattion for javascript/TypeScript projects with 
[sphinx-js](https://github.com/mozilla/sphinx-js), 
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
    * Linux/OsX/MinGW with make capability (see: [this Guide](https://gist.github.com/evanwill/0207876c3243bbb6863e65ec5dc3f058))
    
        `make html`
        
    * Windows
    
        `make.bat html`

#### Notes on the initial configuration

The initial configuration is set up for a pure `typescript` project.

With the source files contained in the `src` directory  in the root directory of the project.
It is also assumed that the root directory of the project containes a `package.json` and a 
`tsconfig.json`, which contains at least a minimal configuration for typedoc as follows:
```
  "typedocOptions": {
    "module": "commonjs"
  },
```

## Credits

This cookiecutter template is based on 
[cookiecutter-pypackage](https://github.com/audreyr/cookiecutter-pypackage).