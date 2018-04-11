# ansible


Ansible playbooks for installing or checking some services.

Your local PC should have ansible 2.2 <

Directories:
  1. backup_script - installing mysql backup script to sandboxes
  2. checkk_disk_space_env - check disk space on servers
  3. docker_service_configs - config files for docker
  4. docker_swarm_production_configuration - install and configure docker swarm on serves
  5. docker-prune - removing stopped containers from servers
  6. docker-swarm-vagrant - start docker swarm with Vagrant
  7. logrotate - configuration logrotate for dockers
  8. rabbit-management - install rabbitmq-management and add users
  9. rabbitmq-queues - check rabbitmq queues on rabbitmq servers
  10. rvm - install rvm and ruby on servers


  How to use:

   1. add user to ansible.cfg file:
          remote_user = example_user

   2. add sudo password to inventory file:
          ansible_sudo_pass=123456677

   3. if needs, please change path to ssh key in inventory file:
          ansible_ssh_private_key_file=~/.ssh/id_rsa


  Start ansible playbook:
   1. Just run playbook:
          ansible-playbook main.yml

   2. Run playbook with special tags:
          ansible-playbook main.yml --tags "user_example"

   3. Run playbook with special groups(groups of hosts):
          ansible-playbook main.ymk -l nodes

More information about Ansible, it can be checked in  Ansible-Cheat-Sheet_Wall-Skills2.pdf  
