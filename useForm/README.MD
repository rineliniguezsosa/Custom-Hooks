# useForm

Recuerda que los Custom hooks son funciones que extraen la logica de los componentes y te permitiran reutilizarlas

1.-Importa la funcion useForm pensemos que estamos en nuestro Search.js
<br>
2.-Desestructuramos los valores de retorno de la funcion useForm y le definimos un estado inicial
<br>
3.-Desestructuramos los valores de values
<br>
4.-Definimos por cada onChange la referencia a la función handleInputChange la cual actualizara los estados de los inputs mediante sus atributos name
<br>

```javascript
    import React from 'react
    import { useForm } from './tudirectorio/useForm'; //1)

    export default function Search(){
    const [values, handleInputChange] = useForm({
        Searchvalues:"" //2
        Searchvalues2:""
    })

    const { Searchvalues,Searchvalues2 } = values; //3

    const handlesearch = (e)=>{
        e.preventDefault()
        console.log(Searchvalues,Searchvalues2)

    }
    return (
        <div>
            <form onSubmit={handlesearch}>
              <input
              type="text"
              onChange={handleInputChange} //4
              name="Searchvalues"
              value={Searchvalues}
              >
              </input>

              <input
              type="text"
              onChange={handleInputChange} //4
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

