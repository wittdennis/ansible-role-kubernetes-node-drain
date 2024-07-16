# Role Name

Ansible role to drain a Kubernetes node

## Requirements

In order to send drain and (un)cordon commands tasks need to be delegated to a kubernetes control plane. This role assumes you have a `kubernetes_control_plane` group in your inventory.

## Role Variables

```yaml
kubernetes_node_drain_grace_period: 300
kubernetes_node_drain_timeout_seconds: 360
kubernetes_node_drain_retries: 3
kubernetes_node_drain_delay_seconds: 10
kubernetes_node_drain_fallback_enabled: false
```

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: wittdennis.kubernetes_node_drain }

## License

MIT
