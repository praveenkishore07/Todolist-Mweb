# Todolist-Mweb

# Ex03 To-Do List using JavaScript
## Date: 20/05/2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
### HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Todo List</title>

    <!-- CSS File -->
    <link rel="stylesheet" href="todo.css" />
</head>
<body>

    <div class="container">
        <h1>Todo List</h1>

        <div class="todo-input">
            <input type="text" id="taskInput" placeholder="Enter ur task..." />
            <button id="addBtn">Add</button>
        </div>

        <ul id="taskList"></ul>
    </div>

    <div class="footer">
        <footer>
        <p>Crafted by A PRAVEEN KISHORE | Roll: 212225220074</p>
        </footer>
    </div>

    <!-- JS File -->
    <script src="todo.js"></script>
</body>
</html>
```
### CSS 
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}

body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(135deg, #4facfe, #00f2fe);
}

.container {
    width: 400px;
    background: white;
    padding: 25px;
    border-radius: 12px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}

h1 {
    text-align: center;
    margin-bottom: 20px;
    color: #4227dc;
}

.todo-input {
    display: flex;
    gap: 10px;
}

.todo-input input {
    flex: 1;
    padding: 10px;
    border: 2px solid #ddd;
    border-radius: 6px;
    outline: none;
    font-size: 16px;
}

.todo-input button {
    padding: 10px 18px;
    border: none;
    background: #007bff;
    color: white;
    border-radius: 6px;
    cursor: pointer;
    transition: 0.3s;
}

.todo-input button:hover {
    background: #133d6a;
}

ul {
    list-style: none;
    margin-top: 20px;
}

li {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #f4f4f4;
    padding: 10px;
    border-radius: 6px;
    margin-bottom: 10px;
}

li.completed span {
    text-decoration: line-through;
    color: gray;
}

.task-buttons button {
    margin-left: 5px;
    padding: 5px 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.complete-btn {
    background: #28a745;
    color: white;
}

.delete-btn {
    background: #dc3545;
    color: white;
}

.footer {
    position: fixed;
    bottom: 15px;
    width: 100%;
    text-align: center;
    color: white;
    font-size: 14px;
    font-weight: bold;
    letter-spacing: 1px;
    background-color: #133d6a;
}
```
### JS
```
const taskInput = document.getElementById("taskInput");
const addBtn = document.getElementById("addBtn");
const taskList = document.getElementById("taskList");

addBtn.addEventListener("click", addTask);

function addTask() {
    const taskText = taskInput.value.trim();

    if (taskText === "") {
        alert("Please enter a task!");
        return;
    }

    // Create list item
    const li = document.createElement("li");

    // Task text
    const span = document.createElement("span");
    span.textContent = taskText;

    // Button container
    const buttonDiv = document.createElement("div");
    buttonDiv.classList.add("task-buttons");

    // Complete button
    const completeBtn = document.createElement("button");
    completeBtn.textContent = "Done";
    completeBtn.classList.add("complete-btn");

    completeBtn.addEventListener("click", () => {
        li.classList.toggle("completed");
    });

    // Delete button
    const deleteBtn = document.createElement("button");
    deleteBtn.textContent = "Delete";
    deleteBtn.classList.add("delete-btn");

    deleteBtn.addEventListener("click", () => {
        li.remove();
    });

    // Append buttons
    buttonDiv.appendChild(completeBtn);
    buttonDiv.appendChild(deleteBtn);

    // Append everything
    li.appendChild(span);
    li.appendChild(buttonDiv);

    taskList.appendChild(li);

    // Clear input
    taskInput.value = "";
}
```

## OUTPUT
<img width="767" height="962" alt="1" src="https://github.com/user-attachments/assets/8c23b412-968f-455f-807f-8af228e7d112" />

<img width="766" height="962" alt="Screenshot 2026-05-20 104136" src="https://github.com/user-attachments/assets/cf8e31ff-8534-4415-bd6c-83cfde0846dc" />


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
