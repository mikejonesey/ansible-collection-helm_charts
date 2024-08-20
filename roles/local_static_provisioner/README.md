mikejonesey.helm_charts.local_static_provisioner
=========

This role is not activley used or maintained, it was used once upon a time to set up lvm or bind pv available to k8s.

Requirements
------------

For LVM volumes, the volume group must pre-exist, the role will only create volumes (lv), not volume groups (vg), or physical volumes (pv).

Role Variables
--------------

### Example LVM

```yaml
helm_lsp_lvm_volumes:
  lvmpv1:
    create: yes
    class: lvm-static
    volume_group: vg1
    size: 10g
  lvmpv2:
    create: yes
    class: lvm-static
    volume_group: vg1
    size: 10g
  lvmpv3:
    create: yes
    class: lvm-static
    volume_group: vg1
    size: 10g
  lvmpv4:
    create: yes
    class: lvm-static
    volume_group: vg1
    size: 10g
  lvmpv5:
    create: yes
    class: lvm-static
    volume_group: vg1
    size: 50g
  lvmpv6:
    create: yes
    class: lvm-static
    volume_group: vg1
    size: 50g
```

Example Bind

```yaml
helm_lsp_bind_volumes:
  - name: bind1
    class: bind-static
    source: /srv/k8s-local-bind/source1
  - name: bind2
    class: bind-static
    source: /srv/k8s-local-bind/source2
  - name: bind3
    class: bind-static
    source: /srv/k8s-local-bind/source3
  - name: bind4
    class: bind-static
    source: /srv/k8s-local-bind/source4
  - name: bind5
    class: bind-static
    source: /srv/k8s-local-bind/source5
```

Dependencies
------------

n/a

Example Playbook
----------------

    - name: Kubernetes Functionality
      hosts: '{{ helm_k8s_master_target | default("k8s_master") }}'
      roles:
        - name: Local Static Provisioner
          role: mikejonesey.helm_charts.local_static_provisioner
          run_once: true
          when: "helm_lsp_lvm_volumes|length>0 or helm_lsp_bind_volumes|length>0"
          tags: local,lvm,bind,provisioner
         
        - name: Other Provisioner
          ...
      tags: provisioners

License
-------

GPL-2.0-or-later

Author Information
------------------

Michael Jones https://www.mikejonesey.co.uk/
