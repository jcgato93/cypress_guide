# Comandos principales de Cypress

## Controlar el browser

- cy.visit(): para cargar una URL
- cy.reload(): para cargar la URL actual
- cy.go('back'): para ir hacia atrás o adelante en la navegación

## Selección de elementos

- cy.get('.selector'): para seleccionar según un selector html/css
- cy.contains('text'): para seleccionar de acuerdo al contenido
- cy.contains('.selector', 'texto'): para seleccionar según el selector y el contenido

## Interactuar con los elementos

- cy.get('.selector').click(): para hacer click sobre un elemento
- cy.get('.selector').dblclick(): para hacer dblclick sobre un elemento
- cy.get('input').type(): para escribir un texto
- cy.get('input').clear(): para limpiar un texto
- cy.get('checkbox').check(): para marcar check
- cy.get('checkbox').uncheck(): para quitar el check
- cy.get('select').select('item'): para seleccionar un item en una lista desplegable

Cypress permite la encadenación de muchos de estos y otros comandos.


Ejemplo test pagina de login

```js
/// <reference types="cypress" />
'use strict'

import * as userLogin from '../fixtures/user-login.json'


describe('Test Login', () => {
    var email = null;
    var password = null;
    before(() => {
        email = userLogin.email
        password = userLogin.password
    })

    beforeEach(() => {
        cy.visit('/login')
        cy.wait(3000);                        
        cy.get('body').then((body) => {
            if(body.find('.avatar').length > 0) {
                cy.get('.avatar').click()
                cy.wait(2000)
                cy.contains('Logout').click()
            }
        })                           
    })

    it('should visit login page', () => {
        cy.visit('/login')
    })

    it('should sign up', () => {
        cy.visit('/login')       
        // buscar por el atributo placeholder         
        cy.get('input[placeholder$="Email"').type(email,{delay: 100})
        cy.get('input[placeholder$="Password"').type(password,{delay: 100})
        cy.get('input[placeholder$="Confirm password"').type(password,{delay: 100})
        cy.contains(':submit', 'Submit').click()

        cy.wait(3000)
    })

    it('should sign in', () => {
        cy.visit('/login')
        // Buscar un elemento que contenga el siguiente texto
        cy.contains('Returning user?').click()
        cy.wait(2000)
        // Buscar por id
        cy.get('#mat-input-0').type(email,{delay: 100})
        cy.get('#mat-input-1').type(password,{delay: 100})
        cy.contains(':submit', 'Submit').click()

        cy.wait(3000)
    })
})
```