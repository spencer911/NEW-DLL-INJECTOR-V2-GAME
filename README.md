# NEW-DLL-INJECTOR-V2-GAME
* ![crates.io](https://img.shields.io/crates/v/dll-injector.svg)

Hello, everyone! Thank you for choosing Harvey's Injector.

This injector will allow you to open DLL files and choose your process, similar to RemoteDLL.

If you encounter any problems concerning my injector, feel free to contact me on Discord!

Discord: RcsUan#0077

I will try my best to fix any problem you encounter. :-)

Sincerely, Rcs

## Introduction

***Dll-Injector*** is a **Windows dynamic-link library** injection tool written in *C++21*. It can inject a `.dll` file into a running process by searching its window title or create a new process with an injection.

## Getting Started

**Warning**

> The project does not contain building configuration files, the source code can be built manually with *Visual Studio 2022*.

### Prerequisites

The project need to configure on/for **Windows 32-bit**.

## Usage

```console
Dll-Injector [-f <proc-path> | <win-title>] <dll-path>
```

**Inject a Dll into a Running Process**

To inject a `.dll` file into a running process, you need to specify the *window title* of the target process and the *path* of the `.dll` file. If `dll-path` is a relative path, it must be relative to the `Dll-Injector.exe`.

```console
Dll-Injector <win-title> <dll-path>
```

For example, inject the `dllmain_msg.dll` (assume it is in the same directory as *Dll-Injector*) into *Windows Calculator*:

```console
Dll-Injector Calculator dllmain_msg.dll
```

**Create a New Process with an Injection**

To create a new process with an injection, you must enable the `-f` option firstly and then specify the *paths* of the target process and the `.dll` file. If `dll-path` is a relative path, it must be relative to the process file.

```console
Dll-Injector -f <proc-path> <dll-path>
```
![image](https://user-images.githubusercontent.com/98352276/152540465-6e67bf42-68e9-453b-98d4-b0ac4a7f6b2c.png)
