# System Baseline

Apply system baseline configuration.

## How to use it

Set the following to true or false in `config/host/<name>.yaml` or `/config/defaults.yaml`:

* `configure_dns` - Configure to corp DNS servers.
* `configure_ntp` - Configure chrony to point at corp NTP servers.
* `configure_updates` - Configure dnf-automatic security updates.
* `configure_proxy` - Set systemd, profile, and environment variables for proxy.
* `configure_cowdsec` - Configure cowdsec.
* `configure_security` - Baseline security hardening.
* `configure_baseline` - Create systemd service `baseline` to run this every 30 minutes.

OpenStack metadata can be set to `"true"` to apply the roles:

* `au.hahl.baseline.role-dns=True`
* `au.hahl.baseline.role-ntp=True`
* `au.hahl.baseline.role-updates=True`
* `au.hahl.baseline.role-proxy=True`
* `au.hahl.baseline.role-baseline=True`
* `au.hahl.baseline.role-crowdsec=True`
* `au.hahl.baseline.role-Security=True`


# Misc

To run the update manually `systemctl start baseline`.

