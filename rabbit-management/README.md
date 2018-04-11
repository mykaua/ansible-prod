# ansible_rabbit_management

It will install rabbitmq-management.

You are able to install rabbit-management using this command:

$ansible-playbook main.yml -t "plugin"

And you can add user using the command:

$ansible-playbook main.yml -e "user_name= password= user_tag=" -t "user_add"

 * user_name - name of user
 * password - password for user
 * user_tag - tag of user

example:

$ansible-playbook main.yml -e "user_name=admin password=admin user_tag=admin" -t "user_add"


Run on special node:

$ansible-playbook main.yml -l test1 -t "plugin"


###enable police
/usr/sbin/rabbitmqctl set_policy ha-all "" '{"ha-mode":"all","ha-sync-mode":"automatic", "ha-promote-on-shutdown":"always"}'
