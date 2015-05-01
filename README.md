## duplicity

[![Build Status](https://travis-ci.org/Oefenweb/ansible-duplicity.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-duplicity) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-duplicity-blue.svg)](https://galaxy.ansible.com/list#/roles/3584)

Set up the latest version of [duplicity](http://duplicity.nongnu.org/) in Ubuntu systems.

#### Requirements

* `python-apt`

#### Variables

* `duplicity_install`: [default: `[]`]: Additional packages to install (e.g. `ncftp`)

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
  - duplicity
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-duplicity/issues)!
