#include <linux/module.h>	-> always needed
#include <linux/kernel.h>   -> needed for log level enums (KERN_INFO, ...)

int init_module(void) -> function that runs when module is loaded
printk(KERN_INFO "Hello world.\n") -> printk (print kernel) logs to /var/log/messages or /var/log/syslog
void cleanup_module(void) -> function that runs when module is unloaded


Metadata, you can see it running modinfo *file.ko*
MODULE_LICENSE("GPL") -> if not defined, you'll get a warning 
MODULE_AUTHOR("Girardin")
MODULE_DESCRIPTION("Simple hello world module")