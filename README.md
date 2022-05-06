[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=7802598&assignment_repo_type=AssignmentRepo)
# monedas: Ejercicio de TDD con Jasmine y Node
### Ejercicio de TDD, usando Jasmine para Node

## Realización del ejercicio
Este ejercicio está pensado para hacerlo con Visual Studio Code, pero puedes en realidad hacerlo con cualquier editor.

Necesitarás tener instalado Node.js para poder ejecutarlo. Por tanto, [descárgalo](https://nodejs.org/en/download/) e instálalo antes de hacer nada más.

* https://nodejs.org/en/download/

A continuación usando la línea de órdenes, haz lo siguiente:

1. Clona este repositorio y entra dentro del directorio que ha creado (*monedas_ejercicio_tdd_jasmine_node*).
2. Ejecuta: 

```npm install --save-dev jasmine```

4. Modifica el fichero *package.json* incluyendo la siguiente línea:

```, "scripts": { "test": "jasmine" }```

5.  Modifica el fichero  *spec/support/jasmine.json* para que la línea que indica el valor de ```spec_dir``` quede así:


```"spec_dir": "./spec"```

6. Copia el fichero *monedas-spec.js.template* en el directorio *spec* y renómbralo para que se llame, finalmente: *monedas-spec.js*
7. Abre Visual Studio Code y haz los ejercicios que se indican en dicho fichero: *monedas-spec.js*


Los ficheros de configuración, deberían haber quedado así:

**package.json**

```
{
  "devDependencies": {
    "jasmine": "^4.1.0"
  },
  "scripts": {
    "test": "jasmine"
  }
}
```

***spec/support/jasmine.json***
```
{
  "spec_dir": "./spec",
  "spec_files": [
    "**/*[sS]pec.js"
  ],
  "helpers": [
    "helpers/**/*.?(m)js"
  ],
  "env": {
    "stopSpecOnExpectationFailure": false,
    "random": false
  }
}
```