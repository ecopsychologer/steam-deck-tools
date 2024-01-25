# steam-deck-tools

Fix packages with missing files
`sudo pacman -S $(pacman -Qk 2>/dev/null | grep -ve ' 0 missing' | awk -F: '{print $1}')`

