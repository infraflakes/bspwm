### Personal bspwm config on imperative distros

Prerequisites:

```
bspwm sxhkd xsel feh polybar terminus-font terminess-nerd-font rofi brightnessctil scrot slock
```

Put these in .config (I personally use stow):
```bash
stow -t ~/.config config
```

Xorg touchpad config:

```
sudo cp -r etc/X11/xorg.conf.d/* /etc/X11/xorg.conf.d
```

Setting up external monitor:

```bash
xrandr -q
```

Then set up as accordingly (example):

```bash
xrandr --output HDMI-1-0 --primary --mode 1920x1080 --pos 0x0 --rate 60 \
                    --output eDP-1  --mode 1920x1080 --pos 1920x0 --rate 144 \
                    --right-of HDMI-1-0
```
