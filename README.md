# Ansible Playbook

This playbook is to help bootstrap a new dev env quickly. For now, it presumes MacOS for a lot of the tasks.

If I start using linux regularly again, it's possible that I make duplicate tasks for some things based on OS (e.g. using `brew` vs `apt-get` for package mgmt).

## Prerequisites

Install `ansible`:

`brew install ansible`

Install the ansible homebrew galaxy:

`ansible-galaxy collection install community.general`

## Execution

You can execute this playbook by:

`ansible-playbook [-t some_tag_here] [flags] local.yml`

For example: 

- to see all possible tags:
`ansible-playbook --list-tags local.yml`
- to see all tasks for a given tag (without execution):
`ansible-playbook -t install --list-tasks local.yml`
- to get verbose output use `-v[vvvvv]` (max of 6 `v`s)
`ansible-playbook -t install --list-tasks -vvv local.yml`

