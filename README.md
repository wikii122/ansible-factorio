Role Name
=========

Create headless Factorio server

Requirements
------------

None additional requirements

Role Variables
--------------

    factorio_credentials:
      username: ''
      password: ''
      token: ''

    factorio_admin_pause: yes
    factorio_copy_mods: no
    factorio_game_name: Factorio game
    factorio_game_password: ''
    factorio_max_players: 12
    factorio_mod_dir: mods/
    factorio_path: /opt
    factorio_port: 34197
    factorio_public: no
    factorio_save_name: savegame.zip
    factorio_run_server: yes
    factorio_user: factorio
    factorio_version: stable

    factorio_upload_save: # Undefined, when defined will upload provided save to server

Dependencies
------------

This role does not depend on any other role

Example Playbook
----------------

To use the role you must simply define following playbook:

    - hosts: servers
      roles:
      - wikii122.factorio

To start public server define some configuration changes:

    - hosts: servers
      roles:
      - role: wikii122.factorio
        factorio_public: yes
        factorio_credentials: <your credentials>

To copy mods put those on your controller and put on the path

    - hosts: servers
      roles:
      - role: wikii122.factorio
        factorio_copy_mods: yes
        factorio_mod_dir: <path_to_factorio_dir>/mods
License
-------

This code is realeased with the MIT license, see the LICENSE file.

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Thank you
------------------

A big thank you to [Wube](https://www.factorio.com/game/about) for making [Factorio](https://www.factorio.com/)