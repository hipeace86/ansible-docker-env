FROM ubuntu:16.04
MAINTAINER hipeace86 <hipeace86@gmail.com>
RUN apt-get -y update && \
    apt-get install -y software-properties-common && \
    apt-add-repository ppa:ansible/ansible -y && \
    apt-get -y update && \
    apt-get install ansible -y && \
    apt-get install net-tools vim ssh -y && \    
    systemctl enable ssh && \
    ssh-keygen -t rsa -f ~/.ssh/id_rsa -P "" && \
    rm -rf /var/lib/apt/lists/* && \
    echo 'ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAzyCyTNfALGFeWoo6psgHzGptW4Cr2/vwUevWjgHaB0vC+/S4OU+IaLU6x2/3r60igz60FWwkZHZq/ZotjWXhMAdIeval77MIsil20N0EaQOueKPLUgkpMBKLDJuLXrfznyjub1K8g8cARfw5yXYhHhExx1ltSrM5N4TZTGGTtynaph2NLPnHvwMRvuJXEyWZJ1hhOGWnXLY0RTA48Bzu+Kw3UJwC97g+G5pqIceHlUbpc3Rw2h4sMT4S/+NQiNPndPXduX2sE8Fyc9D68os12uk95osvgOBBzlQBD2aFNKQ2op3MO0cWwqxXRCFpF/G/+kjJ+vkWdtCWv5nJsC1wzQ== root@cenos.master' >/root/.ssh/authorized_keys && \
    chmod 600 /root/.ssh/authorized_keys
