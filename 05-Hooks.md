# Hooks

Cypress incluye los Hooks de acuerdo a las definiciones y casos de uso definidos por el framework de pruebas Mocha, del cual los adopta.
https://docs.cypress.io/guides/references/bundled-tools.html#Mocha

Los Hooks son funciones o métodos que se ejecutan en determinados momentos del flujo de ejecución de los tests.

Los que usaremos en nuestro proyecto son:

- before(): es una función que se ejecuta una vez antes de la ejecución de todos los tests del mismo grupo.
- beforeEach(): es una función que se ejecuta antes de cada test individual.
- afterEach(): es una función que se ejecuta después de cada test individual.
- after(): es una función que se ejecuta una vez, al finalizar la ejecución de todos los tests del mismo grupo.

Opcionalmente, se puede incluir el método .skip(), encadenado a alguna de las definiciones de test de la siguiente manera: it.skip( ... ), para indicar a Cypress que este test se omitirá durante la ejecución.