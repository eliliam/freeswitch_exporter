# Systemd Unit

Copy freeswitch_exporter to directory `/usr/local/bin/`

The unit file in this directory is to be put into `/etc/systemd/system`.
Create a file at `/etc/defaults/freeswitch_exporter.defaults` with the contents containing any options to pass, example:

```shell
OPTIONS="--web.listen-address=':9282' --freeswitch.password='Freeswitch_esl_password'"
```

Enable and start the service via:

```shell
sudo systemctl daemon-reload
sudo systemctl enable freeswitch_exporter.service
sudo systemctl start freeswitch_exporter.service
```
