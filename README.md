### Got Biz Logic ?
- Clone this repo or copy the code exactly into yours and complete the tasks the service layers. 
- Do not touch any other file other than the service layer (Important)

### Todos:
- Create the following 5 service methods in the service layers
> **AuthorService** : createAuthor and getAllAuthors service methods are needed 
>
> **BookService** : getAllBooksByAuthorId, createBook, getBookById

## To help you with testing in Postman. Below are the expected responses:

- POST: http://localhost:8080/authors
- Expecting status code of : 201
- Expected Response: 
```{
    "id": 3,
    "name": "Maya Angelo"
}
```


-GET:  http://localhost:8080/authors
- Expecting status code of : 200
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

- GET: http://localhost:8080/authors?name=s
- Expecting status code of : 200
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
- Expecting status code of : 201
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

-GET: http://localhost:8080/authors/3/books
- Expecting status code of : 200
- Expected Response:
```[
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

-GET: http://localhost:8080/books/5
- Expecting status code of : 200
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

