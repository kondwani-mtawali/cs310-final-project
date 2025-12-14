# CS 310: Final Project - Kondwani Mtawali & Aaron Wulff

## Summary
This projects automates the creation of two user accounts for the two developers and an administrator at CraftRoast. The account creations include the following:
- SSH Configuration: Directory and Public Key Assignment
- Sets Up User Home Directories
- Grants Admin User Passwordless Authentication

## Usage
1. **Clone repository to local machine**
2. Run CMD: **ansible-playbook playbooks/<playbook_in_playbooks>.yml --check** to ensure proper functionality
3. Run CMD: **ansible-playbook playbooks/<playbook_in_playbooks>.yml** to run playbook and apply changes
### For admins.yml:
- Run CMD: **ansible-playbook playbooks/admins.yml --ask-become-pass** to avoid sudo error

## Resources
- Document used
1. https://docs.ansible.com/projects/ansible/latest/collections/community/general/sudoers_module.html
2. https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/copy_module.html
3. https://docs.ansible.com/projects/ansible/latest/collections/ansible/posix/authorized_key_module.html
4. https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/user_module.html
5. https://docs.ansible.com/projects/ansible/latest/collections/ansible/builtin/file_module.html
6. https://www.youtube.com/watch?v=P5iKWANifrU

### Reports/Reflections Available in Project Directory
