# Joke API

This is a simple REST API built with Express.js that provides endpoints for managing a collection of jokes. The API allows you to retrieve random jokes, get jokes by ID, filter jokes by type, create new jokes, update existing jokes, and delete jokes.

## Endpoints

### 1. GET a random joke

- **URL**: `/random/`
- **Method**: GET
- **Response**: Returns a random joke object as JSON.

### 2. GET a specific joke

- **URL**: `/jokes/:id`
- **Method**: GET
- **Parameters**: `id` (required) - The ID of the joke to retrieve.
- **Response**: Returns the joke object with the specified ID as JSON.

### 3. GET jokes by filtering on the joke type

- **URL**: `/filter`
- **Method**: GET
- **Query Parameters**: `type` (required) - The type of jokes to filter by.
- **Response**: Returns an array of joke objects with the specified type as JSON.

### 4. POST a new joke

- **URL**: `/jokes`
- **Method**: POST
- **Request Body**: JSON object with `text` and `type` properties.
- **Response**: Returns the newly created joke object as JSON.

### 5. PUT a joke

- **URL**: `/jokes/:id`
- **Method**: PUT
- **Parameters**: `id` (required) - The ID of the joke to update.
- **Request Body**: JSON object with `text` and `type` properties.
- **Response**: Returns the updated joke object as JSON.

### 6. PATCH a joke (update only the type)

- **URL**: `/jokes/:id`
- **Method**: PATCH
- **Parameters**: `id` (required) - The ID of the joke to update.
- **Request Body**: JSON object with `type` property.
- **Response**: Returns the updated joke object as JSON.

### 7. DELETE a specific joke

- **URL**: `/jokes/:id`
- **Method**: DELETE
- **Parameters**: `id` (required) - The ID of the joke to delete.
- **Response**: Returns the deleted joke object as JSON.

### 8. DELETE all jokes

- **URL**: `/all`
- **Method**: DELETE
- **Query Parameters**: `key` (required) - The master API key.
- **Response**: Returns an array of all deleted jokes as JSON.

## Installation

1. Clone this repository: `git clone https://github.com/your-username/joke-api.git`
2. Install dependencies: `npm install`
3. Start the server: `npm start`

The server will be running on `http://localhost:3000`.

## Usage

You can test the endpoints using tools like Postman or curl. Here are some example requests:

- GET a random joke: `curl http://localhost:3000/random/`
- GET a specific joke: `curl http://localhost:3000/jokes/42`
- GET jokes by type: `curl http://localhost:3000/filter?type=Puns`
- POST a new joke: `curl -X POST -H "Content-Type: application/json" -d '{"text":"Why did the tomato turn red?","type":"Food"}' http://localhost:3000/jokes`
- PUT a joke: `curl -X PUT -H "Content-Type: application/json" -d '{"text":"Why did the tomato turn red? Because it saw the salad dressing!","type":"Food"}' http://localhost:3000/jokes/42`
- PATCH a joke: `curl -X PATCH -H "Content-Type: application/json" -d '{"type":"Wordplay"}' http://localhost:3000/jokes/42`
- DELETE a joke: `curl -X DELETE http://localhost:3000/jokes/42`
- DELETE all jokes: `curl -X DELETE http://localhost:3000/all?key=4VGP2DN-6EWM4SJ-N6FGRHV-Z3PR3TT`

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.
