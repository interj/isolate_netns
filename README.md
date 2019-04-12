# isolate_netns

More than a few times I needed a simple tool routing traffic from specific application through different network interface.
This does just that.

## Requirements
- dnsmasq
- ip-netns - every Linux past 2.2 should have it

## Usage
Script can be run either as interactive shell, 
or simply execute commands passed after interface name in isolated network environment.

```
Usage: isolate_netns [OPTION]... INTERFACE [SHELL_COMMAND]

Run shell with isolated network, execute SHELL_COMMAND if present, interactive shell otherwise
-d DNS ip address, assumed to be the same as gateway address if not present
-g gateway ip address, will use interface default if not present
-a host ip address with prefix length, will use interface default if not present
-h this help
```
