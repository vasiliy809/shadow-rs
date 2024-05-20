## Hide Driver

Description:
This command allows you to hide a specific driver on the system.

```powershell
shadow.exe driver hide --name <name>
```
Options:
* `hide`: Hides the specified driver.
* `name`: The name of the driver file (e.g., `example.sys`) you want to hide.

Example of use:

```powershell
shadow.exe driver hide --name example.sys
```

This command will hide the driver named `example.sys`.

## Enumerate Driver

Description:
This command lists all drivers currently loaded in the system.

```powershell
shadow.exe driver -l
```
Options:
* `-l / --list`: Lists all loaded drivers.

