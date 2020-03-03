# Stubs, Spies y Clocks

https://docs.cypress.io/guides/guides/stubs-spies-and-clocks.html

- Stubs: 
    proporciona una manera programática de simular, sustituir o tomar control del comportamiento esperado de funciones o eventos que suceden en la interfaz de nuestra aplicación.

- Spies: 
    permiten intervenir en los llamados a funciones para determinar si fueron llamadas durante la ejecución del testing y qué parámetros recibieron en esa llamda.

- Clocks: 
    proporciona una forma de alterar programáticamente la hora y fecha del entorno durante la ejecución del testing.

NOTA; No se recomienda el uso de estas funcionalidades cuando se realiza End-to-end testing, particularmente con Firebase, ya que pudieran generar comportamientos inesperados y no deseados como resultado de las pruebas. Estas funcionalidades son más útiles para pruebas de otro tipo.    