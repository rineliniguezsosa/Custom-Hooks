# useForm

Recuerda que los Custom hooks son funciones que extraen la logica de los componentes y te permitiran reutilizarlas

1.-Importa la funcion useForm pensemos que estamos en nuestro Search.js
<br>
2.-Desestructuramos los valores de retorno de la funcion useForm y le definimos un estado inicial

```javascript
    import React from 'react
    import { useForm } from './tudirectorio/useForm'; //1)

    export default function Search(){
    const [values, handleInputChange] = useForm({
        Searchvalues:"" //2
        Searchvalues2:""
    })

    const { Searchvalues,Searchvalues2 } = values;

    const handlesearch = (e)=>{
        e.preventDefault()
        console.log(Searchvalues,Searchvalues2)

    }
    return (
        <div>
            <form onSubmit={handlesearch}>
              <input
              type="text"
              onChange={handleInputChange}
              name="Searchvalues"
              value={Searchvalues}
              >
              </input>

              <input
              type="text"
              onChange={handleInputChange}
              name="Searchvalues2"
              value={Searchvalues2}
              >
              </input>

              <button type="submit" className="btn btn-primary">Search</button>
            </form>
        </div>
    )
    }
```

