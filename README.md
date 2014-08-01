# Ansible Environment Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-role-environment.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-role-environment)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-role-environment.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-role-environment)

> `environmanet` is an [Ansible](http://www.ansible.com) role which:
> 
> * adds `/etc/environment` variables

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.environment
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.environment
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-role-environment.git
```

## Variables

```
# environment_config:
#   - { name: LC_ALL, value: en_US.UTF-8 }
#
environment_config: []
```

## Example playbook

```
- host: all
  roles: 
    - franklinkim.environment
  vars:
    environment_config:
      - { name: LC_ALL, value: en_US.UTF-8 }
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-role-environment.git
$ cd ansible-role-environment
$ vagrant up
```

## Contributing
[![I Love Open Source](http://www.iloveopensource.io/images/logo-lightbg.png)](http://www.iloveopensource.io/projects/53da2bea87659fce66003fa9)

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.