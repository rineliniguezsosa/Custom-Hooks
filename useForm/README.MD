# useForm

Recuerda que los Custom hooks son funciones que extraen la logica de los componentes y te permitiran reutilizarlas

1.-Importa la funcion useForm pensemos que estamos en nuestro Search.js

2.-Desestructuramos los valores de retorno de la funcion useForm y le definimos un estado inicial

```javascript
    import React from 'react
    import { useForm } from './yourdirectorio/useForm'; //1)

    const [values, handleInputChange] = useForm({
     Searchvalues:"" //2
    })
```

