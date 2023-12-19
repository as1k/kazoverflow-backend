# Kazoverflow

## Introduction

Welcome to the Kazoverflow web application! This project aims to replicate the core features of 
StackOverflow, providing a platform for users to engage in a community-driven question and answer 
environment.

## Features

- **Registration:** Users can create a new account.
- **Authentication:** Registered users can log in.
- **Category:** Creation and deletion of categories.
- **Discussion:** Creation and deletion of discussions.
- **Topic** Creation and deletion of topics.
- **Comment:** Users can reply to topics in the comment section using a paginated list.

## Getting Started

### Prerequisites

- **Node.js:** Ensure you have Node.js installed on your machine for Angular development.
- **Angular CLI:** Install Angular CLI globally using `npm install -g @angular/cli`.
- **Django:** Set up a Django backend for the REST API. Follow
  the [Django installation guide](https://docs.djangoproject.com/en/stable/intro/install/) for
  details.
- **Django REST Framework:** Install Django REST framework for building APIs in your Django project
  using `pip install djangorestframework`.
- **SQLite:** SQLite is included with Python, so no additional installation is required.

### Installation

1. Clone the repositories: 
```bash
git clone https://github.com/as1k/kazoverflow-backend.git
git clone https://github.com/nnbzh/web_dev_2023.git
```

2. **Install Angular dependencies:**
```bash
cd web_dev_2023
npm install
```

3. **Install Django dependencies:**
```bash
cd kazoverflow-backend
pip install -r requirements.txt
```

4. **Apply database migrations:**
```bash
cd kazoverflow-backend
python manage.py migrate
```

5. **Start the Angular application:**
```bash
cd web_dev_2023
ng serve
```

6. **Start the Django server:**
```bash
cd kazoverflow-backend
python manage.py runserver
```

7. **Access the application:**
Open your browser and navigate to `http://localhost:4200` to access the Angular app, and `http://localhost:8000` for the Django API.

## Usage

1. **Registration:**
  - Navigate to the registration page.
  - Provide the required information to create a new account.

2. **Authentication:**
  - Log in with the credentials used during registration.

3. **Category:**
  - Create a new category:
    - Access the admin page.
    - Enter the necessary details for the new category.
    - Submit to create the category.

  - Delete a category:
    - Access the admin page.
    - Select the category to be deleted.
    - Confirm the deletion.

4. **Discussion:**
  - Create a new discussion:
    - Access the admin page.
    - Fill in the discussion details.
    - Submit to create the discussion.

  - Delete a discussion:
    - Access the admin page.
    - Select the discussion to be deleted.
    - Confirm the deletion.

5. **Topic:**
  - Create a new topic:
    - Access the topic creation page.
    - Provide the necessary information for the new topic.
    - Submit to create the topic.

  - Delete a topic:
    - Navigate to the topic management section.
    - Select the topic to be deleted.
    - Confirm the deletion.

6. **Comment:**
  - Reply to topics:
    - Navigate to the topic with the comment section.
    - Use the paginated list to view existing comments.
    - Add a new comment to participate in the discussion.

  - Pagination:
    - Navigate through the paginated list to view additional comments.

Note: Ensure proper authorization for actions like category, discussion, and topic deletion based on user roles and permissions.

## Technologies Used

- **Node.js**
- **Angular CLI**
- **HTML5, CSS3, TypeScript, JavaScript**
- **Django**
- **Django REST Framework**
- **SQLite**

# Forum API Documentation

## Auth

### Login

- **Method:** POST
- **URL:** `{{8000}}/api/login/`
- **Request Body:**
    ```json
    {
        "username": "username",
        "password": "password"
    }
    ```
- **Response:** *(No specific details provided)*

### Register

- **Method:** POST
- **URL:** `{{8000}}/api/signup/`
- **Request Body:**
    ```json
    {
        "username": "username",
        "password": "password",
        "email": "email"
    }
    ```
- **Response:** *(No specific details provided)*

## Categories

### All

- **Method:** GET
- **URL:** `{{8000}}/api/categories/`
- **Response:** *(No specific details provided)*

### Detail

- **Method:** GET
- **URL:** `{{8000}}/api/categories/1`
- **Response:** *(No specific details provided)*

### Discussions

- **Method:** GET
- **URL:** `{{8000}}/api/categories/1/discussions`
- **Response:** *(No specific details provided)*

## Discussions

### All

- **Method:** GET
- **URL:** `{{8000}}/api/discussions/`
- **Response:** *(No specific details provided)*

### Detail

- **Method:** GET
- **URL:** `{{8000}}/api/discussions/1`
- **Response:** *(No specific details provided)*

### Topics

- **Method:** GET
- **URL:** `{{8000}}/api/discussions/1/topics`
- **Response:** *(No specific details provided)*

## Topics

### Create

- **Method:** POST
- **URL:** `{{8000}}/api/topics/`
- **Request Body:**
    ```json
    {
        "discussion_id": 1,
        "title": "title",
        "description": "description",
        "author": "author",
        "last_author": "author",
        "replies": 0,
        "date": "Y-m-d",
        "last_date": "Y-m-d",
        "views": 0,
        "unread": 0
    }
    ```
- **Response:** *(No specific details provided)*

### Detail

- **Method:** GET
- **URL:** `{{8000}}/api/topics/1`
- **Response:** *(No specific details provided)*

### Delete

- **Method:** DELETE
- **URL:** `{{8000}}/api/topics/1`
- **Request Body:**
    ```json
    {
        "discussion_id": 1,
        "title": "title",
        "description": "description",
        "author": "author",
        "last_author": "author",
        "replies": 0,
        "date": "Y-m-d",
        "last_date": "Y-m-d",
        ""
    }
    ```
- **Response:** *(No specific details provided)*

## Comments

### Create

- **Method:** POST
- **URL:** `{{8000}}/api/comments/`
- **Request Body:**
    ```json
    {
        "topic_id": 1,
        "author": "Author",
        "content": "Comment description",
        "date": "Y-m-d"
    }
    ```
- **Response:** *(No specific details provided)*

## Acknowledgments

Special thanks to the StackOverflow community for inspiring this project.
Happy coding! 🚀

### About developers

| Name                    |                                           Github                                           |
|-------------------------|:------------------------------------------------------------------------------------------:|
| Balgabay Nurassyl       |                       [nnbzh](https://github.com/nnbzh/ForumProject)                       |
| Nurmukhambet Assylanbek | [asiknurmukhambet](https://github.com/asiknurmukhambet/ForumProject/blob/master/README.md) |
| Sarsenov Yerlan         |                    [yerlansarsenov](https://github.com/yerlansarsenov)                     |
| Saduakhassov Nursat     |                     [WooWooNursat](https://github.com/WooWooNursat)                        |