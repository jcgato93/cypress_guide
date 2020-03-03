# Variables de entorno y configuración

https://docs.cypress.io/guides/guides/environment-variables.html#Setting

Una de las formas más sencillas es insertando las variables de entorno en el 
archivo cypress.json de lasiguiente manera 

```json
{
  "projectId": "128076ed-9868-4e98-9cef-98dd8b705d75",
  "env": {
    "foo": "bar",
    "some": "value"
  }
}
```

y para retornar los valores de dichas variables

```js
Cypress.env()       // {foo: 'bar', some: 'value'}
Cypress.env('foo')  // 'bar'
Cypress.env('some') // 'value'
```