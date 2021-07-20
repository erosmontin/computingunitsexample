# computingunitsexample

just run 
```
docker-compose -f camrie-linux-bd.yml up
```

and then visit localhost:4002/login to start the app


change the position of the local volume on your machine the '/data/tmp' directory to your favorite directory

## what's going on
there are three main groups of images here:
- brainstem
  - brainstem: get the requests from users and route them to the right basic unit
  - brainstemstate: redis database to keep track of te tasks
- basic unit:
  - camriespinalnode: gets the requests from the brainstem and add a task on the musckestate
  - camriemusleworker: retrieves quesed tasks from musclestate and solve it
  - camriemusclestate: redis database filled with tasks
  - camriespinainpsector: mehr/flower image that shows the tasks scheduled in the musclestate
- gui
  - camrieback: express backend
  - camriefront: angularjs frontend

##APIs example

https://www.getpostman.com/collections/f0f3f0f12ef4685d24a6
