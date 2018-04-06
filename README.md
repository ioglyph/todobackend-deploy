Deploy logic using Ansible for sample todobackend application.

Reminder, this uses Ansible which runs best on Python 2.7. Especially for the library modules included herein. From an active pipenv shell, it is better to do the following to run playbooks:

```
$(pipenv --venv)/bin/ansible-playbook site.yml --ask-vault-pass -e '{"ecs_tasks": ["migrate", "collectstatic"], "stack_config": "true", "debug": "true"}' -i inventory
```
