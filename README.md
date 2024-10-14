# Task Manager API

A simple Task Manager API built using Django and Django REST Framework. 
This API allows user to create, read, update and delete tasks.

## Features

- Create a task
- View all tasks
- View a single task by ID
- Update a task
- Delete a task

## Requiremments

- Python 3.x
- Django 4.x
- Django REST Framework 3.x

## Installation
1. Clone the repository: 
	```bash
		git clone https://github.com/Sam-spec-ops/task-manager-api.git
		cd task-manager-api
	```

2. Create and activate a virtual environment: 
	- **On macOS/Linux**:
		```bash
			python3 -m venv env
			source env/bin/activate
		```

	- **On Windows**:
		```bash
			python -m venv env
			.\env\Scripts\Activate
		```

3. Install the required dependencies:
	```bash
		pip install -r requirements.txt
	```

4. Apply the migrations:
	```bash
		python manage.py makemigrations
		python manage.py migrate
	```

5. Start the development server:
	```bash
		python manage.py runserver
	```

## Api Endpoints

### Task Endpoints:

- **GET** `/api/tasks/` - Retrieve all tasks
- **POST** `/api/tasks` - Create new task
- **GET** `/api/tasks/<id>/` - Retrieve a specific task by its ID
- **PUT** `/api/tasks/<id>/` - Update a specific task by its ID
- **DELETE** `/api/tasks/<id>/` - Delete a specific task by its ID

### Example Request Bodies

#### Creating a Task:
```json
{
	"title": "Finish project",
	"description": "Complete Django API project",
	"completed": true
}