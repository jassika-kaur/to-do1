<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TO-DO</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>To-Do List</title>
        <style>
            body {
                font-family: Arial, sans-serif;
                background-color: blueviolet;
                display: flex;
                justify-content: center;
                align-items: center;
                height: 100vh;
                margin: 0;
            }
    
            .container {
                background: white;
                padding: 20px;
                border-radius: 8px;
                box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
                width: 300px;
                text-align: center;
            }
    
            h2 {
                margin-bottom: 10px;
            }
    
            input {
                width: 70%;
                padding: 8px;
                border: 1px solid #ccc;
                border-radius: 4px;
            }
    
            button {
                padding: 8px 10px;
                background: #28a745;
                color: white;
                border: none;
                cursor: pointer;
                border-radius: 4px;
            }
    
            ul {
                list-style: none;
                padding: 0;
            }
    
            li {
                background: #f9f9f9;
                margin: 5px 0;
                padding: 8px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                border-radius: 4px;
            }
    
            .delete-btn {
                background: red;
                color: white;
                border: none;
                padding: 5px;
                cursor: pointer;
                border-radius: 4px;
            }
        </style>
    </head>
    <body>
    
    <div class="container">
        <h2>To-Do List</h2>
        <input type="text" id="taskInput" placeholder="Add a new task">
        <button onclick="addTask()">Add</button>
        <ul id="taskList"></ul>
    </div>
    
    <script>
        function addTask() {
            let taskInput = document.getElementById("taskInput");
            let taskText = taskInput.value.trim();
    
            if (taskText === "") return; // Prevent empty tasks
    
            let li = document.createElement("li");
            li.innerHTML = `${taskText} <button class="delete-btn" onclick="removeTask(this)">X</button>`;
            
            document.getElementById("taskList").appendChild(li);
            taskInput.value = ""; // Clear input field
        }
    
        function removeTask(button) {
            button.parentElement.remove();
        }
    </script>
    
    </body>
    </html>
    
    
</body>
</html>
