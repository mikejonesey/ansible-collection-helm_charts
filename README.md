# Ansible Collection - mikejonesey.helm_charts

This collection is for the most part deprecated. The only charts that are still maintained / used, are for calico and storage.

## Remaining Roles

### Networking

Calico is still setup early in cluster setup, before fluxcd is installed.

### Storage

The local provisioner performs tasks on host to prepare for the provisioner, which are better suited to ansible.

## Collection Roles

| Name                                                                     | Description                                                                              |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| ~~fluentbit~~                                                            | Migrated to FluxCD                                                                       |
| ~~gitlab_runner~~                                                        | Migrated to FluxCD                                                                       |
| ~~graylog~~                                                              | Migrated to FluxCD                                                                       |
| ~~haproxy_ingress~~                                                      | Migrated to FluxCD                                                                       |
| ~~harbor~~                                                               | Migrated to FluxCD                                                                       |
| [helm](roles/helm)                                                       | Installs helm cli util                                                                   |
| ~~jenkins~~                                                              | Migrated to FluxCD                                                                       |
| ~~kube_prometheus_stack~~                                                | Migrated to FluxCD                                                                       |
| [local_static_provisioner](roles/local_static_provisioner)               | (not in use/maintained) Setup LVM volumes, and install helm chart for local provisioner. |
| [nfs_subdir_external_provisioner](roles/nfs_subdir_external_provisioner) | Install chart for nfs provisioner.                                                       |
| ~~sonarqube~~                                                            | Migrated to FluxCD                                                                       |
| [tigera_operator](roles/tigera_operator)                                 | Install helm chart for Calico                                                            |
| ~~zabbix_helm_chrt~~                                                     | Migrated to FluxCD                                                                       |

