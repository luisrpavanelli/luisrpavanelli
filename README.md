# Edge
# API REST en formato JSON. Web service fake (falso) con datos de prueba, pero ideal para aprender y prototipar aplicaciones frontend con un framework Javascript del lado del cliente.
# Podemos crear un API REST, que podremos usar con fines didácticos o para prototipado, ideal cuando estamos aprendiendo a desarrollar con un framework Javascript del lado del cliente, o cuando tenemos que realizar una aplicación frontend sin tener que entretenernos con el desarrollo backend.
# API perfectamente funcional, que admita las operaciones típicas de cualquier API REST estándar, ofreciendo las habituales operaciones través de los distintos verbos del HTTP, pero sin tener que invertir horas de nuestro tiempo para aprovisionarlo. Este tipo de servicios web se conocen como "API RESR fake", pues son realmente datos falsos, únicamente con propósitos de prueba.
# Para poder ser tan rápidos usaremos un sencillo archivo JSON como fuente de datos, donde podremos generar nuestro modelo de datos, con distintas entidades, y datos de prueba. Como servidor REST usaremos un programa llamado "json-server", desarrollado con NodeJS que nos ofrece la posibilidad de tener un servidor web que responde a las operaciones típicas de las API.
# El API REST creado, realizará todas las operaciones posibles sobre nuestros datos (lecturas, modificaciones, inserciones y borrados), almacenando los datos en el archivo JSON. La persistencia de los datos se realiza en el propio archivo de texto JSON, de este modo, en futuros accesos a la aplicación web, el API recordará su estado manteniendo toda la actividad que se haya realizado a lo largo del tiempo.

# Crear un archivo JSON con los datos de nuestra API
# En cualquier carpeta de nuestro ordenador debemos crear el archivo JSON que va a servir de origen de datos para nuestra API. Los datos serán aquellos que necesitemos en nuestra aplicación y en el propio JSON se puede introducir de inicio un conjunto de datos de prueba.
# Podemos ver un ejemplo de datos de muestra, en el siguiente código JSON, que almacena películas y un conjunto de clasificaciones de películas.

{
  "peliculas": [
    {
      "id": 1,
      "nombre": "El sexto sentido",
      "director": "M. Night Shyamalan",
      "clasificacion": "Drama"
    },
    {
      "id": 2,
      "nombre": "Pulp Fiction",
      "director": "Tarantino",
      "clasificacion": "Acción"
    },
    {
      "id": 3,
      "nombre": "Todo Sobre Mi Madre",
      "director": "Almodobar",
      "clasificacion": "Drama"
    },
    {
      "id": 4,
      "nombre": "300",
      "director": "Zack Snyder",
      "clasificacion": "Acción"
    },
    {
      "id": 5,
      "nombre": "El silencio de los corderos",
      "director": "Jonathan Demme",
      "clasificacion": "Drama"
    },
    {
      "id": 6,
      "nombre": "Forrest Gump",
      "director": "Robert Zemeckis",
      "clasificacion": "Comedia"
    },
    {
      "id": 7,
      "nombre": "Las Hurdes",
      "director": "Luis Buñuel",
      "clasificacion": "Documental"
    }
  ],
  "clasificaciones": [
    {
      "nombre": "Drama",
      "id": 1
    },
    {
      "nombre": "Comedia",
      "id": 2
    },
    {
      "nombre": "Documental",
      "id": 3
    },
    {
      "nombre": "Acción",
      "id": 4
    }
  ]
}

# Este archivo JSON tendrá típicamente una extensión .json. En nuestro caso lo podríamos guardar como "db.json". De esta manera ya tenemos todo el código que necesitaremos para crear nuestro API REST fake con unos datos iniciales.

