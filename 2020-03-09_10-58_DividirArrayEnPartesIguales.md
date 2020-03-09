## Inicio parametros
```typescript
const array: number[] = [];
array.length = 3500;
const maxLength = 1000;
array.fill(1); //Lleno el array para que el length no se vuelva tonto
const arrayDivisiones = [] // Contiene todos los arrays de datos
```

```typescript
let splicer = array.length / maxLength; 
for (let i = splicer; i >0; i--) {
    arrayDivisiones.push(array.slice(0, maxLength));
    array.splice(0, maxLength);
}
```

Hago n llamadas, por partes pueda dividir el array, y añado los valores a ArrayDivisiones.

El resultado de esta operación será:

```console
[LOG]: Cantidad de divisiones: ,  4
[LOG]: 1000
[LOG]: 1000
[LOG]: 1000
[LOG]: 500
```
