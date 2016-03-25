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
