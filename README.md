# steam-deck-tools

### Fix packages with missing files
`sudo pacman -S $(pacman -Qk 2>/dev/null | grep -ve ' 0 missing' | awk -F: '{print $1}')`


### Full Setup
`sudo steamos-readonly disable && sudo pacman-key --init && sudo pacman-key --populate archlinux && sudo pacman -Syu tmux htop wget git base-devel cmake gcc $(pacman -Qk 2>/dev/null | grep -ve ' 0 missing' | awk -F ':' '{print $1}') --overwrite '*'`
