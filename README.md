Role Name
=========

> A finial is an element marking the top or end of some object, often formed to be a decorative feature, or the finishing touch.

Finial is a simple Ansible role that finishes off the provisioning of VMs, completing tasks such as the registration of RHEL machines to Red Hat, and installation of common applications. It was designed as a companion role to [Cornerstone](https://github.com/danhawker), but can be used independently.

Requirements
------------

None

Role Variables
--------------

    # Prefix used when deploying with Cornerstone
    finial_prefix: cornerstone

    # Red Hat Subs
    finial_rhsm_username_org: <add_your_rhsm_username_or_organisation_id>
    finial_rhsm_password_key: <add_your_rhsm_password_or_activation_key>
    finial_rhsm_pool: <add_your_rhsm_poolid>

    # Base Red Hat Repos to Enable
    finial_rhsm_repos:
        - rhel-7-server-rpms
        - rhel-7-server-extras-rpms



Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      vars:
      finial_rhsm_username_org: <username>
      finial_rhsm_password_key: <password>
      finial_rhsm_pool: <pool_id>

      roles:
         role: danhawker.finial

License
-------

MIT

Author Information
------------------

Dan Hawker [Github](https://github.com/danhawker)
