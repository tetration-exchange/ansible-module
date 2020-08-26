Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

Testing
-------
Python Testing is done via Pytest.
- Create a Virtual Environment
- Install Dependencies from `requirements.txt`
- Run the command `pytest --cov=. --cov-report term-missing --cov-fail-under=80 tests/`

Ansible Testing is done via Molecule
- Create a Virtual Environment
- Install Dependencies from `requirements.txt`
- Run the command `molecule converge -s users` to run the Users scenario
- Run the command `molecule converge --all` to run all the scenarios

The scenarios are in the **molecule** folder.  Each scenario is named after the module its tests are written for.  Molecule is designed to do stuff to a VM/Container and then test the state of the container.  Since this is not the case, instead we use the `converge.yml` file to exercize the role.  

Environmental variables are set in the `molecule.yml` file.  If you have an `.env.yml` file set in the project root, when molecule runs, it will set the contents of that file as environmental variables. This way you can test both local and remote.


License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
