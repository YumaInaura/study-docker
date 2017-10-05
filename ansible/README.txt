docker image build . -t ansible_server

docker run -d -p 30000:22 ansible_server

ansible -i inventory.txt example -m command -a 'ls -la'

