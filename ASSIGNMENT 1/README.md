# E-commerce API

A simple FastAPI-based e-commerce API with product management endpoints.

## Features

- View all products
- Filter products by category
- Search products by name (case-insensitive)
- Get in-stock products only
- Store summary with statistics
- Best deals (cheapest & most expensive products)

## Installation

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   - Windows: `venv\Scripts\activate`
   - Linux/Mac: `source venv/bin/activate`
4. Install dependencies:
   ```bash
   pip install fastapi uvicorn
   ```

## Running the Application

Start the server with:
```bash
uvicorn main:app --reload
```

The API will be available at `http://127.0.0.1:8000`

## API Endpoints

### Products
- `GET /` - Welcome message
- `GET /products` - Get all products
- `GET /products/category/{category_name}` - Filter by category
- `GET /products/instock` - Get only in-stock products
- `GET /products/search/{keyword}` - Search products by name
- `GET /products/deals` - Get cheapest and most expensive products

### Store
- `GET /store/summary` - Store statistics and categories

## Testing

Visit `http://127.0.0.1:8000/docs` for interactive API documentation (Swagger UI).

## Sample Data

The API includes 7 sample products across Electronics and Stationery categories.
