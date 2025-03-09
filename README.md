# Chinese macropad in linux (ubuntu)

This page describe how to use a chinese macropad (3 keys + 1 knob) in Ubuntu (24.10).

1. Buy a macropad [on aliexpress](https://s.click.aliexpress.com/e/_EyCfpXA) like this one 

![](macropad.jpg)

2. Clone this repo

3. Edit mapping.yaml file to set your own key shortcuts

```yaml
orientation: normal
rows: 1
columns: 3
knobs: 1
layers:
- buttons:
  # first, second and third button
  - ["q", "ctrl-shift-q", "alt-shift-q"]
  knobs:
  # counter clock wise, press and clock wise knob
  - ccw: "alt-ctrl-shift-r"
    press: "alt-ctrl-shift-t"
    cw: "alt-ctrl-shift-y"
```

4. Validate your configuration

```shell
tools/ch57x-keyboard-tool validate < mapping.yaml
```

5. Connect your macropad and check it :

```shell
lsusb
   ...
   Bus ... Device ...: ID 1189:8890 Acer Communications & Multimedia 
   ...
```

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


