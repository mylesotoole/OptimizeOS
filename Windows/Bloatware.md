## Debloat Windows 11

### Powershell (Admin):

#### Remove all preinstalled Microsoft apps (can be redownloaded again through the store):

```powershell
Get-AppxPackage -AllUsers | Remove-AppxPackage
```

#### Add back Microsoft store:

```powershell
Get-AppxPackage -allusers Microsoft.WindowsStore | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```

#### Third-party advanced debloating tool:

```powershell
irm christitus.com/win | iex
```
