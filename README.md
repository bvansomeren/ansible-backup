bvansomeren.backup
==================

Ensures rsync is installed, creates a backup user and installs a given public key in the authorized files.

Requirements
------------

None

Role Variables
--------------

These are the required variables. No defaults are provided.

	backup_username

The useraccount that the backupserver should log into. for example 'backups'

	backup_pubkey

The String value of the public key that needs to be added to the `authorized_keys` for the backup user. For example: "{{ lookup('file', '{{ variable_with_filepath }}') }}"

Dependencies
------------

Goes together with `bvansomeren.backup-server` but does not depend on it.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: bvansomeren.backup, backup_username: "test_example", backup_pubkey: "{{ lookup('file', '~/.ssh/id_rsa.pub') }}" }

License
-------

BSD

Author Information
------------------

