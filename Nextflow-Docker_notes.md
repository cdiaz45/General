# Setting the permissions for docker - ubuntu

You need Docker to work your way through the nextflow training exercises. So a few notes beloew regarding accessibility

## How to deal with Docker permission denied when trying to connect to the Docker daemon socket

Help can be found [here](https://www.digitalocean.com/community/questions/how-to-fix-docker-got-permission-denied-while-trying-to-connect-to-the-docker-daemon-socket).
Very useful [Demo](https://www.youtube.com/watch?v=XfZvKLNXC9M)

Commands that worked for me (assuming you have Docker installed):
```
sudo systemctl status docker
```

You will get denied when you run this
```
docker ps -a
```

So add user to the docker group using the command exactly as it shows here. No need to look for your user ID
```
sudo usermod -aG docker ${USER}
```

Open a new tab and sign into aws again. The following command shoud work
```
docker ps -a
```
