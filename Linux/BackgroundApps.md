## Show all startup applications

```cd /etc/xdg/autostart/```

```sudo sed --in-place 's/NoDisplay=true/NoDisplay=false/g' *.desktop```

## Disable Pop!_Shop (Pop!_OS)

```mkdir -p ~/.config/autostart```

```cp /etc/xdg/autostart/io.elementary.appcenter-daemon.desktop ~/.config/autostart/```

```echo "X-GNOME-Autostart-enabled=false" >> ~/.config/autostart/io.elementary.appcenter-daemon.desktop```
