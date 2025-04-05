# sit323-2025-prac5p

This task implements a simple calculator microservice built with Node.js and Express. It supports four basic arithmetic operations: addition, subtraction, multiplication, and division (app was extracted from task 4.2C). The microservice is containerized using Docker, ensuring easy deployment.


Steps Undertaken in Creating Calculator Microservice:
- The steps can be referred to task 4.2c at https://github.com/223257356/sit323-2025-prac4c

Dockerizing the Calculator Microservice:
1. Dockerfile was created in the root folder of this project.
2. Within the Dockerfile, node:16 is used as the base image, /usr/src/app is set as the working directory inside the container, 'npm install' command will run to install all dependencies from the package.json file. Port 3000 is exposed to make the application accessible from the outside and 'npm start' is used to run 'node app.js'.
3. A YAML file, 'docker-compose.yml' is created which configures the containerized environment.
4. The YAML file builds the Docker image from the Dockerfile where it maps Port 3000 on the container  to Port 3000 on the host. It then mounts the current directory into the container for development and testing.
5. To run the application, the task file was cloned to the a new Github repository using git clone.
6. The application was then built and run using docker via the command 'docker-compose up --build'.
7. For pushing Docker Image, a new repo was created within Docker Hub.
8. In the CLI, login to Docker was done using the command 'docker login'.
9. The image was then tagged using command 'docker tag sit323-2025-prac5p-web wongyj/sit323-2025-prac5p-web:latest'.
10. The image was finally pushed using command 'docker push wongyj/sit323-2025-prac5p-web:latest'.
# sit323-2025-prac5p
