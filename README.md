***INFORMATION ABOUT ELASTICSEARCH INSTALLATION***

Original source for Elasticsearch role: https://github.com/elastic/ansible-elasticsearch

Installation was made on CentOS Linux release 7.6.1810 (Core), Elasticsearch version - 6.6.0

Commands to start Elasticsearch playbook down below:

    1. Install Ansible

sudo yum install epel-release -y
    
sudo yum install ansible -y

    2. Cloning repo with Elasticsearch playbook
    
git clone --branch ansible-elasticsearch https://git.epam.com/Aleksei_Kioller/friends_day_19

    3. Also execute following commands

mkdir -p roles

ansible-galaxy install elastic.elasticsearch,6.6.0 -p roles 

ansible-playbook -i inventory playbook.yml --user=username --extra-vars "ansible_become_pass=password"

    4. To make Elasticsearch be accessable from outside VM parse following commands in /etc/elasticsearch/node1/elasticsearch.yml : 
    
network.bind_host: 0.0.0.0

transport.host: localhost

transport.tcp.port: 9300
