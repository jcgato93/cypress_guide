# Integrando Cypress al proyecto

Instalar dependencia de Cypress

        $ npm i cypress -D

Instalar dependencia de [chancejs](https://chancejs.com/)
para crear datos aleatorios

        $ npm i chance -D


## Modificar script de test

En el archivo package.json , en el script de "e2e" cambiar 
el valor por "cypress open"


## Configurar Cypress

Tan solo se corre el siguiente comando 

        $ npm run e2e

Dentro de este se recomiendo hacer un enlace al repositorio
para que cypress guarde las capturas de pantalla de las pruebas en el repositorio.