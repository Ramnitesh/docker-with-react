# Docker commands:
1. check docker version in your local machine
```bash
PS C:\any-where>docker --version
```

2. To pull hello world image from hub.docker.com
```bash
PS C:\any-where>docker pull hello-world
```

3. To check all installed or active images
```bash
PS C:\any-where>docker images
```

4. To build a container for the hello-world image.
```bash
PS C:\any-where>docker run hello-world
```

5. To list all the containers
```bash
PS C:\any-where>docker ps -a
```

6. To list the active containers
```bash
PS C:\any-where>docker ps
```

7. To remove container
```bash
PS C:\any-where>docker rm <ContainerID> 
```

8. To remove image. i stands for image
```bash
PS C:\any-where>docker rmi <ImageID or Repo Name>
``` 

9. It will automatically create image Ubuntu and will create a container for it and also will sleep it after 10 secs
```bash
PS C:\any-where>docker run -d sample-web-app sleep 10
```

10. If two images are having same name it will remove latest version among.
```bash
PS C:\any-where>docker rmi sample-web-app:latest
```

11. it will remove image forcefully
```bash
PS C:\any-where>docker rmi <imageId or Name> -f 
```

12. create image
```bash
PS C:\your-project>docker build -t sample-web-app .
```

13. create container
```bash 
PS C:\your-project>docker run --name sample-web-app-container -p 9000:80 sample-web-app:1.0.0
```

14. Start the container
```bash
PS C:\any-where>docker start [containerid]
```

15. Get all ids of container and images
```bash 
PS C:\any-where>$(docker images -q) -- for images
PS C:\any-where>$(docker ps -a -q) -- for conatiner

PS C:\your-project>dcoker rmi $(docker images -q)
```

16. go inside the docker container
```bash 
PS C:\any-where>docker exec -it [containerid] bash
```

17. use cd command to go inside the dir
```bash
'#' cd usr
```

18. check current path
```bash
'#' pwd
```

19. See content of the file
```bash
'#' cat index.html
```

20. add -d to remove all console while creating container
```bash
C:\Learning>docker run -d -v C:\dockerbackup:/usr/share/nginx/dockerfiles --name sample-web-app-container-backup -p 9000:80 sample-web-app:1.0.0
02420184acbf16c77e31e5064f062a1dd2412beac877f27825614bc701b3cf0a
C:\Learning>
```

21. Add volume
```bash
docker run -d -v C:\dockerbackup:/usr/share/nginx/dockerfiles --name sample-web-app-container -p 9000:80 sample-web-app:1.0.0
```
