# Docker Assignment

5th semester docker assignment for the course Operating Systems(CS51) <br>
Questions repository: https://github.com/rathneesh/uvce-assignment/blob/master/assignment.md <br>
Assignment 4 Reference repository: https://github.com/rathneesh/uvce-assignment <br>

## Team members
- [Sreya Salil](https://github.com/SreyaSalil) (1MS18CS124)
- Priyanka S (1MS18CS098)

## How to run this project
- <b>Step 1:</b> Clone this repository <br>
   ``` 
   git clone https://github.com/SreyaSalil/DockerAssignment
   ```

- <b>Step 2:</b> `cd` into the directory<br>
  ```
  cd DockerAssignment
  ```
- <b>Step 3:</b> Run the project
  ```
  docker-compose up --build
  ```
- <b>Step 4:</b> Open up the browser and paste the below url
  ```
  http://localhost:8000/
  ```
  The browser should display ```Hello World ! I am back with db running .!``` message. The app is up and running inside a docker container using docker-compose.

- <b>Step 5:</b> Verify DB is up and running and tables are created

  Use any of the database clients like MySQL workbench or SQLDeveloper. Make sure you have the driver installed for the MySQL db     running on the client you are using.

  Connect to MySQL database using the properties specified in ```docker-compose.yml``` file with host as ```localhost```.
  
- <b>Step 6: </b> Run simple commands like ```show tables``` or ```desc <<tablename>>``` to make sure table is created with exact fields specified in the Flask models. 

- <b>Step 7: </b> Run ```docker-compose down``` to stop containers and remove containers, networks, volumes, and images created
## Note:

1. Don't use the ```MYSQL_ROOT_PASSWORD``` but the password for the db you created, i.e ```MYSQL_PASSWORD```

2. The port to be used is ```32000``` which is the port on which app is running on localhost. Don't use ```3306``` as port to connect from the client as it's the port where container is running.

3. Since these files were commited from a Windows machine, take care to change the line endings of ```docker-entrypoint.sh``` from ```CR LF``` to ```LF```
   
