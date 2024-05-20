# Callback

Description: This command provides operations for managing various system callbacks.

```powershell
shadow.exe callback [OPTIONS] --callback <CALLBACK>
```

Options:

- `-l, --list`: Enumerate existing callbacks.
- `-e, --enumerate`: Enumerate removed callbacks.
- `--remove`: Remove a specific callback.
- `--restore`: Restore a specific callback.
- `-c, --callback`: Specify the type of callback for operations.

Callback Types:

- `process`: Callback for process creation notifications (`PsSetCreateProcessNotifyRoutine`).
- `thread`: Callback for thread creation notifications (`PsSetCreateThreadNotifyRoutine`).
- `load-image`: Callback for image loading notifications (`PsSetLoadImageNotifyRoutine`).
- `registry`: Callback for registry change notifications (`CmRegisterCallbackEx`).
- `ob-process`: Callback for object processing related to processes (`PsProcessType`).
- `ob-thread`: Callback for object processing related to threads (`PsThreadType`).

Example Usage:

1. List Existing Callbacks:
```powershell
shadow.exe callback -l
```
This command enumerates all currently active callbacks.

2. Enumerate Removed Callbacks:
```powershell
shadow.exe callback -e
```
This command lists callbacks that have been previously removed.

3. Remove a Callback:
```powershell
shadow.exe callback --remove 1234 --callback process
```
This command removes a process creation callback identified by `1234`.

4. Restore a Callback:
```powershell
shadow.exe callback --restore 1234 --callback load-image
```
This command restores a previously removed image loading callback identified by `1234`.

