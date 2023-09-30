# todo-api
ToDO API using Spring Boot


# use chrome console to create a simple task
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