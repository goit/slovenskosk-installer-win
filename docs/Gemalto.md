# Gemalto CCID Driver Installer

Filename: **GemPcCCID.exe**


# Command Line Options

| Parameter        | Description                                               |
|------------------|-----------------------------------------------------------|
| `/Q`             | Quiet modes for package                                   |
| `/T:<full path>` | Specifies temporary working folder                        |
| `/C`             | Extract files only to the folder when used also with `/T` |
| `/C:<Cmd>`       | Override Install Command defined by author                |


## Notes

Official command line option `/Q` cannot be used with the **GemPcCCID.exe**.
This parameter will cause the process to exit with error message `Error creating process <<None>>.`

When **GemPcCCID.exe** is run as priviledged process it will extract MSI files
and run quite installation from MSI.

The **GemPcCCID.exe** does not support uninstallation command. Gemalto driver
can be uninstalled with command:

```
msiexec.exe /x{2BDB6BE4-A124-4412-A547-46021A8D17E2}
```