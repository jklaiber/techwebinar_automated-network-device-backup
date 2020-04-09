# MyLearning Tech Webinar Automated Network Device Backup
Here you can find all the material which was used for the tech webinar.  
  
If you want to know more about these topics you are welcome to visit our [website](https://mylearning.ch) or contact us directly.  
  
There is also a [blog](https://mylearning.ch/blog/676) post (in german) on the same topic.

## Ansible
When you want to try out the Ansible Playbooks don't forget to edit the backup paths, inventory files and add a Ansible-Vault file.

## Infrastructure
When you want to build your own test environment, you can find more information below.

### AWX
To start a local Ansible AWX instance you can simply execute the command below:
```bash
docker-compose up -d
```

### NetBox
To start a local NetBox instance you can find more information [here](https://github.com/netbox-community/netbox-docker), or you can use the commands below (simply past it in your terminal):
```bash
git clone -b release https://github.com/netbox-community/netbox-docker.git
cd netbox-docker
tee netbox-docker.override.yml <<EOF
version: '3.4'
services:
  nginx:
    ports:
      - 8000:8080
EOF
docker-compose pull
docker-compose up
```