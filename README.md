This repository joins two git repositories as submodules and with the help of docker-compose.yml, it lets us run them together.
- upload-file-angular is an Angular App with Material and FlexLayout
- upload-file-netcore is an N-Tier ASP.NET Core WebApi with .NET 5, Mapster and Minio Client
- For storing files, Minio is preferred as it uses filesystem and in this case an unconnected docker volume

***Prerequisites***
- [Docker Desktop](https://www.docker.com/products/docker-desktop)

***How to run this app***

Clone this repository with recursively adding the submodules by executing the following command:

 
     git clone --recursive https://github.com/mburakeker/upload-file-compose.git

change directory to upload-file-compose:

     cd upload-file-compose

After installing and starting the docker desktop, change directory to upload-file-compose, open the terminal and execute the following command:


     docker-compose up -d --build

Wait for it to build and boot. 
Then check out the [Angular App](http://localhost:80)

Once you are finished, you can stop the containers and remove the volumes it created by entering the following command in the same directory:

     docker-compose down -v
