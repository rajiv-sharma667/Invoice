# Invoice Management API

This is a simple RESTful API built using Django and Django REST Framework (DRF) to manage invoices and their details. The API allows users to create and update invoices with multiple details in a single request.

## Project Description

The **Invoice Management API** is a backend API designed to manage invoices and their details for a business or service. It allows users to:
- Create a new invoice with multiple invoice details.
- Update an existing invoice and its details.

The `Invoice` model includes:
- `invoice_number` (unique identifier for the invoice)
- `customer_name` (name of the customer)
- `date` (invoice date)

The `InvoiceDetail` model includes:
- `description` (description of the product/service)
- `quantity` (quantity of the product/service)
- `price` (unit price of the product/service)
- `line_total` (total for this line item, which is `quantity * price`)

## Technologies Used

- **Django**: A Python-based web framework for building scalable web applications.
- **Django REST Framework (DRF)**: A powerful toolkit for building Web APIs in Django.
- **SQLite**: The default database for Django, used to store invoice and invoice detail data.
- **Python 3.x**: Programming language used for the backend.

## Setup Instructions

### Step 1: Install Dependencies

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/invoice.git
    cd invoice
    ```

2. Set up a virtual environment:

    ```bash
    python3 -m venv venv
    source env/bin/activate  # For Linux/Mac
    # On Windows use: env\Scripts\activate
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

### Step 2: Set Up the Database

1. Run the database migrations to create the necessary tables:

    ```bash
    python manage.py migrate
    ```

2. Create a superuser (optional, for accessing the Django admin interface):

    ```bash
    python manage.py createsuperuser
    ```

### Step 3: Run the Development Server

To start the Django development server, run:

```bash
python manage.py runserver
```

### Step 4: Access the API

The API endpoints will be available at:
http://127.0.0.1:8000/api/invoices/

### API Endpoints
1. POST /api/invoices/
2. PUT /api/invoices/{invoice_id}/
