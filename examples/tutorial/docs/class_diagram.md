
# Diagrama de clases de Flaskr

Este diagrama muestra las clases principales del blog, sus atributos y la relación entre usuarios y publicaciones.

```mermaid
[classDiagram

class user {
    +INTEGER id
    +TEXT username
    +TEXT password
}

class post {
    +INTEGER id
    +INTEGER author_id
    +TIMESTAMP created
    +TEXT title
    +TEXT body
}

user "1" --> "0..*" post : escribe](https://github.com/shafaqmajid/pallets-flask/blob/develop/examples/tutorial/docs/class_diagram.md)
```

