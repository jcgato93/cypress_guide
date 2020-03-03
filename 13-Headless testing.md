# Headless testing

Cuando estamos realizando End-to-end testing en un ambiente real de producción, por lo general no tenemos acceso a la interfaz gráfica del servidor. En estos casos se hace necesario entonces tener la posibilidad de ejecutar todo el flujo de pruebas como lo hemos definido, pero sin la simulación visual de lo que sucede en el navegador durante todo el proceso. Para esto, Cypress dispone de la funcionalidad Headless testing.

El cambio necesario para realizar un Headless testing es básicamente la sustitución del argumento open por run, en la ejecución del script de Cypress en las configuraciones del archivo package.json, quedando los scripts de la siguiente manera:


        ""e2e"": ""cypress run --project ./test"",

Al ejecutar npm run test ya no se ejecutará en el test runner de Cypress sino en un navegador interno sin interfaz gráfica; sin embargo, Cypress registrará toda la ejecución en un video que guardará en la carpeta /videos en el sistema de archivos del servidor además de mostrar todas las salidas del proceso en la terminal de línea de comandos.

Al igual que como sucede con los screenshots la recomendación es que la carpeta /videos se excluya del repositorio Git a través del .gitignore para evitar un uso innecesario de recursos adicionales del servidor.        