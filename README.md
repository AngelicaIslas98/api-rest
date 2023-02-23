# Api-rest

Esta API contiene diferentes rutas de acceso a una aplicacionde películas. Los datos solicitados se entregan en formato **JSON: "Title", "Director", "Year", "Rating".** Adicionalmente se realizó una conexión a una API externa para simular una base de datos de la lista de usuarios. 

La API permite el uso de los metodos CRUD o GET, POST, PUT y DELETE. 

# Configuración de entorno
- Node.JS
- Visual Studio Code
- Postman
- JSON Viewer (extensión del navegador)
 
# Dependencias 
Instalación desde la terminal:
 
 Ejecución para Node
 
 `npm init --y`
 
 
 Framework de node
 
 `npm express`
 
 
 Modulo para ver por consola las peticiones del servidor
 
 `npm morgan `


# Método GET 
Solicitu desde el navegador con url http://localhost:3000/test
Solicitud desde navegador con url http://localhost:3000/api/movies
Solicitud desde navegador con url http://localhost:3000/api/users

`{`

`"title": "Alien",`

`"director ": "James Cameron",`

`"year": "1979",`

`"rating": "9.6"`

`}`


## Ejecución desde Postman
### Configuración de solicitudes con postman

**HEADERS**

**KEY:** Content-type

**VALUE:** application/json

**BODY**
Selección de **"raw"**
http://localhost:3000/api/movies


# Método POST
Desde postman con url http://localhost:3000/api/movies
Permite agregar elementos en formato **JSON**, los datos se guardaran si se cumple con las variables requeridas (title, director, year, rating) con aumento automatico del ID, en caso contrario se enviara un estado 500 con un mensaje de error.


# Método PUT
Permite actualizar/cambiar los datos en memoria de una película, 
http://localhost:3000/api/movies/:id, a tráves de un ciclo se busca la coincidencia  del ID de la película y modificará los datos enviados. 


# Método DELETE
Se buscará la coincidencia del ID ingresado para elimiar los datos en memoria.
http://localhost:3000/api/movies/:id


# Acceder a una API externa
Se realizo una conexión con una API  https://jsonplaceholder.typicode.com/
desde el navegador o postman se pueden obtener los datos con la url http://localhost:3000/api/users
