### Got Biz Logic ?
- Clone this repo (KUDOS IF YOU CLONE AND FIGURE THINGS OUT) **or** copy the code into yours then **complete the tasks in the service layers**. 
- https://github.com/MikailaAkeredolu/devLogicNeededForServiceLayer
- **Do not** use or modify one of your older projects. IF YOU CAN'T CLONE START NEW PROJECT
- **Do not touch any other file other than the service layer AND properties file** (Important)

### Todos:
- Create the following 5 service methods in your service layers
> **AuthorService** :
- createAuthor
- getAllAuthors
>
> **BookService** :
- getAllBooksByAuthorId
- createBook
- getBookById

## To help you with testing in Postman.
### Below are the expected responses if your service methods work properly:

- POST: http://localhost:8080/authors
- Expected Response: 
```
{
    "id": 3,
    "name": "Maya Angelo"
}
```
<br />

- GET:  http://localhost:8080/authors
- Expected Response:
```
[
    {
        "id": 1,
        "name": "Ralph Ellison"
    },
    {
        "id": 3,
        "name": "Maya Angelo"
    }
]
```

<br />

- GET: http://localhost:8080/authors?name=s
- Expected Response:
```
[
    {
        "id": 1,
        "name": "Ralph Ellison"
    },
    {
        "id": 2,
        "name": "Jack Daniels"
    }
]
```

<br />

- POST: http://localhost:8080/authors/3/books
- Expected Response: 
```
    {
    "id": 5,
    "title": "caged birds sing",
    "isbn": 3456,
    "author": {
        "id": 3,
        "name": "Maya Angelo"
    }
}
```

<br />

- GET: http://localhost:8080/authors/3/books
- Expected Response:
```
[
    {
        "id": 4,
        "title": "Google it",
        "isbn": 12345,
        "author": {
            "id": 3,
            "name": "Maya Angelo"
        }
    },
    {
        "id": 5,
        "title": "caged birds sing",
        "isbn": 3456,
        "author": {
            "id": 3,
            "name": "Maya Angelo"
        }
    }
]
```

<br />

- GET: http://localhost:8080/books/5
- Expected Response:
```
{
    "id": 5,
    "title": "caged birds sing",
    "isbn": 3456,
    "author": {
        "id": 3,
        "name": "Maya Angelo"
    }
}
```
 **Do not touch any other file other than the service layer AND properties file** (Important)
