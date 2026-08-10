# Changelog

## 1.3.1 - 2026-08-10

* Improvements for `postgresql_objects` role (#12)
  * Add support for schemas
  * Add support for abritrary queries
  * Update role parameters to match modules
  * Fix all linter errors in postgresql roles
* Update ansible-lint to v25 and fix GH workflow (#14)
* Tinc revamp (#13)
  * Replace `json_query` with pure Jinja2
    The JMESPath code is very difficult to read, this commit replaces it with a
    slightly less hacky implementation.
  * Remove unneeded dependency on ansible facts
  * Move complex logic to vars/
  * Clean-up vars/
  * Fix names of private variables
  * Improve selection of addresses for ferm
  * Add variables to override automatic defaults
    Add `tinc__connect_to` and `tinc__ferm_allow_from` variables to allow
    override the defaults computed from other hosts' configurations.
* libvirt_host: support older distros (#16)
* Libvirt roles upgrade (#17, #18)
  * Upgrade ansible-role-libvirt-vm to v1.17.0
  * Upgrade ansible-role-libvirt-host to v1.16.0

## 1.3.0 - 2025-05-10

* New `postgresql` and `postgresql_objects` roles from the Galaxy project
  (https://galaxy.ansible.com/ui/standalone/namespaces/2450/).
* Updated `ntp` and `libvirt_host` roles.
* Various small fixes for `tinc` role.

## 1.2.0 - 2024-11-01

New release adding `tinc` role.

## 1.1.0 - 2024-10-23

New release adding `libvirt_host`, `libvirt_vm`, and `ntp` roles.

## 1.0.0 - 2024-09-11

Initial release with `resolv` role.
