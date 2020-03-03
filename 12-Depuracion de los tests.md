# Depuración de los tests

Cyrpress provee dos herramientas para hacer depuración durante la ejecución de los tests:

- debugger 

    que detiene la ejecución del código y permite el acceso a la consola de inspección tanto en el código de los tests como de la aplicación que estamos probando.

```js
cy.contains('button', 'Crear').as('botonCrar').then(() => {
    debugger;
})
```

- .debug() 

    que es una función encadenable a cualquier otra función de Cypress, y que al igual que debugger, permite la depuración del código durante la ejecución de un flujo de pruebas.

```js
cy.contains('button', 'Crear').as('botonCrar').debug()
```