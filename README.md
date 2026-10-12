# Employee & Department REST API

A database-backed REST API for managing employees and departments built with Django REST Framework.

## Setup Instructions

1. Clone the repository
2. Create a virtual environment: `python -m venv venv`
3. Activate the environment: `source venv/bin/activate` (Windows: `venv\Scripts\activate`)
4. Install dependencies: `pip install -r requirements.txt`
5. Run database migrations: `python manage.py migrate`
6. Start the development server: `python manage.py runserver`

## API Documentation

### Departments
*   `GET /api/departments/` - List all departments
*   `POST /api/departments/` - Create a department
*   `GET /api/departments/<id>/` - Retrieve a department
*   `PUT/PATCH /api/departments/<id>/` - Update a department
*   `DELETE /api/departments/<id>/` - Delete a department

### Employees
*   `GET /api/employees/` - List all employees (Paginated)
*   `POST /api/employees/` - Create an employee (assigns to department via `department` ID)
*   `GET /api/employees/<id>/` - Retrieve an employee
*   `PUT/PATCH /api/employees/<id>/` - Update an employee
*   `DELETE /api/employees/<id>/` - Delete an employee

### Search & Filter
*   **Search by name:** `GET /api/employees/?search=john`
*   **Filter by department:** `GET /api/employees/?department=<id>`