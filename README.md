
# Snake-Ansible

Ansible playbook to install the Snake-Server. See the Snake-Server source code here: https://github.com/ivan1993spb/snake-server

## Presettings

1. Check if you have Python and pip
2. Clone this repository
3. Initialize virtual environment and install dependencies:
    ```bash
    python3 -m venv .venv
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

## Update

```
ansible-playbook -i inventories update.yml
```

## Uninstall

```
ansible-playbook -i inventories uninstall.yml
```

## License

See [LICENSE](LICENSE).
