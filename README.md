# Student Management System

A simple student management web application built with FastAPI, SQLite, Jinja2 templates, HTML, and CSS. The application demonstrates complete CRUD functionality for student records.

## Features

- **Create:** Add a new student with name, age, gender, marks, course, image URL, and status.
- **Read:** View all student records on the home page or open a single student profile.
- **Update:** Edit existing student information.
- **Delete:** Remove a student record from the database.
- Automatically creates the SQLite `students` table when the application starts.

## Technologies and Concepts Used

- Python
- FastAPI
- Pydantic
- SQLite
- Jinja2 Templates
- HTML and CSS
- Uvicorn
- CRUD operations
- Form handling
- HTTP routing
- Template rendering
- Database integration
- Data validation

## Project Structure

```text
std-management/
|-- main.py
|-- students.db
|-- templates/
|   |-- Home.html
|   |-- add-student.html
|   |-- edit-student.html
|   `-- single-std.html
`-- README.md
```

## Prerequisites

- Python 3.10 or later
- pip

## Installation and Setup

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   cd std-management
   ```

2. Create and activate a virtual environment:

   **Windows**

   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

   **macOS/Linux**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required packages:

   ```bash
   pip install fastapi "uvicorn[standard]" jinja2 python-multipart
   ```

## Run the Application

Start the FastAPI development server:

```bash
uvicorn main:app --reload
```

Open the application in a browser:

- Application: http://127.0.0.1:8000
- Interactive API documentation: http://127.0.0.1:8000/docs

## Application Routes

| Method | Route | Description |
|---|---|---|
| `GET` | `/` | Displays all students |
| `GET` | `/student/add` | Opens the add student form |
| `POST` | `/students/add` | Creates a student |
| `GET` | `/students/{std_id}` | Displays a student profile |
| `GET` | `/students/edit/{std_id}` | Opens the edit student form |
| `POST` | `/students/edit/{std_id}` | Updates a student |
| `POST` | `/std/delete/{std_id}` | Deletes a student |

## Database

The application uses a local SQLite database named `students.db`. The `students` table contains:

- `id`
- `name`
- `age`
- `gender`
- `marks`
- `course`
- `image`
- `status`

The table is created automatically when `main.py` starts.

## Learning Outcome

Although this is a basic project, it helped me understand and practically implement FastAPI fundamentals. Building it provided hands-on experience in using routing, form handling, Pydantic models, Jinja2 templates, SQLite database operations, and CRUD functionality together in a real application.

