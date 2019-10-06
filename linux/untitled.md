# Linux and Network troubleshooting

First step before troubleshooting, is to understand what you are troubleshooting. try narrowing the scope.

### List of last reboots

```text
last reboot

who -b
```

### Issues with test vms getting unresponsive

hypotesys:

* things are related to hypervisor
* collectd
* sensu
* file system corruption

facts:

* top shows that a vm has high cpu utilization but the vm shows no sign of cpu utilization

### Memory

[https://linuxhint.com/check\_memory\_usage\_process\_linux/](https://linuxhint.com/check_memory_usage_process_linux/)

```text
sudo pmap 15336 | tail -n 1
sudo pmap 917 531 | grep total
```

### Piping

```text
netstat -noatup | vim
```

### System core dumps

* [Understand and configure core dumps on Linux](https://linux-audit.com/understand-and-configure-core-dumps-work-on-linux/)

  ```text
  gdb core.xxx
  ```

### References

* [Five rules for troubleshooting an unfamiliar system](http://www.mooreds.com/wordpress/archives/2043)

