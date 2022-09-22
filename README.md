Google GKE Setup
=========

Ansible role to setup a bastion server to connect with a GKE cluster



Example Playbook
----------------

```
- hosts: all
  become: no
  remote_user: "root"

  roles:
    - role: ansible-role-google-setup
      CLUSTER_NAME: "{{ lookup('env', 'CLUSTER_NAME') }}"
      LOCATION: "{{ lookup('env', 'LOCATION') }}"
      PROJECT_ID: "{{ lookup('env', 'PROJECT_ID') }}"

```

Author Information
------------------

- [César vergara](mailto:cvergarae@smu.cl)

