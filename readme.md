# Usage


## Visual Studio Code
to use vscode_settings symlink it.

first delete settings if its there:

```sh
rm ~/.config/Code/User/settings.json
```

```sh
ln vscode_settings.json ~/.config/Code/User/settings.json
```

## Ubuntu key fixes

Modiefied from this [vim keys guide](https://itectec.com/ubuntu/ubuntu-configure-caps-lock-as-altgr-and-arrows-like-in-vim/) to emacs keys

This changes Caps lock to altgr and adds emac movement for caps+key

This should probably also be enough to symlink, but only copied file when i did it.

```sh
ln xkb_altgr_emacs /usr/share/X11/xkb/symbols/altgr_emacs
```

Now we need to include the file into all language files that we use. For me this is english so the `us` file and norwegian `no` file.

Add `include "altgr_emacs(altgr-emacs)"` to the end of the `{xkb_symbols "basic"}` section in the language files you need in `/usr/share/X11/xkb/symbols`
