# Setup for Linux

## 1. Put keyboard file into XKB symbols directory

Make a symlink to `/usr/share/X11/xkb/symbols/`:

```sh
sudo ln -s /path/to/programmer-qwerty/linux/usP /usr/share/X11/xkb/symbols/
```

Optionally, copy the file:

```sh
sudo cp /path/to/programmer-qwerty/linux/usP /usr/share/X11/xkb/symbols/
```

## 2. Register the layout

Edit file `/usr/share/X11/xkb/rules/evdev.xml` to have:

```xml
<layout>
  <configItem>
    <name>usP</name>
    <shortDescription>us-programmer</shortDescription>
    <description>US Programmer</description>
  </configItem>
</layout>
```

  
Tip: search for `</layoutList>` in `evdev.xml`. Put the xml block above the `</layoutList>`.

## 3. Add the `usP` keyboard to your desktop environment

## 4. Reboot

