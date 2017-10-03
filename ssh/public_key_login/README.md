$ docker build . -t ssh_server

$ docker run -d -p 10000:22 ssh_server

$ docker exec <CONTAINER_ID> cat /root/.ssh/id_rsa > ~/.ssh/id_rsa_docker_ssh

$ ssh root@<CONTAINER_IP_ADDRESS> -p 10000 -i ~/.ssh/id_rsa_docker_ssh



