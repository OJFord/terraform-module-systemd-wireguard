Configure a full-mesh WireGuard network on a list of terraform-managed peer servers, and optionally a local peer (e.g. for management).

## Dependencies

On the remote peers:
* systemd >= v243
* systemd-networkd
* wireguard-dkms
* wireguard-tools

Locally:
* jq

### Optionally

Locally, if configuring a `local_peer`:
* wireguard-tools

If `use_extant_systemd_conf`:
* configured systemd-networkd netdev with the same interface name as provided to this module (e.g. default `wg0`)