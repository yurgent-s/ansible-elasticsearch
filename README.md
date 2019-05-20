***INFORMATION ABOUT ELASTICSEARCH INSTALLATION***

Original source for Elasticsearch role: https://github.com/elastic/ansible-elasticsearch

Installation was made on CentOS Linux release 7.6.1810 (Core), Elasticsearch version - 6.6.0

Commands to start Elasticsearch playbook down below:

    1. Install Ansible

sudo yum install epel-release -y
    
sudo yum install ansible -y

    2. Install Git to clone this branch
    
sudo yum install git -y

git clone https://github.com/yurgent-s/ansible-elasticsearch.git

cd ansible-elasticsearch

    3. Start playbook
    
ansible-playbook -i inventory playbook.yml --user=username --extra-vars "ansible_become_pass=password"
