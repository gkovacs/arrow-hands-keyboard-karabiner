# arrow-hands-keyboard-karabiner

Maps alt+left hand keys (qwerty asdfeg) to arrow keys and pc-style home/end. Includes both qwerty and colemak versions

This is for OSX, it is the Karabiner elements equivalent of https://github.com/gkovacs/arrow-mouse-hands-keyboard (which is for X11 / linux)

To install, place the contents of this repo into your `~/.config/karabiner` directory

## Installation

Install Karabiner elements

```
cd ~/.config/
rm -rf karabiner # this deletes your existing karabiner configuration
git clone https://github.com/gkovacs/arrow-hands-keyboard-karabiner.git karabiner
```

## Compose key

Also includes compose key support. It is mapped to fn+space as well as to delete (fn+backspace). It is generated as follows (must be run on Ubuntu)

```
cat /usr/share/X11/locale/en_US.UTF-8/Compose | perl compose2keybindings.pl > DefaultKeyBinding.dict
```

Then replace

```
	"\UF710" = {
```

With

```
	"\U00A7" = {
```

And copy the resulting file to `~/Library/KeyBindings/DefaultKeyBinding.dict`

## License

MIT

## Credits

By [Geza Kovacs](https://github.com/gkovacs)

