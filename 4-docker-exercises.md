##### Introducing conteinerization
1. Check your `docker version`
2. Check your `docker info`
3. List all possible commands you can do with the docker client.
4. List your currently running containers, check for stopped ones too. It should be empty!
5. Run your first container! Run the official `hello-world` Docker Image. 
6. Read the text that shows up specially the 4 bullet points.
7. List your currently running containers again, check for stopped ones too.
8. Make sure to remove your stopped container.
9. Now start another `hello-world` container using the `--rm` flag. Do you need to remove it after?
10. Is `hello-world` a 'long running' process or a 'short lived' process?

##### Images VS Containers: Running Existing Images as Containers
1. List all the images you have downloaded to your local machine.
2. List all the containers you have running or stopped on your local machine.
3. Open your browser and type localhost:80 in the url. Now try to reach localhost:8080.
4. Run the following two images at the same time using the same terminal:
* nginx (map the port 80:80 from the container)
* httpd (map the port 8080:80  from the container)
5. Test the fact your webservers are up by checking the same urls again. You should get a different page for each.
6. List all the images you have downloaded to your local machine. Are there new images here?
7. Make sure to stop and remove your containers.
8. Cleanup your images to avoid consuming too much space now.

##### Getting inside the Container
1. Start a new ubuntu container in version 16.04 interactively. Inside it, use the command `lsb_release -a` to check its version.
2. Start a new ubuntu container in version 18.04 interactively. Inside it, use the command `lsb_release -a` to check its version.
3. Start a nginx node in non-detached mode. Access the url localhost:80. What do you see in the terminal when you reload the page? Stop the container using `ctrl-c` in the terminal.
4. Now start a nginx container again in detached mode. Attach into it and then print the contents of the file `/usr/share/nginx/html/index.html`. It should match exactly what you see when you access the URL. 
5 (challenge). Same as step 4. but instead of printing the file, modify it and check the URL again.
6. Now start a nginx container again in detached mode. How can you access its logs the same way as in 3.? Notice that you need to be able to see the logs 'flowing', and not only the current state for them on the console. Test it reloading the `localhost` page.
7. Make sure to cleanup by stopping and removing all containers.

##### Using the DockerHub for production ready images
1. Navigate through the [Docker Hub](https://hub.docker.com/) and the [Official Images](https://hub.docker.com/search/?q=&type=image&image_filter=official)
2. Identify two Linux Images: Debian and Ubuntu. 
3. Run an interactive container for each of them and test the curl command on both by using:
   ```apt-get install curl```
   ```curl --version```
   ```curl http://www.concordia.ca/```
4. Suppose you're working on a computer without Python where you can't install any software, but that has docker installed? Run a program that prints `Hello World!` from inside a docker container. What image would you use?
5. Make sure to cleanup by stopping and removing all containers.

##### Creating your own Images and modifying existing Images
1. Write a small python script that only prints `I'm a short lived python script running within a docker container!!!`. Save it as `short-lived.py`
2. Create a new Dockerfile based on the ubuntu linux docker image. This image should always launch your `short-lived.sh` script when started.
3. Build this image and run it to test it.
4. Repeat the same steps, but now use a long running process. You can use a `while(True)` loop in  your python script in order to achieve this.
5. Make sure to cleanup by stopping and removing all containers.
6. Create a new Image based on mysql, making sure that the password is always set to: `12345678`

##### Volumes
1. Write a small python script that prints the contents of a file, the file path/name should be passed as an argument. Save it as file-from-volume-printer.py
2. Create a new Dockerfile based on the ubuntu docker Image. This image should always launch your `file-from-volume-printer.py` script when started. Do not add the file to be printed in the Image.
3. Build this image and run it, binding the external file using the `-v` flag. Pass the location of the file to the script as an argument. Make sure the file gets printed.
4. Make sure to cleanup by stopping and removing all containers.