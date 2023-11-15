# Testing
## 1. Check that passing a given input into our tests returns the expected output
To ensure that our tests validate the expected output for a given input, we use the equal function from our test helpers. This function compares the expected output with the actual output and logs the result.
```javaScript
// Test for adding a task
test('01 Submitting a new task adds it to the list', async () => {
    const inputField = await waitForElement('.addTaskField');
    const taskList = document.querySelector('#listToDo');
    inputField.value = 'Task Create Test';
    // ... code to trigger task addition ...

    const addedTask = taskList.lastElementChild;
    const taskText = addedTask.querySelector('.taskText').textContent;

    equal(taskText.trim(), 'Task Create Test', 'Task text should match input');
});
```

## 2. Write tests to mimic the behaviour of a user performing different actions
To simulate user behavior, we can programmatically trigger UI events like clicks or keypresses, and then check if the application responds correctly.
```javaScript
// Test for clearing a task
test('02 Clearing task text removes it from the list', async () => {
    const inputField = await waitForElement('.addTaskField');
    const addTaskButton = await waitForElement('.addTaskButton');
    // ... setup ...

    // Simulate user clearing the task text and pressing Enter
    const taskText = addedTask.querySelector('.taskText');
    taskText.value = '';
    taskText.dispatchEvent(new Event('input'));
    taskText.dispatchEvent(new KeyboardEvent('keypress', { key: 'Enter' }));

    equal(taskList.childElementCount, 0, 'Task list should be empty after clearing');
});
```
# JS
## 1. Write testable, modular functions
Modular functions are self-contained and perform a single task. This makes them easier to test and maintain.
```javaScript
// Function to add a task
function addTask(taskText) {
    const taskList = document.querySelector('#listToDo');
    const newTask = document.createElement('li');
    newTask.textContent = taskText;
    taskList.appendChild(newTask);
}

// Usage in the app
addTaskButton.addEventListener('click', () => {
    const taskText = inputField.value;
    addTask(taskText);
});
```
## 2. Write functions that add, remove or modify DOM nodes
Functions that manipulate the DOM are essential for interactive web applications.
```javaScript
// Function to remove a task
function removeTask(taskElement) {
    taskElement.remove();
}

// Usage in the app
taskList.addEventListener('click', (event) => {
    if (event.target.matches('.removeTaskButton')) {
        removeTask(event.target.parentElement);
    }
});
```
## 3. Apply event listeners to HTML form elements
Event listeners allow us to respond to user actions like clicks, inputs, or form submissions.
```javaScript
inputField.addEventListener('input', (event) => {
    if (event.target.value.trim() === '') {
        disableAddTaskButton();
    } else {
        enableAddTaskButton();
    }
});
```
## 4. Use scope to control what variables are accessible inside functions and blocks
Using scopes properly ensures that variables are only accessible where they're needed, reducing the risk of accidental modifications.
```javaScript
function updateTaskList() {
    const taskList = document.querySelector('#listToDo');
    // taskList is only accessible within this function
    // ... code to update task list ...
}
```
# Design 
## 1. Use CSS grid to create complex layouts
CSS grid is a powerful tool for creating complex, two-dimensional layouts.
```javaScript
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 10px;
}

.item {
    background-color: lightblue;
    padding: 20px;
    text-align: center;
}
```
## 2. Use CSS grid to make layouts that adapt to the viewport size
CSS grid can be combined with media queries to create responsive designs that adapt to different screen sizes.
```javaScript
.container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    grid-gap: 10px;
}

@media screen and (max-width: 600px) {
    .container {
        grid-template-columns: 1fr;
    }
}
```
This approach allows your application to have a responsive design, ensuring a good user experience across various devices and screen sizes.
