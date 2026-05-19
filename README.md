# MovieRater API

A RESTful API for managing and rating movies, built with Django REST Framework. Supports full CRUD operations on movies, directors and ratings.

---

## Tech Stack

- **Python 3**
- **Django**
- **Django REST Framework**
- **SQLite** (default) / PostgreSQL ready

---

## Features

- Create, read, update and delete movies
- Manage directors linked to movies
- Submit and retrieve movie ratings
- RESTful endpoints following standard HTTP conventions

---

## Project Structure

```
MovieRaterApi/
├── api/                    # API layer — serializers, views, URLs
│   ├── serializers.py
│   ├── views.py
│   └── urls.py
├── movierater/             # Core app — models and business logic
│   ├── models.py
│   └── admin.py
├── manage.py
└── README.md
```

---

## Installation & Setup

**1. Clone the repository**
```bash
git clone https://github.com/federicovalino/MovieRaterApi.git
cd MovieRaterApi
```

**2. Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate      # macOS / Linux
venv\Scripts\activate         # Windows
```

**3. Install dependencies**
```bash
pip install django djangorestframework
```

**4. Run migrations**
```bash
python manage.py migrate
```

**5. Start the server**
```bash
python manage.py runserver
```

---

## API Endpoints

### Movies

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/movies/` | List all movies |
| POST | `/api/movies/` | Create a new movie |
| GET | `/api/movies/<id>/` | Retrieve a movie |
| PUT | `/api/movies/<id>/` | Update a movie |
| DELETE | `/api/movies/<id>/` | Delete a movie |

### Ratings

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/movies/<id>/ratings/` | Get ratings for a movie |
| POST | `/api/movies/<id>/ratings/` | Submit a rating |

---

## Movie Object

```json
{
  "id": 1,
  "title": "Inception",
  "director": "Christopher Nolan",
  "rating": 4.8,
  "description": "A thief who enters the dreams of others."
}
```

---

## Built With

- [Django](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
