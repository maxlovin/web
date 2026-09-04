# Flask Blog

A full-featured blog application built with Flask, featuring user authentication, an admin-only posting system, comments and a rich text editor.

## Features

- **User authentication** — register, log in, and log out (via Flask-Login)
- **Admin-only controls** — only the admin account (first registered user) can create, edit, and delete posts
- **Blog posts** — create, edit, and delete posts with a title, subtitle, image URL, and rich-text body
- **Rich text editing** — powered by CKEditor for formatting post content
- **Comments** — logged-in users can comment on posts; commenter avatars are generated via Gravatar
- **Responsive design** — styled with Bootstrap 5


### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate    # on Windows: .venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables (see below), then run the app:
   ```bash
   python main.py
   ```

5. Visit `http://localhost:5001` in your browser.

## Usage

- **Register an account** at `/register`. The **first user to register becomes the admin** (user ID 1) and gains access to creating, editing, and deleting posts.
- **Create a post** at `/new-post` (admin only).
- **Comment on a post** by logging in and visiting any post page.

## Project Structure

```
.
├── main.py              # Application entry point, routes, and models
├── forms.py              # WTForms form definitions
├── requirements.txt      # Python dependencies
├── templates/             # Jinja2 HTML templates
├── static/                # CSS, JS, and image assets
└── posts.db               # SQLite database (auto-created on first run)
```
