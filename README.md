<!DOCTYPE html>
<html>
<head>
  <title>ToDo App - Prateek Jadaun</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body { font-family: Arial; padding: 20px; background: #f0f0f0; max-width: 500px; margin: auto; }
    h1 { color: #333; text-align: center; }
    input { padding: 12px; width: 65%; border: 1px solid #ccc; }
    button { padding: 12px; background: #28a745; color: white; border: none; width: 25%; }
    li { background: white; margin: 8px 0; padding: 12px; list-style: none; cursor: pointer; border-radius: 4px; }
  </style>
</head>
<body>
  <h1>My ToDo List</h1>
  <input type="text" id="taskInput" placeholder="Task likho...">
  <button onclick="addTask()">Add</button>
  <ul id="taskList"></ul>

  <script>
    function addTask() {
      let input = document.getElementById("taskInput");
      let task = input.value.trim();
      if(task === "") return;
      let li = document.createElement("li");
      li.innerText = task;
      li.onclick = function() { this.remove(); }
      document.getElementById("taskList").appendChild(li);
      input.value = "";
    }
  </script>
</body>
</html>
