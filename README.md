# chinese macropad in linux (ubuntu)

This page describe how to use a chinese macropad (3 keys + 1 knob) in Ubuntu (24.10).

1. Buy a macropad on aliexpress : 

2. Clone this repo

3. Edit mapping.yaml file to set your key own shortcuts 

4. Validate your configuration

```shell
tools/ch57x-keyboard-tool validate < mapping.yaml
```

5. Connect your macropad

6. Apply configuration to your macropad

```shell
tools/ch57x-keyboard-tool upload < mapping.yaml
```

To change led configuration :

```shell
# configuration 1
tools/ch57x-keyboard-tool led 1

# configuration 2
tools/ch57x-keyboard-tool led 2

# switch off
tools/ch57x-keyboard-tool led 0
```

## References

- https://github.com/kriomant/ch57x-keyboard-tool
- https://xaviesteve.com/7047/setup-macropad-aliexpress-linux/
- http://www.fabienm.eu/wordpress/2024/03/18/configuration-dun-clavier-3-boutons-sous-linux/


