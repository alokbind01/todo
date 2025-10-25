# Django ToDo Application

A simple and elegant ToDo application built with Django that allows users to manage their daily tasks efficiently.

## Features

- ✅ **Add Tasks**: Create new tasks with a simple form
- ✅ **Mark as Complete**: Mark tasks as done with a single click
- ✅ **Mark as Incomplete**: Undo completed tasks if needed
- ✅ **Edit Tasks**: Update existing task descriptions
- ✅ **Delete Tasks**: Remove tasks permanently
- ✅ **Task Organization**: Separate views for pending and completed tasks
- ✅ **Responsive Design**: Bootstrap-powered UI that works on all devices
- ✅ **Real-time Updates**: Tasks are organized by creation and update time

## Project Structure

```
ToDO/
├── manage.py                 # Django management script
├── db.sqlite3               # SQLite database file
├── templates/               # HTML templates
│   ├── home.html           # Main application page
│   └── edit_task.html      # Task editing form
├── todo/                   # Main application
│   ├── models.py           # Task model definition
│   ├── views.py            # Application views
│   ├── urls.py             # URL patterns
│   ├── admin.py            # Admin configuration
│   └── migrations/         # Database migrations
├── ToDo_main/              # Django project settings
│   ├── settings.py         # Project configuration
│   ├── urls.py             # Main URL routing
│   └── views.py            # Project-level views
└── env/                    # Virtual environment
```

## Installation & Setup

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd ToDO
```

### Step 2: Create Virtual Environment

```bash
python -m venv env
```

### Step 3: Activate Virtual Environment

**On Windows:**
```bash
env\Scripts\activate
```

**On macOS/Linux:**
```bash
source env/bin/activate
```

### Step 4: Install Dependencies

```bash
pip install django
```

### Step 5: Run Database Migrations

```bash
python manage.py migrate
```

### Step 6: Start the Development Server

```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## Usage

1. **Adding Tasks**: Enter your task in the input field at the bottom of the page and click "Add"
2. **Completing Tasks**: Click the green "Mark as Done" button next to any pending task
3. **Editing Tasks**: Click the blue "Edit" button to modify a task description
4. **Deleting Tasks**: Click the red "Delete" button to permanently remove a task
5. **Undoing Tasks**: Click the yellow "Undo" button to move completed tasks back to pending

## Technical Details

### Models

- **Task Model**: Contains task description, completion status, and timestamps
  - `task`: CharField (max 250 characters)
  - `is_completed`: BooleanField (default: False)
  - `created_at`: DateTimeField (auto-generated)
  - `updated_at`: DateTimeField (auto-updated)

### Views

- `home`: Displays all tasks (pending and completed)
- `addtask`: Creates new tasks
- `mark_as_done`: Marks tasks as completed
- `mark_as_undone`: Reverts completed tasks to pending
- `edit_task`: Updates task descriptions
- `delete_task`: Removes tasks permanently

### Database

- Uses SQLite3 for development (included in Django)
- Database file: `db.sqlite3`
- Migrations are included in the `todo/migrations/` directory

## Technologies Used

- **Backend**: Django 5.2.7
- **Database**: SQLite3
- **Frontend**: HTML5, Bootstrap 5.3.0, Font Awesome Icons
- **Language**: Python 3.8+

## Development

### Running Tests

```bash
python manage.py test
```

### Creating Superuser (Admin Access)

```bash
python manage.py createsuperuser
```

Then visit `http://127.0.0.1:8000/admin/` to access the Django admin interface.

### Making Changes

1. Modify models in `todo/models.py`
2. Create migrations: `python manage.py makemigrations`
3. Apply migrations: `python manage.py migrate`
4. Update views and templates as needed

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Future Enhancements

- [ ] User authentication and personal task lists
- [ ] Task categories and tags
- [ ] Due dates and reminders
- [ ] Task priority levels
- [ ] Search and filter functionality
- [ ] Export tasks to various formats
- [ ] Dark mode theme
- [ ] Mobile app version

## Support

If you encounter any issues or have questions, please open an issue in the repository or contact the development team.

---

**Happy Task Managing!** 🎯
