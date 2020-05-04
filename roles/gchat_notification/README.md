g-chat-notification-for-aws
=========

This role was made to simplify interactions between AWS usage and notifications.  This role will take the parsed output of an AWS API response and parse the message to a given gchat room based on the template selected.

Requirements
------------

Ansible, AWS, a brain

Role Variables
--------------

url- The gchat webook url used for comms
header- which notification template should be used
body- a template lookup stored in as a var, for example: "{{ lookup('template', 'default.j2') }}"

Dependencies
------------

It is expected that this role will be called after AWS has been called and the instances of interest that you wish to notify about have been selected.

Example Playbook
----------------
ansible-playbook -i localhost, --role gchat_notification -e "@vars.yml"
(where vars.yml contains the required vars)

or
ansible-playbook -i localhost, --role gchat_notification
(if you have decided to shove your vars in the vars.yml file within the role)


TBD

License
-------

BSD

Author Information
------------------

Brandon Marlow lives in the Pacific Northwest with his wife and a gaggle of animals.  In his (little) spare time he enjoys building things and writing terrible json queries.
