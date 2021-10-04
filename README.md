# Ejercicios con Objetos, JSON y Local Storage

### Objetos

1. Crea tres objetos `usuario1`, `usuario2`, `usuario3` que tengan las propiedades `nombreUsuario` y `contrasenia` como strings. 
2. Definí una función `saludar` que reciba como parámetro un objeto y que modifique el HTML de tu página para que aparezca un h1 que diga "Hola, {nombreUsuario}".
3. Probá tu función con los tres objetos definidos antes.  
4. Definí una función `modificarNombreDeUsuario` que reciba dos parametros: un objeto `usuario` y un string `nuevoNombre`. La función debe retornar el objeto con la propiedad `nombreUsuario` modificada para tener el valor de `nuevoNombre`. 
5. Probá tu función con los tres objetos definidos antes. 
6. Definí una función `modificarContrasenia` que reciba dos parametros: un objeto `usuario` y un string `nuevaContrasenia`. La función debe retornar el objeto con la propiedad `contrasenia` modificada para tener el valor de `nuevaContrasenia`. 
7. Probá tu función con los tres objetos definidos antes. 
8. Crea la función `convertirAJSON`. La función debe recibir un objeto `usuario` como parámetro y retornar el objeto convertido a JSON. 
9. Crea la función `convertirDesdeJSON`. La función debe recibir una cadena JSON `objetoJSON` y retornar la cadena convertida a un objeto de Javascript. 
10. Probá tus funciones con los tres objetos definidos antes. 
11. Definí la función `guardarEnLocalStorage` que reciba como parámetro **un objeto de Javascript** y un string, y guarde en localStorage la cadena con el string como nombre de la clave (Recordá que antes de guardar un objeto en localStorage hay que convertirlo a JSON: usá la función `convertirAJSON` que declaraste antes)
12. Definí la función `leerDesdeLocalStorage` que reciba como parámetro un string `clave` y retorne **un objeto de Javascript** con los datos guardados bajo esa clave en localStorage. (Utilizá la función `convertirDesdeJSON`!)

### Ejercitación integradora

Tratá de usar las funciones declaradas en los ejercicios anteriores. 

1. Crea una pagina que tenga un titulo que diga "Hola!" y un botón que diga "Iniciar sesión"
2. Al hacer click en el botón Iniciar Sesión, debe hacerse visible un formulario con un campo `usuario` y otro `contraseña`, y un botón para enviar el form. 
3. Definí un objeto `usuario` en javascript en donde estén definidas dos propiedades: nombreUsuario y contrasenia (o usá los objetos definidos antes). 
4. Si los datos ingresados por el usuario en el form coinciden con los guardados en el objeto, la web debe:
    1.  Mostrar como saludo "Hola {nombreUsuario}"
    2.  Ocultar el botón "iniciar sesión"
    3.  Ocultar el formulario para iniciar sesión
    4.  Mostrar dos botones nuevos: `Cambiar mis datos`, `Cerrar sesión`. 
    5.  Pista: Definí una variable global para guardar si el usuario inició sesión o no, y determinar a partir de ella qué elementos se deben mostrar en la página. 
5. Si el usuario hace click en "cerrar sesión", el titulo debe volver a decir "Hola!" y el botón "Iniciar sesión" debe volver a ser visible. 
6. Si el usuario hace click en "Cambiar mis datos", se abre un formulario con un campo `usuario` y otro `contraseña`, y un botón para enviar el form. Al enviarse, se deben modificar las propiedades nombreUsuario y contrasenia del objeto `usuario`. 

Una vez completados todos los puntos anteriores, queremos que la sesión del usuario persista aunque cierre la página. 

1. Al iniciar sesión, se deben guardar en `localStorage` el nombre del usuario y la propiedad: `sesionIniciada: true`. 
2. Al saludar al usuario, el título debe consumir la propiedad guardada en `localStorage`. 
3. Al cerrar sesión, la propiedad `sesionIniciada` debe pasar a ser `false`. 
4. Para determinar si la sesión está iniciada o no, usar la propiedad `sesionIniciada` desde `localStorage`. 
5. Si el usuario cambia su nombre o contraseña desde el formulario, los datos en `localStorage` deben actualizarse también. 
