
# ------------------------------------------------------------------------------
# To run Ubuntu on Docker locally, follow these steps:
# -------------------------------------------------------------------------------
Install Docker on your computer.
Open a terminal or command prompt.
Use the docker pull command to download the latest version of the Ubuntu image from Docker Hub:
Copy code
`$ docker pull ubuntu`
Use the docker run command to start a new container based on the Ubuntu image you just downloaded:
Copy code
`$ docker run -it ubuntu`
This will start a new container and open a command prompt inside the container, where you can run Ubuntu commands.

You can also use the -d flag with the docker run command to start the container in the background, so you can continue using your terminal or command prompt for other tasks:

Copy code
`$ docker run -d ubuntu`
To access the container and run commands inside it, use the docker exec command:

Copy code
`$ docker exec -it modest_kirch bash`
Replace <container-id> with the ID of the container that you want to access. You can use the docker ps command to view a list of all running containers and their IDs.

`Remember to always stop and remove containers when you are finished with them, to avoid using up `valuable resources on your computer. Use the docker stop and docker rm commands to do this:

Copy code
`$ docker stop modest_kirch`
`$ docker rm modest_kirch`
Replace <container-id> with the ID of the container you want to stop and remove.

# To install Git on Ubuntu Docker, follow these steps:

Update the package list on your Ubuntu system by running the apt-get update command:
Copy code
`$ apt-get update`
This will download the latest package information from the Ubuntu package repositories, which will allow you to install the latest versions of software using the apt-get install command.

Install Git using the apt-get install command, like this:
Copy code
`$ apt-get install git`
This will install the Git package and all of its dependencies, which are required for Git to work properly.

Verify that Git was installed successfully by running the git --version command, which will display the version number of Git:
Copy code
$ git --version
`git version 2.25.1`
If you are still having trouble installing Git on Ubuntu Docker, you can try using the aptitude command instead of apt-get. The aptitude command provides a more user-friendly interface for managing packages on Ubuntu systems. To install Git using aptitude, run the following commands:

Copy code
`$ aptitude update`
`$ aptitude install git`
Once Git is installed, you can use it to manage your source code repositories and collaborate with other developers on your projects. For more information on how to use Git, see the Git documentation or the Pro Git book.

# ------------------------------------------------------------------------------
# To edit searxng and build a Docker image, you will need to follow these steps:
# -------------------------------------------------------------------------------

Make sure you have Docker installed on your computer. If you don't have it, you can download it from the Docker website.

Clone the searxng repository from GitHub using the following command:

Copy code
`git clone https://github.com/edcarlos-92/ayosearch.git ayosearch`
`git clone https://github.com/edcarlos-92/ayosearch.git ayosearch`
Once the repository has been cloned, navigate to the searxng directory and edit the files as needed. You can use any text editor or IDE to make the changes.

After you have made the necessary changes, you can build the Docker image by running the following command in the searxng directory:

Copy code
`docker build -t searxng .`
docker build --init /lib/systemd/systemd -t searxng . <image> <command>

This will build the Docker image using the Dockerfile in the current directory. The -t flag allows you to specify a name for the image, in this case "searxng".

Once the image has been built, you can run it using the following command:
Copy code
`docker run -it -p 8888:8888 searxng`
This will start a container based on the searxng image and bind the container's port 8888 to the host's port 8888. You can then access searxng from your web browser at http://localhost:8888.

I hope this helps! Let me know if you have any other questions.


# Setting File
searx\settings.yml

# file permission
`chmod u+x manage`