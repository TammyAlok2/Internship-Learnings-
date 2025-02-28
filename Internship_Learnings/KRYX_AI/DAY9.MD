# Greetings :
 Thanks a lot god for everything . 

## Date : 27/02/25 

## Work Started and Completed : 
-  1PM to 6pm 

## Learnings 
 - # FastAPI MongoDB CRUD API

This is a simple CRUD API built with **FastAPI** and **MongoDB** using **Motor**, an asynchronous MongoDB driver. The API allows managing items in a MongoDB collection.

## Features
- Create an item
- Read all items
- Read a single item
- Update an item
- Delete an item
- Async database operations using **Motor**
- Pydantic models for data validation

---

## Installation

### 1. Clone the repository
```sh
git clone https://github.com/your-repo/fastapi-mongodb-crud.git
cd fastapi-mongodb-crud
```

### 2. Create and activate a virtual environment
```sh
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install dependencies
```sh
pip install -r requirements.txt
```

### 4. Configure MongoDB

Create a `.env` file in the root directory and add your MongoDB connection string:
```sh
MONGO_URI=mongodb://localhost:27017
```
Ensure MongoDB is running locally or provide a remote MongoDB connection.

---

## Project Structure
```
fastapi-mongodb-crud/
│── app/
│   ├── main.py            # Entry point of the API
│   ├── database.py        # MongoDB connection setup
│   ├── models.py          # Pydantic models
│   ├── schemas.py         # Data validation schemas
│   ├── routes/
│   │   ├── item_routes.py # CRUD operations for items
│── .env                   # Environment variables
│── requirements.txt       # Project dependencies
│── README.md              # Documentation
```

---

## Running the API

### 1. Start the FastAPI server
```sh
uvicorn app.main:app --reload
```

### 2. Open API Documentation
- Swagger UI: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- Redoc: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## API Endpoints

### 1. Create an Item (POST `/items/`)
**Request Body:**
```json
{
    "name": "Laptop",
    "description": "Gaming Laptop",
    "price": 1200.50,
    "quantity": 5
}
```
**Response:**
```json
{
    "id": "65d8a9f8c29d1f0017e5a2a1",
    "name": "Laptop",
    "description": "Gaming Laptop",
    "price": 1200.50,
    "quantity": 5
}
```

### 2. Get All Items (GET `/items/`)
**Response:**
```json
[
    {
        "id": "65d8a9f8c29d1f0017e5a2a1",
        "name": "Laptop",
        "description": "Gaming Laptop",
        "price": 1200.50,
        "quantity": 5
    }
]
```

### 3. Get a Single Item (GET `/items/{item_id}`)
**Response:**
```json
{
    "id": "65d8a9f8c29d1f0017e5a2a1",
    "name": "Laptop",
    "description": "Gaming Laptop",
    "price": 1200.50,
    "quantity": 5
}
```

### 4. Update an Item (PUT `/items/{item_id}`)
**Request Body:**
```json
{
    "price": 1300.00
}
```
**Response:**
```json
{
    "message": "Item updated successfully"
}
```

### 5. Delete an Item (DELETE `/items/{item_id}`)
**Response:**
```json
{
    "message": "Item deleted successfully"
}
```

---

## Technologies Used
- FastAPI
- Uvicorn
- MongoDB
- Motor (async MongoDB driver)
- Pydantic (data validation)

---

## License
This project is licensed under the MIT License.

---

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you’d like to change.

---

## Contact
For any inquiries, feel free to reach out at [your-email@example.com](mailto:your-email@example.com).

