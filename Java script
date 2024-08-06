function addTask() {
  const taskInput = document.getElementById('taskInput');
  const taskList = document.getElementById('taskList');

  if (taskInput.value.trim() !== '') {
      const listItem = document.createElement('li');
      listItem.textContent = taskInput.value;

      const deleteButton = document.createElement('button');
      deleteButton.textContent = 'Delete';
      deleteButton.onclick = function () {
          listItem.classList.add('fade-out');
          setTimeout(() => taskList.removeChild(listItem), 300);
      };

      const updateButton = document.createElement('button');
      updateButton.textContent = 'Update';
      updateButton.onclick = function () {
          const updatedTask = prompt('Update task:', listItem.firstChild.textContent);
          if (updatedTask !== null && updatedTask.trim() !== '') {
              listItem.firstChild.textContent = updatedTask;
          }
      };

      listItem.appendChild(updateButton);
      listItem.appendChild(deleteButton);
      taskList.appendChild(listItem);

      taskInput.value = '';
      taskInput.focus();
  }
}
