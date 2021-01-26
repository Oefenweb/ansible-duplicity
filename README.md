## duplicity

[![CI](https://github.com/Oefenweb/ansible-duplicity/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-duplicity/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-duplicity-blue.svg)](https://galaxy.ansible.com/Oefenweb/duplicity)

Set up (the latest version of) [duplicity](http://duplicity.nongnu.org/) in Ubuntu systems.

#### Requirements

* `python-apt`

#### Variables

* `duplicity_install_method`: [default: `native`]: The way to install duplicity (e.g. `native` (from Ubuntu repo), `ppa` (`ppa:duplicity-team/duplicity-release-git`), or `pip`)

* `duplicity_pip_dependencies_python`: [default: `['duplicity==0.8.13']`]: Pip dependencies to install. Only relevant when using `duplicity_install_method: pip`

* `duplicity_install`: [default: `[]`]: Additional packages to install (e.g. `ncftp`)

## Dependencies

* `build-essential` (will be installed)
* `librsync-dev` (will be installed)
* `rdiff` (will be installed)
* `gettext` (will be installed)

* `python(2|3)` (will **not** be installed)
* `python(2|3)-dev` (will **not** be installed)
* `pip` (will **not** be installed)

when using `duplicity_install_method: pip`

#### Example(s)

##### Default

```yaml
---
- hosts: all
  roles:
    - duplicity
```

##### PPA

```yaml
---
- hosts: all
  roles:
    - duplicity
  vars:
    duplicity_install_method: ppa
```

##### Pip

```yaml
---
- hosts: all
  roles:
    - duplicity
  vars:
    duplicity_install_method: pip
    # Always install latest
    duplicity_pip_dependencies_python:
      - duplicity
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-duplicity/issues)!
