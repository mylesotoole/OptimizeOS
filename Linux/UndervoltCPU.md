## Configure Undervolt

### Installation

Install pip

```sudo apt install python3-pip```

Install undervolt::

```sudo pip install undervolt```

### Start on boot

Creat new config file:

```sudo nano /etc/systemd/system/undervolt.service```

Edit config file to match:

```
[Unit]
Description=undervolt
After=suspend.target
After=hibernate.target
After=hybrid-sleep.target

[Service]
Type=oneshot
ExecStart=/usr/local/bin/undervolt -v --core -148 --cache -148

[Install]
WantedBy=multi-user.target
WantedBy=suspend.target
WantedBy=hibernate.target
WantedBy=hybrid-sleep.target
```
Check that your script works:

```systemctl start undervolt```

Now you may enable undervolt service:

```systemctl enable undervolt```