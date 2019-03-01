
# Snake-Ansible

Ansible playbook to install Snake-Server. See Snake-Server source code here: https://github.com/ivan1993spb/snake-server

## Presettings

1. Check whether you have python 2.7 and pip
2. Clone the repository
3. Initialize virtual environment and install dependencies:
    ```bash
    virtualenv -p python2 .venv
    source .venv/bin/activate
    pip install -r requirements.txt
    ```
4. Create `inventories` file:
    ```
    [all]
    host1
    host2
    hostN
    ```
5. Setup variables in `group_vars/all.yml`:
    ```bash
    cp group_vars/all.yml.sample group_vars/all.yml
    ```

## Install

```
ansible-playbook -i inventories install.yml
```

Use flags `-K`, `-k`, `-u` to control access.

## Uninstall

```
ansible-playbook -i inventories uninstall.yml
```

## License

See [LICENSE](LICENSE).
