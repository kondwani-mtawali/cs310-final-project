# CS 310: Final Project - Kondwani Mtawali & Aaron Wulff

## Summary
This projects automates the creation of two user accounts for the two developers and an administrator at CraftRoast. The account creations include the following:
- SSH Configuration: Directory and Public Key Assignment
- Sets Up User Home Directories
- Grants Admin User Passwordless Authentication

The `bagisto.yml` playbook deploys the Bagisto e-commerce platform for CraftRoast using Docker. This declarative configuration ensures that Bagisto can be consistently deployed or redeployed on a server with minimal manual intervention.The playbook follows Bagisto’s official Docker-based installation method, making the deployment reliable and easy to maintain.
The `bagisto.yml` playbook performs the following tasks:
- Installs required system packages:
  - Docker
  - Docker Compose
  - Git
- Ensures the Docker service is enabled and running
- Clones the official Bagisto Docker repository into `/opt/bagisto`
- Starts the Bagisto application using Docker Compose

The `grafana.yml` playbook deploys a Grafana monitoring instance for CraftRoast using Docker. Grafana provides visibility into system and application metrics and supports monitoring the e-commerce environment. This playbook ensures Grafana is deployed in a consistent and repeatable manner using a declarative configuration.
The `grafana.yml` playbook performs the following tasks:

- Installs Docker
- Ensures the Docker service is enabled and running
- Deploys the official Grafana Docker container
- Configures the container to restart automatically
- Exposes Grafana on port 3000
- Uses a Docker volume to persist Grafana data

The playbook is idempotent and can be re-run safely.

Because the playbook is idempotent, it can be safely re-run without creating duplicate resources.

## Usage
1. **Clone repository to local machine**
2. Run CMD: **ansible-playbook playbooks/<playbook_in_playbooks>.yml --check** to ensure proper functionality
3. Run CMD: **ansible-playbook playbooks/<playbook_in_playbooks>.yml** to run playbook and apply changes
### For admins.yml:
- Run CMD: **ansible-playbook playbooks/admins.yml --ask-become-pass** to avoid sudo error

### How to Use grafana.yml playbook

Run the playbook using Ansible from the root of the repository:

```bash
ansible-playbook playbooks/grafana.yml
```

After execution, Grafana will be available at:

```
http://<server-ip>:3000
```

Default login credentials:
- Username: `admin`
- Password: `admin`

---
## Resources
- Document used
1. https://docs.ansible.com/projects/ansible/latest/collections/community/general/sudoers_module.html
2. https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/copy_module.html
3. https://docs.ansible.com/projects/ansible/latest/collections/ansible/posix/authorized_key_module.html
4. https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/user_module.html
5. https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/file_module.html
6. https://www.youtube.com/watch?v=P5iKWANifrU
7. https://docs.ansible.com/
8. https://devdocs.bagisto.com/getting-started/installation.html#🐳-docker-installation
9. https://docs.docker.com/
10. https://docs.ansible.com/
11. https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/
12.  https://docs.docker.com/

### *Reports/Reflections Available in Project Directory
