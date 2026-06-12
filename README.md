# razer-blade-15-rz09-audio
razer blade 15 z09 audio fix


put sh in `/usr/local/bin/razer-blade-15-rz09-audio.sh`

assing run perms `chmod +x /usr/local/bin/razer-blade-15-rz09-audio.sh`

run script `sudo  /usr/local/bin/razer-blade-15-rz09-audio.sh`

edit `sudo nano /etc/systemd/system/razer-audio.service`

```sh
[Unit]
Description=Razer Blade Audio Fix
After=multi-user.target suspend.target hibernate.target hybrid-sleep.target

[Service]
Type=oneshot
ExecStart=/usr/local/bin/razer-blade-15-rz09-audio.sh

[Install]
WantedBy=multi-user.target suspend.target hibernate.target hybrid-sleep.target
```

run `sudo systemctl daemon-reload`
