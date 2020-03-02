# Ejecución de Scripts

Seguramente en algun momento necesitaremos utilizar comandos del sistema o de nodeJs para 
ejecutar Scripts para hacer cosas como limpiar la base de datos antes o despues de las pruebas.

Para esto cypress nos brinda los metodos .exec() para correr comandos del del y .task() para 
comandos desde el sistema.

```js
cy.exec('npm run test:clean')
```


También se pueden ejecutar comandos de tipo shell o scripts externos, con la función
```js
cy.task(...)
```