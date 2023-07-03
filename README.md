# Movie API

> This is a simple movie API that allows you to perform CRUD operations on movies using HTTP requests. The API is built with Go and uses the `github.com/julienschmidt/httprouter` package for routing.

## Features

- Get a list of all movies
- Get details of a specific movie
- Add a new movie
- Update an existing movie
- Delete a movie

## Getting Started

> To run the movie API on your local machine, follow these steps:

1. Make sure you have Go installed on your system. You can download it from the official website:
```shell
 https://golang.org/
```

2. Clone this repository to your local machine or download the source code:
```shel
git clone https://github.com/aron-helu/Crud_Api.git
```

3. Open a terminal or command prompt and navigate to the project's root directory:
```shell
cd Crud_Api
```

4. Run the following command to start the API server:
```shell
go run main.go
```
The server will start running on http://localhost:8000.

## API Endpoints
## Get All Movies
- URL: ``` /movies ```
- Method:  ``` GET ```
- Description: ``` Retrieves a list of all movies```.
- Response: ``` Returns a JSON array containing movie objects.```

## Get a Movie

- URL: ```/movies/:id ```
- Method: ``` GET ```
- Description: ``` Retrieves details of a specific movie.```
- Parameters:
  - ``` id (string) ``` The ID of the movie.
- Response: ```Returns a JSON object representing the movie.```

## Add a Movie
- URL: ```/movies```
- Method: ``` POST ```
- Description: ``` Adds a new movie to the collection. ```
- Request Body: ``` Expects a JSON object representing the movie.```
- Response: ``` Returns the newly created movie as a JSON object.```

## Update a Movie
- URL: ```/movies/:id```
- Method: ``` PUT ```
- Description: ``` Updates an existing movie.```
- Parameters:
  - ```id (string): ``` The ID of the movie.
- Request Body: ``` Expects a JSON object representing the updated movie.```
- Response: ``` Returns the updated movie as a JSON object. ``` 

## Delete a Movie
- URL: ``` /movies/:id ```
- Method: ``` DELETE ```
- Description: ``` Deletes a movie from the collection.```
- Parameters:
  - ```id (string): ``` The ID of the movie.
- Response: ```Returns the updated movie collection as a JSON array.```

## Example Usage
> Here's an example of how you can use cURL to interact with the movie API:

1. Get all movies:

```shell
curl http://localhost:8000/movies
```
2. Get a specific movie:

```shell
curl http://localhost:8000/movies/1
```
3. Add a new movie:

```shell
curl -X POST -H "Content-Type: application/json" -d '{
  "isbn": "123456",
  "title": "New Movie",
  "director": {
    "firstname": "Jane",
    "lastname": "Doe"
  }
}' http://localhost:8000/movies
```

4. Update a movie:

```shell
curl -X PUT -H "Content-Type: application/json" -d '{
  "isbn": "654321",
  "title": "Updated Movie",
  "director": {
    "firstname": "John",
    "lastname": "Smith"
  }
}' http://localhost:8000/movies/1
```

5. Delete a movie:

```shell
curl -X DELETE http://localhost:8000/movies/1
```
> Feel free to explore and interact with the movie API using different HTTP clients or tools.

## Authors

👤 **Aaron Abraham**

- GitHub: [@Aaron](https://github.com/aron-helu)

- LinkedIn: [@Aaron](https://www.linkedin.com/in/aron-abraham-90a4321b0/)


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).



## Show your support

Give a ⭐️ if you like this project!


## 📝 License

This project is [MIT](./LICENSE) licensed.
