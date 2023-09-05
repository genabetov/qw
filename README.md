# QuakeWorld package

## For Windows users

Just [download a zip archive](https://github.com/genabetov/qw/archive/refs/heads/main.zip), don't forget to extract it.

- `ezquake-std.exe` - client with legacy renderer
- `ezquake-glsl.exe` - client with modern renderer

## For Linux haxxors

```bash
sudo apt install build-essential libspeex-dev libexpat-dev libcurl4-openssl-dev libspeexdsp-dev libsndfile1-dev libpng-dev libjpeg-dev libcurl4-openssl-dev libjansson-dev libpcre3-dev libnotify-bin libnotify4 libsdl2-dev libpcre3-dev libxxf86vm-dev

cd ~
git clone https://github.com/genabetov/qw
cd qw
git clone https://github.com/QW-Group/ezquake-source
cd ezquake-source
git submodule update --init --recursive
make -j5
cp ezquake-linux-x86_64 ..
cd ..
./quake.sh
```

## Binds

### General binds:

| ` ~                                | W                          | S                    | A                        | D                          | Space                |
|------------------------------------|----------------------------|----------------------|--------------------------|----------------------------|----------------------|
| Toggle console <br>`toggleconsole` | Move forward<br>`+forward` | Move back<br>`+back` | Move left<br>`+moveleft` | Move right<br>`+moveright` | Jump<br>`+jump` |

| Left Mouse Button       | Right Mouse Button   | Middle Mouse Button   | Mouse4                      | Mouse5                | Shift                  | Ctrl                |
|-------------------------|----------------------|-----------------------|-----------------------------|-----------------------|------------------------|---------------------|
| Fire Lightning<br>`+lg` | Fire Rocket<br>`+rl` | Fire Shotgun<br>`+sg` | Fire SuperShotgun<br>`+ssg` | Fire Grenade<br>`+gl` | Fire Nailgun<br>`+sng` | Swing Axe<br>`+axe` |

### Team reports:

| MWheelDown                                                      | MWheelUp                                                               |
|-----------------------------------------------------------------|------------------------------------------------------------------------|
| Full status + Closest mate status<br>`tp_msgreport; shownick 1` | Point Item/Enemy/Mate + Closest mate status<br>`tp_msgpoint; shownick` |

| 1                                   | 2                              | 3                           |
|-------------------------------------|--------------------------------|-----------------------------|
| Quad Dead/Over <br>`tp_msgquaddead` | Enemy Quad<br>`tp_msgenemypwr` | Get Quad<br>`tp_msggetquad` |


| 4                           | 5                             | 6                                | 7                         | C                        |
|-----------------------------|-------------------------------|----------------------------------|---------------------------|--------------------------|
| Get Pent<br>`tp_msggetpent` | Item Soon<br>`tp_msgitemsoon` | Enemy Slipped<br>`tp_msgslipped` | Shortcut<br>`tp_msgtrick` | Coming<br>`tp_msgcoming` |

| E                         | F                             | G                       | Q                              | R                    |
|---------------------------|-------------------------------|-------------------------|--------------------------------|----------------------|
| Took item<br>`tp_msgtook` | No/Cancel<br>`tp_msgnocancel` | Yes/OK<br>`tp_msgyesok` | Need something<br>`tp_msgneed` | HELP<br>`tp_msghelp` |

| T                           | V                          | X                    |
|-----------------------------|----------------------------|----------------------|
| You Take<br>`tp_msgyoutake` | Replace<br>`tp_msgreplace` | Safe<br>`tp_msgsafe` |

### Misc:

| F1                                       | F2                             | F3                       | F4                                 | F5                  | F6                        |
|------------------------------------------|--------------------------------|--------------------------|------------------------------------|---------------------|---------------------------|
| Agree to admin/captain election<br>`yes` | Agree to map change<br>`agree` | Ready to play<br>`ready` | Not ready/Break a match<br>`break` | Join game<br>`join` | Observe game<br>`observe` |

| F12                        | Alt                  |
|----------------------------|----------------------|
| Screenshot<br>`screenshot` | Smiley<br>`say <:=)` |

## Info

**After changing something in game settings you should do console command `cfg_save`**

## Generic console settings

```
name your nickname
color 13 8 // your color in scoreboard
team red // your team
cl_fakename pla // short name in teamplay chat (3 chars max pls)
// also see https://ezquake.com/docs/charsets.html#colored-text
sensitivity 2 // mouse sensitivity
volume 0.3 // sound volume
gamma 0.6 // display gamma
contrast 1.6 // display contrast
crosshairsize 1
crosshaircolor 255 255 0
crosshairimage 7 // from qw/crosshairs
```

**DON'T FORGET ABOUT `cfg_save`**

...and more [there](https://ezquake.com/docs.html)

## Tweaks for potato PCs

```
vid_software_palette 0 // turn on hardware gamma adjustment
vid_usedesktopres 0 // don't use native display resolution
vid_width 640 // display resolution width
vid_height 480 // display resolution height
r_dynamic 0 // turn off dynamic lights
```

### For ultra potatoes

```
r_drawflat 1 // single colored walls and floors
r_fastturb 1 // single colored liquids
r_fastsky 1 // single colored sky
```

### For middle potatoes

```
gl_max_size 16 // max map textures size: must be power of 2
```
