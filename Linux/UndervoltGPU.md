## Configure GPU Power Limit

Create bash script:

```nano ~/nvidia-pl.sh```

Copy text into file:

```
#!/bin/bash

sudo nvidia-xconfig --cool-bits=31

sudo nvidia-smi -pm 1

sudo nvidia-smi -i 0 -pl 130

sudo nvidia-smi -i 0 -lgc 1837

nvidia-settings -a GPUPowerMizerMode=1 
```

Give execute permission:

```chmod +x nvidia-pl.sh```

### Enable on startup:

Launch editor:

```crontab -e```

Add line to end of the file and save:

```@reboot sh /home/$USER/nvidia-pl.sh```

Test if it saved:

```crontab -l```

Check your power limit:

```sudo nvidia-smi```
