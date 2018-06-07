# Tutorial Ansible Sekolahlinux

## Tutorial & Penjelasan Lengkap

* **[https://sekolahlinux.com/mengenal-dan-belajar-ansible-pada-linux/](https://sekolahlinux.com/mengenal-dan-belajar-ansible-pada-linux/)**

## Layout Ansible File
```
|-- inventories
|   `-- production
|       |-- group_vars
|       |   |-- all.yml
|       |   `-- nginx.yml
|       `-- hosts
|-- roles
|   |-- common
|   |   `-- tasks
|   |       `-- main.yml
|   `-- web-server
|       |-- handlers
|       |   `-- main.yml
|       `-- tasks
|           `-- main.yml
|-- templates
|   `-- default.j2
|-- vault_pass.txt
|-- vault_vars.yml
`-- webserver.yml
```

## Run Ansible File
```
ansible-playbook -i inventories/production/hosts --vault-password-file vault_pass.txt webserver.yml

or

ansible-playbook -i inventories/production/hosts --vault-password-file vault_pass.txt webserver.yml
```
