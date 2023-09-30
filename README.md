## Setup
- install [OpenJDK17](https://builds.openlogic.com/downloadJDK/openlogic-openjdk/17.0.8+7/openlogic-openjdk-17.0.8+7-windows-x64.msi)
- set vscode preferences for java home path: (search in vscode settings for JDK)
    ```
    "java.jdt.ls.java.home": "C:\\Program Files\\OpenLogic\\jdk-17.0.8.7-hotspot"
    ```
- open the file `src\main\java\com\sacavix\todoapp\controller\TaskController.java` then run or debug it
- to change default port, edit the file `src\main\resources\application.yml`

## todo-api
Simple ToDO API using Spring Boot with H2 in memory database


## use chrome console to create a simple task
```
fetch('tasks', {
  method: 'POST',
  body: JSON.stringify({
    title: 'foo',
    description: 'bar'
  }),
  headers: {
    'Content-type': 'application/json; charset=UTF-8'
  }
})
.then(res => res.json())
.then(console.log)
```

## Endpoints

- GET `/tasks`: list all tasks
- POST `/tasks`: create a task
- GET `/tasks/status/{status}`: get all tasks by status
- PATCH `/tasks/mark_as_finished/{id}`: mark a task as finished
- DELETE `/tasks/{id}`: delete a task by id 