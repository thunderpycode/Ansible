Passwordless Authentication:
1. Generate Public and  private key --> ssh-keygen
2. copy public key and paste to remote server's /.ssh/authorized_keys
3. go to remote server.
4. vi /etc/ssh/sshd_config, ANd add below Configurations:
            PermitRootLogin yes
            PubkeyAuthentication yes
            PasswordAuthentication no
            AuthorizedKeysFile      .ssh/authorized_keys .ssh/authorized_keys2

--------------------------------------------------------------------------------------- 
Some Fundamentals:

1. Handlers: In Ansible, handlers are special tasks that are only executed when triggered by the notify directive, after a certain set of conditions are fulfilled. Handlers are typically used to start, restart, reload, and stop services on target nodes only when there is a change in the state of the task, and not when no change is made. 



---------------------------------------------------------------------------------------- 
Commands
1. To run playbook for this project  : ansible-playbook playbook.yml -i Inventory/hosts