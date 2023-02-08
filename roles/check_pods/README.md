check_pods
==========

Verify that pods are in requested state. By default "Running",
but it is possible to override the state variable.

Requirements
------------

Role relies on `kubernetes.core` collection and calls `kubernetes.core.k8s_info`.

Role Variables
--------------

Variable `desired_state` is set to "Running" by default and can be overriden
when the role is called.

Dependencies
------------

No other roles are required.

Example Playbook
----------------

Hypothetical check for "Failing" state of pods.

    - hosts: localhost
      vars:
        desired_state: "Failing"
      roles:
        - validationsframework.operators_validations.check_pods


License
-------

BSD

Author Information
------------------

Jiri Podivin <jpodivin@redhat.com>
