# Setup hadoop with Ansible

## Install Ansible

```
python -m venv ~/.cache/venvs/ansible
source ~/.cache/venvs/ansible/bin/activate
pip install ansible
```

## Run playbook

```
source ~/.cache/venvs/ansible/bin/activate
cd <where-ever-it-was-unpacked>

# on first run set hdfs_format to true to format hdfs
ansible-playbook -i inventory.yml hadoop.yml -K --extra-vars "hdfs_format=true"

# on all other runs set it to false to not format hdfs
ansible-playbook -i inventory.yml hadoop.yml -K --extra-vars "hdfs_format=false"
```
