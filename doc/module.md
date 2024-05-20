## Hide Module

Description: This command allows you to hide a specific module in the system.
```powershell
shadow.exe module hide --pid <pid> --name <name>
```
Options:
- `hide`: Hides the specified module.
- `pid`: The process ID (PID) of the process where you want to hide the module.
- `name`: The name of the module to hide, including the full path.

Example of use:
```powershell
shadow.exe module hide --pid 1234 --name C:\Windows\System32\KERNEL32.DLL
```

This command will hide the module with the name `C:\Windows\System32\KERNEL32.DLL` in the process with PID `1234`.

# Enumerate Module

Description: This command allows you to list all modules in a specific process.
```powershell
shadow.exe module enumerate --pid <pid>
```
Options:
- `enumerate`: Lists the modules in the specified process.
- `pid`: The process ID (PID) of the process whose modules you want to list.

Example of use:
```powershell
shadow.exe module enumerate --pid 1234
```

This command will list all modules loaded by the process with PID `1234`.