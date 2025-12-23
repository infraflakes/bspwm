### Personal bspwm config on imperative distros

Prerequisites:

```
bspwm sxhkd xsel xorg-xsetroot feh polybar terminus-font rofi
```

```bash
cp -r config/* .config
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
