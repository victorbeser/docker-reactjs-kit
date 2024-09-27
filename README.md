# The better way to use Docker & React JS together

| Docker | React JS |
|--------|---------|
| <img src="https://www.docker.com/wp-content/uploads/2023/05/symbol_blue-docker-logo.png" width="200px" height="120px" /> | <img src="https://dabeng.github.io/img/reactjs.png" width="200px" height="180px" /> |

Imagine a modern development environment widely adopted by large companies around the world. 
With Docker and React JS, I offer you an experience that goes beyond the conventional, with all installations pre-configured for you. 
This means more agility, efficiency, and a focus on what truly matters: creating innovative solutions.

## Techs

- **React JS**: A JavaScript Framework for web development.
- **Docker**: Containerization platform.

## Requirements

Before we start you will need this:

- [Node JS 16+](https://www.php.net/downloads)
- [Docker](https://www.docker.com/get-started)
- [Git](https://git-scm.com/downloads)

## How-to

1. Let's start our React JS project:

   ```bash
   npx create-react-app your-project-name

2. Get this repo as a clone into your system:

   ```bash
   git clone https://github.com/victorbeser/docker-reactjs-kit.git

3. Copy and paste all the files of 'docker-laravel-kit' folder to 'your-project-name' project React JS folder;
   
   ```bash
   It should be like this:
   /your-project-name/
     - (dot)docker
     - .dockerignore
     - docker-compose.yml
     - Dockerfile

4. Rename the (dot)docker folder to .docker and the (dot)dockerignore to .dockerignore;
5. Now we need to change the 'docker-compose.yml' file to work correctly:
   
   ```bash
   docker-compose.yml
   your-project-name: # Change here the 'your-project-name'
    image: your-project-name:latest  # Change here the 'your-project-name'


6. Open some terminal/cmd in your project's folder and type the following command to initiate the building of your container:
   
   ```bash
   docker-compose build

7. Now use the following command to start your container:
   
   ```bash
   docker-compose up -d

8. Okay then, we need to install our packages into the container, use the following command to access the bash of your container:
   
   ```bash
   docker-compose exec laravel bash # Note: You can check the name of the "service" using the command 'docker-compose ps'


9. This isn't necessary exactly, we have this in Dockerfile but use this command just to be sure!
   
   ```bash
   npm install 
 
Now you should be able to access your project and see the React's home page without any problems in http://localhost:3000/

![image](https://github.com/user-attachments/assets/ec2d62f8-e4cd-4db4-a4ac-397931aab994)



Note: You can change the port in 'docker-compose.yml':

   ```bash
   docker-compose.yml
   ports:
      - "3000:80" # Change here the 8084 port
  ```

Now that you got your Front-End web application working very well try creating your Back-End web application with Laravel & Docker <a href="https://github.com/victorbeser/docker-laravel">clicking here</a>!
