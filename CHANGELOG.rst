====================================
Mikejonesey.Kubernetes Release Notes
====================================

.. contents:: Topics

v1.0.5
======

Release Summary
---------------

Tigera Operator must not be run within a Namespace managed by the operator

Bugfixes
--------

- bugfix, new version of tigera operator must not be installed to a namespace managed by tigera operator - The following namespaces cannot be used - calico-system - calico-apiserver - tigera-system - tigera-elasticsearch - tigera-compliance - tigera-intrusion-detection - tigera-dpi - tigera-eck-operator - tigera-fluentd - calico-system - tigera-manager

v1.0.4
======

Release Summary
---------------

documentation updates, and add local_provisioner to public galaxy

Minor Changes
-------------

- add local_static_provisioner to public galaxy
- lint updat and allow nfs provisioner in galaxy

v1.0.3
======

Release Summary
---------------

Update tigera operator default version

Minor Changes
-------------

- cleanup, lint, and limit packaging for public release for use with mikejonesey.kubernetes
- make tigera operator more flexible and update default version

Bugfixes
--------

- correct file permission values cache dir

v1.0.0
======

