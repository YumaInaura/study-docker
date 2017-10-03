$ ssh-keygen -f ./id_rsa -t rsa -b 4096 -C 'example@com' -N ''

$ docker image build . -t ssh_server

$ docker run -d -p 10000:22 ssh_server

$ ssh root@127.0.0.1 -p 10000 -i id_rsa

