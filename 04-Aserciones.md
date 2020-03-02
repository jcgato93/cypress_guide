# Aserciones

Basicamente nos permite comprobar si un test esta bien o no.

Cypress utiliza Chai como libreria de aserciones
[Chai Assertions](https://docs.cypress.io/guides/references/assertions.html)

Ejemplo de asercion

```js
it('should sign up', () => {
        cy.visit('/login')                
        cy.get('input[placeholder$="Email"').type(email,{delay: 100})
        cy.get('input[placeholder$="Password"').type(password,{delay: 100})
        cy.get('input[placeholder$="Confirm password"').type(password,{delay: 100})
        cy.contains(':submit', 'Submit').click()

        cy.wait(3000)

        // para indicar que el elemento definido por .selector no debería estar presente en el DOM
        cy.get('mat-error').should('not.exist')

        // para indicar que sí debería existir y estar visible.
        // cy.get('mat-error').should('be.visible')
    })
```