# Build up Docker LEMP stack by vagrant-up command

If execute **vagrant up** command, launch server and build environment by Ansible.
Letest version LEMP stack are installed at building up.
current example:

- Ansible v2.16.7
- Docker v26.1.4
- Docker Compose v2.27.1
- PHP v8.3.8
- Nginx v1.27.0
- MariaDB v11.4.2

## Environment

**vagrant up** command can be enabled.

- Vagrant
- VirtualBox

## Launch

Execute command in cosole.

```bash
vagrant up
```

## Sample script

Sample PHP scripts are available for web browser.

- index.php
- index2.php

```bash
http://192.168.33.10/
http://192.168.33.10/index2.php
```

## License

[MIT](./LICENSE)
