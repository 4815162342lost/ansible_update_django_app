# ansible_update_django_app
This is Ansible playbook for application upgrade

This is simple playbook for upgrade django_application in virtual python env. Steps:
1) Download python-package (tar.gz)
2) Copy package to servers
3) Stop application
4) Create backup if necessary
5) Update package via pip
6) Make manage.py executable
7) Make migration
8) Make collectstatic
9) Start application
10) Remove python-package from server

Run example:
ansible-playbook -i ./tat_prod/inventory -e "version=21.08.1.1 make_dump=True" ./install_app.yaml
