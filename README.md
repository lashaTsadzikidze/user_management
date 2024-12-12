
# User Management System

This project is a Django-based application for managing users. It provides features such as user registration, login, and CRUD operations for managing user accounts. It includes a role-based permissions system where admins can assign users to specific groups (`default` and `mod`) with predefined permissions.

## Features

- User registration and authentication.
- Create, read, update, and delete user profiles.
- Admin dashboard for managing users and permissions (requires superuser privileges).
- Role-based permissions:
  - `default` group: Add posts and view posts.
  - `mod` group: Add posts, delete posts, and view posts.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/lashaTsadzikidze/user-management.git
   cd user-management
   ```

2. **Set up a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply migrations**:
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser** (to access the admin dashboard):
   ```bash
   python manage.py createsuperuser
   ```

   #### Enter User details
    - Username: The username for the superuser.
    - Email Address: (Optional).
    - Password: Set a secure password (you’ll need to confirm it).
    example:
    ```
    Username: admin
    Email address: admin@example.com
    Password: ********
    Password (again): ********
    Superuser created successfully.
    ```

6. **Run the development server**:
   ```bash
   python manage.py runserver
   ```

7. **Access the application**:
   - Open your browser and navigate to `http://127.0.0.1:8000`.
   - To access the admin dashboard, visit `http://127.0.0.1:8000/admin` and log in with the superuser credentials.

## Setting Up Groups and Permissions

1. Log in to the admin dashboard (`/admin`) using the superuser credentials.
2. Navigate to the **Groups** section.
3. Create the following groups:
   - `default`
   - `mod`
4. Assign permissions to the groups:
   - For the `default` group:
     - Add the permissions `Can add post` and `Can view post`.
   - For the `mod` group:
     - Add the permissions `Can add post`, `Can delete post`, and `Can view post`.
5. Assign users to the appropriate groups via the **Users** section in the admin dashboard.

## Usage

### Admin Features
- Add post, delete any post and ban user accounts.
- Manage user permissions and groups.

### End-User Features
- Register and log in.
- Users in the `default` group:
  - Can add and view posts.
- Users in the `mod` group:
  - Can add, view, and delete posts.
