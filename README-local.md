# Templatee of an ansible pleybook

## To test it from local machine use vagrant%

Some basic commands to proceed:
```shell
vagrant up

vagrant halt
vagrant destroy
```

rsync make you dirs synchronize (deletion too). You can cpecify it in vars.yml. 

To test connection to vagrant try to use: 
```shell
vagrant ssh

ssh vagrant@<ip-addr> -p <port> -i {your/pub/key/path.pem} -o PubkeyAcceptedKeyTypes=ssh-rsa #!!!if you are using rsa. Else recommended to use OPENSSH key type!!! Else it wont try rsa and fails
```

Ansible command to run playbook:
```shell
ansible-playbook -i ansible/inventories/local/hosts.yml playbook.yml
```
