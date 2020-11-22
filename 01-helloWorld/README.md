# Hello World Module
## Includes
`#include <linux/module.h>`	-> always needed

`#include <linux/kernel.h>`   -> needed for log level macros (KERN_INFO, ...)

## Functions
`int init_module(void)` -> function that runs when module is loaded

`printk(KERN_INFO "Hello world.\n")` -> output to /var/log/messages or /var/log/syslog; you can also see it running `dmesg`; [reference](https://elinux.org/Debugging_by_printing)

`void cleanup_module(void)` -> function that runs when module is unloaded


## Module metadata
Run `modinfo file.ko` to check this out

`MODULE_LICENSE("GPL")` -> if not defined, you'll get a warning

`MODULE_AUTHOR("Girardin")`

`MODULE_DESCRIPTION("Simple hello world module")`
