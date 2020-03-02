# Variables, Fixtures y Alias

Debido a que Cypress es asíncrono, la forma de definir y usar variables en el código de los tests es diferente a como se hace regularmente en JavaScript.

Los fixtures son estructuras u objetos JSON definidos en archivos individuales que se pueden reutilizar en cualquier momento de la secuencia de ejecución de los tests. Para poder hacer referencia a ellos posteriormente es necesario asignarles un alias.

La forma de incorporar un fixture en cada uno de los tests, sería incorporándolo en el Hook beforeEach() de la manera siguiente:

```js
cy.fixture(<archivo.json>).as(<alias>)
```

y para poder hacer uso de éste, se le debe asignar un alias:

```js
cy.get('@alias').then((var) => {
    // --- en este ambito ya se puede usar como una variable más

    cy.get('input').type(var)
})
```

Al usar el símbolo “”@"" en el selector, se hace referencia a una variable (fixture) y no a un elemento de la interfaz.

NOTA: Tenga en cuenta que las funciones de Cypress no regresan un valor en sí mismas, ya que internamente funcionan de manera asíncrona.