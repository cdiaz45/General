# Working with docker - ubuntu

You need Docker to be working to work your way through the nextflow training exercises. So a few notes beloew regarding accessibility

## How to deal with Docker permission denied when trying to connect to the Docker daemon socket

Help can be found [here] (https://www.digitalocean.com/community/questions/how-to-fix-docker-got-permission-denied-while-trying-to-connect-to-the-docker-daemon-socket).
Very useful [Demo] (https://www.youtube.com/watch?v=XfZvKLNXC9M)

Commands that worked for me (assuming you have Docker installed):
```
sudo systemctl status docker
```

You will get denied when you run this
```
docker ps -a
```

So add user to the docker group
```
sudo usermod -aG docker ${USER}
```

I use a key to get into aws so, I needed to open a new tab and sign into aws, then test this command. It shoud work
```
docker ps -a
```
