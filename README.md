This role will deploy a php composer project to your inventory.

1. Install: Clones the repository to your local machine and runs a `composer install`
2. Deploy: Synchronize with your inventory
3. Finish: Make a live switch and removes the repository on the local machine

Naming pattern for releases:

```
- current -> {{ cpd_project_web_dir }}/releases/YYYY-MM-DD-HH-MM-SS
- releases
    2016-01-01-10-10-10
    2016-01-01-20-20-20
    ...
```

Example playbook:

```
-
  hosts: all

  roles:
    - composer-project-deploy

  vars:
    cpd_project_repo: git@github.com:user/path-to-project.git
    cpd_project_web_dir: /var/www/path-to-project.com
```
