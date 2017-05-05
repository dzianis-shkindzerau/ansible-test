# List of useful commands


## Ad-Hoc commands
[CLI Patterns](http://docs.ansible.com/ansible/intro_patterns.html)
```bash
$ ansible demo -m ping
$ ansible all -m ping
#
$ ansible all -a "/bin/echo hello"
$ ansible all -a "/bin/echo hello" -f 3
#
$ ansible all -m shell -a 'echo $TERM'
#
$ ansible all -m copy -a "src=/etc/hosts dest=/tmp/hosts"
# 
# gathering facts
$ ansible all -m setup

```


## Use Playbooks
```bash
$ ansible-playbook playbooks/dev.yml
```

## Use Galaxy
```bash
$ ansible-galaxy install git+git@github.com:JohnPreston/riakcs-cluster.git,master
$ ansible-galaxy list/search etc.
```


## Step by step guide
1. init role [as described here](http://docs.ansible.com/ansible/galaxy.html#create-roles)
```bash
$ ansible-galaxy init role_name
```
2. add tasks to a role
3. add role to a playbook
4. commit changes

