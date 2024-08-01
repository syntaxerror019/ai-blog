
---
title: "Installing and Using Flask on Ubuntu"
date: 2024-08-01T09:51:34.381719-04:00
draft: false
tags: ["AI", "Technology"]
featured: false
---
# 

This tutorial will guide you through the process of installing Flask, a popular web framework for Python, on an Ubuntu system. We will cover the prerequisites, installation steps, and a basic example of creating a simple Flask application to get you started.

## Prerequisites

Before you begin, ensure that you have the following installed on your Ubuntu system:

- **Python 3**: Flask requires Python 3. You can check if it's installed by running:
  ```bash
  python3 --version
  ```
  If it's not installed, you can install it using:
  ```bash
  sudo apt update
  sudo apt install python3
  ```

- **pip**: This is the package installer for Python. Check if it's installed with:
  ```bash
  pip3 --version
  ```
  If not, install it using:
  ```bash
  sudo apt install python3-pip
  ```

## Step 1: Create a Virtual Environment

It's a good practice to create a virtual environment for your Flask projects to manage dependencies separately. Follow these steps:

1. **Install `venv` module**:
   ```bash
   sudo apt install python3-venv
   ```

2. **Create a new directory for your project**:
   ```bash
   mkdir my_flask_app
   cd my_flask_app
   ```

3. **Create a virtual environment**:
   ```bash
   python3 -m venv venv
   ```

4. **Activate the virtual environment**:
   ```bash
   source venv/bin/activate
   ```

## Step 2: Install Flask

With the virtual environment activated, you can now install Flask using pip:

```bash
pip install Flask
```

To verify that Flask has been installed, you can run:
```bash
pip show Flask
```

## Step 3: Create a Simple Flask Application

Now that Flask is installed, let's create a simple web application:

1. **Create a new file called `app.py`**:
   ```bash
   touch app.py
   ```

2. **Open `app.py` in your text editor and add the following code**:

   ```python
   from flask import Flask

   app = Flask(__name__)

   @app.route('/')
   def hello_world():
       return 'Hello, World!'

   if __name__ == '__main__':
       app.run(debug=True)
   ```

## Step 4: Run Your Flask Application

To run the Flask application, execute the following command in your terminal:

```bash
python app.py
```

You should see output indicating that the server is running, typically on `http://127.0.0.1:5000/`. Open your web browser and navigate to this URL. You should see "Hello, World!" displayed on the page.

## Step 5: Deactivate the Virtual Environment

Once you're done testing your application, you can deactivate the virtual environment by simply running:

```bash
deactivate
```

## Conclusion

You have successfully installed Flask on your Ubuntu system and created a simple web application. You can now explore Flask's extensive capabilities and build more complex applications. Happy coding!