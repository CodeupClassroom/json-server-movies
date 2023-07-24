# JSON Server for Movies

This repository can be used to have a locally running mock REST API for Movies
using [JSON Server](https://github.com/typicode/json-server).

## Setup

1. Clone this repository
2. From a terminal, move into the project root (this is the default terminal behavior if the project is open in
   IntelliJ).
3. Run `npm install` to download the needed dependencies
4. Run `npm start` to start running JSON server on `http:localhost:3000`

## Populating Data

JSON Server uses the file `db.json` to maintain data for the movies. This file can be edited directly and will change
automatically as various HTTP requests are made. The starting data for this file is the following:

```json
{
  "movies": [
    {
      "title": "Casablanca",
      "rating": "4",
      "id": 1
    },
    {
      "title": "Star Wars: A New Hope",
      "rating": "5",
      "id": 2
    }
  ]
}
```

## Routes

This mock API follows standard REST conventions:

| ROUTE          | METHOD | DESCRIPTION                                                                                         |
|----------------|--------|-----------------------------------------------------------------------------------------------------|
| `/movies`      | GET    | Returns all movies                                                                                  |
| `/movies/{id}` | GET    | Returns a specific movie                                                                            |
| `/movies`      | POST   | Adds a new movie when passed a movie object in the body of the request (no id property needed)      |
| `/movies/{id}` | PUT    | Updates a movie record when passed a movie object in the body of the request (id property required) |
| `/movies/{id}` | DELETE | Deletes a movie record (body can be empty)                                                          |