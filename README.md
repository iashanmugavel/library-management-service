# **Library Management Service**

A **Python FastAPI** application that provides APIs for managing a library system. This service allows users to interact with library resources, such as books, authors, and borrowers, through RESTful APIs.

---

## **Features**
- Manage books, authors, and borrowers.
- FastAPI-based implementation for high performance.
- Modular and extensible design for future enhancements.

---

## **Setup Instructions**

Follow these steps to set up the project locally.

### **Prerequisites**
1. **Python**: Ensure Python 3.12.4 is installed. Use [asdf](https://asdf-vm.com/) for managing Python versions.
2. **Pipenv**: Install Pipenv for managing dependencies.

---

### **Step 1: Install Python**

Use `asdf` to install Python 3.12.4:

```bash
asdf install python 3.12.4
asdf local python 3.12.4
```

---

### **Step 2: Install Pipenv**

If Pipenv is not installed, you can install it globally using `pip`:

```bash
pip install pipenv
```

---

### **Step 3: Create a Virtual Environment**

Navigate to the project directory and initialize a virtual environment:

```bash
cd library-management-service
pipenv install
```

This command will:
- Create a `Pipfile` to manage dependencies.
- Set up a virtual environment.

---

### **Step 4: Add Dependencies**

To add new dependencies to the project:

- For a production dependency:
  ```bash
  pipenv install "fastapi[standard]"
  ```

- For a development dependency:
  ```bash
  pipenv install pytest --dev
  ```

These commands will update the `Pipfile` and lock the dependencies in `Pipfile.lock`.

---

### **Step 5: Activate the Virtual Environment**

To activate the virtual environment, run:

```bash
pipenv shell
```

Once activated, you can run the application or tests in an isolated environment.

---

## **Running the Application**

1. Ensure all dependencies are installed:
   ```bash
   pipenv install
   ```

2. Start the FastAPI application:
   ```bash
   uvicorn app.main:app --reload
   ```

3. Access the API documentation:
   - Interactive Swagger UI: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
   - ReDoc: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## **Running Tests**

To run the test suite using `pytest`:

```bash
pytest
```

---

## **Setting Up Linting**

### **Pylint Setup and Usage**

`Pylint` is a linting tool that helps ensure code quality by checking for errors, enforcing coding standards, and offering suggestions for improvements.

#### Step 1: Install Pylint

To install `pylint`, run the following command:

```bash
pipenv install pylint --dev
```

#### Step 2: Generate Pylint Configuration File

You can generate a default `pylint` configuration file by running:

```bash
pylint --generate-rcfile > .pylintrc
```

This will create a `.pylintrc` file in your project, which can be customized for your needs.

#### Step 3: Run Pylint

To lint FastAPI application, run:

```bash
pylint .
```

---

## **Development Notes**

- Use the following command to check for unused dependencies or environment issues:
  ```bash
  pipenv check
  ```

- To update a specific package:
  ```bash
  pipenv update <package_name>
  ```

---

## **Contributing**

We welcome contributions! To contribute:
1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Submit a pull request.

---

## **License**

This project is licensed under the [MIT License](LICENSE).

--- 
