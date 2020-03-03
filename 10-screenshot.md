# Screenshot

https://docs.cypress.io/api/commands/screenshot.html#Command-Log

Con la función cy.screenshot( , { } ) es posible tomar un captura o screenshot de la pantalla o interfaz de nuestra aplicación en cualquier momento durante la ejecución del testing.

Esta funcionalidad permite algunas opciones de configuración muy útiles como: blackout para ocultar elementos o información que no deba ser expuesta en la captura, clip para recortar y capturar sólo una región de la interfaz, capture: ‘fullPage’ para hacer una captura de toda la página y no solo lo visible en el viewport del navegador, entre otras.

Los archivos de las imágenes capturadas (con formato png) son guardados en subcarpetas identificadas con el nombre de la suite de tests en ejecución, dentro del directorio /screenshots creado automáticamente por Cypress.

Es recomendable excluir los screenshots del repositorio github agregando la carpeta correspondiente al archivo .gitignore.