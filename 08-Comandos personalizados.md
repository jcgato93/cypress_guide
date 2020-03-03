# Comandos personalizados

La idea es que cada conjunto o suite de tests sea independiente entre sí; sin embargo, hay ocasiones en que varios tests o grupos de tests requieren ejecutar instrucciones comunes. Los comandos personalizados son una manera muy conveniente de agrupar varias instrucciones para reutilizarlas o compartirlas entre diferentes lugares de nuestro flujo de testing en una o varias suites.

La definición de los comandos personalizados se hace en el archivo comands.js en la carpeta /support de la siguiente manera:

```js
Cypress.Commands.add('miComandoPersonalizado', (<paranms>) => {
    // --- instrucciones comunes agrupadas como comando personalizado
})
```

luego para hacer uso del comando personalizado, se debe invocar como cualquier método propio de Cypress:

```js
cy.miComandoPersonalizado(<params>)
```