# Techy-jaunt Backend Project

## Overview

This project provides a set of APIs to manage user authentication and registration and verification. It supports user management functionalities such as registration and login.

---

## Server Link

**Base URL:** [https://techyjaunt-project.onrender.com](https://techyjaunt-project.onrender.com)

---


## api endpoints

### 1. Register User

-   **Method:** `POST`
-   **Endpoint:** `{server}/register`
-   **Purpose:** Allows new users to register their details in the database.
-   **Request Body Example:**
    ```json
    {
        "name": "John",
        "email": "johndoe@example.com",
        "password": "securepassword"
    }
    ```

### 2. Login in user

-   **Method:** `POST`
-   **Endpoint:** `{server}/login`
-   **Purpose:** Allows existing users to log in using their email address and password.
-   **Request Body Example:**
    ```json
    {
        "email": "johndoe@example.com",
        "password": "sample"
    }
    ```

### 3. Get user data

-   **Method:** `GET`
-   **Endpoint:** `{server}/user`
-   **Purpose:** Fetches the data of the logged in user.
-   **Note:** Make sure to include token in your headers when sending request. This token expires after 1h.
-   **Request Body Example:**
    ```txt
      headers: {
        'Authorization': `Bearer ${token}`
      }
    ```

## User Object Structure

The user object returned by the API contains the following fields:

1. \_id - Unique identifier for the user.
2. name - The user's name.
3. email - The user's email address.

**Note:** Ignore user \_id as this will be given to the user once registered on the database.