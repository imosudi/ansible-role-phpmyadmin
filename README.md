Role Name: phpmyadmin
=========

Install phpmyadmin

Note: This role will not manage your apt cache. So manage it by yourself.

Role Variables
--------------

User for database
    phpmyadmin_control_user: phpmyadmin

Password for database
    phpmyadmin_control_password: False

Host which should run the WebGUI
    phpmyadmin_control_server: "{{ inventory_hostname }}"

MySQL server IP
    phpmyadmin_control_server_ip: "localhost"

WebGUI IP
    phpmyadmin_control_client_ip: "localhost"
    
Database:
    phpmyadmin_control_database: phpmyadmin
Example Playbook
----------------

    - hosts: appservers
      vars:
        phpmyadmin_control_password: "mySecret"
        phpmyadmin_control_server_ip: "10.0.3.2"
        phpmyadmin_control_client_ip: "10.0.3.1"
      roles:
        - phpmyadmin
License
-------

CC-BY
