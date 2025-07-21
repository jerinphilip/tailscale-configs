# tailscale-configs

Quick and dirty setup of an additional service setup to headless connect a
machine as a tailscale node.


Can be at one of:

```bash
~/.config/systemd/user/tailscale-usession.service
/etc/systemd/tailscale-usession.service
```

Network and tailscaled are dependencies and this service will be spawned after.

```bash
yay -S tailscale
sudo systemctl enable tailscaled


# edit with headless auth credentials

sudo cp tailscale-usession.service /etc/systemd/system/
systemctl daemon-reload
systemctl enable tailscale-usession
```
