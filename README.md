# Ansible role - kypo-user-access

This role was specially designed for KYPO sandbox. It sets user-access public
SSH key as authorized key and optionally sets password to a user.

## Requirements

* This role requires root access, so you either need to specify `become` directive as a global or while invoking the role.

    ```yml
    become: yes
    ```

## Role parameters

Mandatory parameters

* `kypo_user_access_username` - The name of the user to give SSH access to.

Optional parameters.

* `kypo_user_access_password` - The password of user `kypo_user_access_password` (omitted by default).

## Example

The simplest example.

```yml
roles:
    - role: kypo-user-access
      kypo_user_access_username: kypo
```
