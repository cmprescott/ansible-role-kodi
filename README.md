Ansible Role: Kodi
=========
[![Build Status](https://travis-ci.org/cmprescott/ansible-role-kodi.svg?branch=master)](https://travis-ci.org/cmprescott/ansible-role-kodi)

Installs and configures Kodi.

Requirements
------------

```shell
# Ansible version 1.8.4+
ansible --version

# OS
case $OSTYPE in
  # Linux needs apt
  "linux"*)
      apt --version;;
esac
```

Role Variables
--------------

```yaml
# Each of these are just arrays of file paths
kodi_source_files: []
kodi_source_music: []
kodi_source_pictures: []
kodi_source_programs: []
kodi_source_videos: []


# Optional settings (Not defined by default)
kodi_pkg_pvr:           # See http://kodi.wiki/view/PVR_recording_software
kodi_mysql_server:
kodi_mysql_user:
kodi_mysql_pass:
kodi_advanced_settings: # Write as much XML as you want into here
```

Dependencies
------------

None.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - name: media client
      role: cmprescott.kodi
      kodi_source_videos: [ '/mnt/kodi/Movies' ]
```

License
-------

BSD

Author Information
------------------

Prescott Chris
