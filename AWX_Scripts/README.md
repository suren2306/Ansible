
## This repository contains scripts that helps to automate day to day administrator tasks
 <br />
**Note :**  
[Ping playbook](https://github.com/suren2306/Ansible-Playbooks/blob/master/AWX_Scripts/ping.yml) is used to test the reachablity of all hosts from the control machine. If any host throws python dependency error then you can run the [prerequisite playbook](https://github.com/suren2306/Ansible-Playbooks/blob/master/AWX_Scripts/prerequisite.yml) on that particular host.
 <br />
**Basic commands :**
- To run a playbook `ansible-playbook <playbook-name>`
- To run a playbook and provide sudo password `ansible-playbook <playbook-name> -K`
- To skip certain tags in a playbook `ansible-playbook <playbook-name> --skip-tags <tag_to_be_skipped>`
 <br />

**Table of Contents**
- Change SSH port - This playbook changes the default SSH port from 22 to 2222.
- Disable root login - This playbook disables root login and restarts SSH.
- Sudo access - This playbook prompts for a username and add that user in sudoers file.
- User creation - This playbook creates new user with key based access and pre-defined password. Place the keys under ssh_keys directory. The format should be userName.key.pub
- User deletion - This playbook deletes the user account and remove the users home directory. If you dont want to delete the users home directory then you can add `--skip-tags delete_home` at the end of ansible command.
