## Shellcode

Description:
This command injects shellcode into a specific process.

```powershell
shadow.exe injection shellcode --pid <pid> --path <path> -t [thread / apc]
```
Options:
* `-p / --pid`: The process ID (PID) of the target process.
* `--path`: The path to the shellcode file.
* `-t`: Specifies the injection type, either thread or apc.
- `thread`: Injects the shellcode using a new thread.
- `apc`: Injects the shellcode using an Asynchronous Procedure Call (APC).

Example of use:

```powershell
shadow.exe injection shellcode --pid 5678 --path C:\Path\To\Shellcode.bin -t thread
```

This command injects shellcode from `C:\Path\To\Shellcode.bin` into the process with PID `5678` using the thread injection method.

## DLL

Description:
This command injects a DLL into a specific process.

```powershell
shadow.exe injection dll --pid <pid> --path <path> -t thread
```
Options:
* `--pid`: The process ID (PID) of the target process.
* `--path`: The path to the DLL file to inject.
* `-t`: Specifies the injection type (e.g., thread).

Example of use:

```powershell
shadow.exe injection dll --pid 5678 --path C:\Path\To\Library.dll -t thread
```




