# pacadd
A simple tool for managing repositories in Arch Linux

## How-to use:

**pacadd -h**

## Usage: pacadd [options] NAME URL [options]
```

  -a, --add 'NAME' 'URL'		Adds [NAME] and Server=URL to /etc/pacman.conf
  	-a 'URL' -i			Adds Server=URL to /etc/pacman.d/mirrorlist or <path> (if declared)
  	-a NAME -i			Adds [NAME] and Include=/etc/pacman.d/mirrorlist or <path> (if declared) to /etc/pacman.conf
  	-a NAME -s 'URL' -i		Adds [NAME] and Include=/etc/pacman.d/mirrorlist to /etc/pacman.conf; Server=URL to /etc/pacman.d/mirrorlist
  	-a NAME -s 'URL' -i <path>	Adds [NAME] and Include=<path> to /etc/pacman.conf;  Server=URL to <path>
	-a NAME -ts 'URL'		Adds [NAME] and Server=URL/$repo/os/$arch to /etc/pacman.conf
  	-a 'URL' -ts			Adds Server=URL/$repo/os/$arch to /etc/pacman.d/mirrorlist
  	-a 'URL' -ts -i			Adds Server=URL/$repo/os/$arch to /etc/pacman.d/mirrorlist or <path> (if declared)
  	-a NAME -s 'URL' -i <path> -ts	Adds [NAME] and Include=<path> to /etc/pacman.conf; Server=URL/$repo/os/$arch to /etc/pacman.d/mirrorlist
  -r, --remove 'NAME'			Removes [NAME] from /etc/pacman.conf
  	-r -m 'URL'			Removes Server=URL from /etc/pacman.d/mirrorlist
  	-r -m 'URL' <path>		Removes Server=URL from <path>
  -c, --comment 'NAME'			Comment out the line of [NAME] from /etc/pacman.conf
  -u, --uncomment 'NAME'		Uncomment the line of [NAME] from /etc/pacman.conf
  -l, --list				Shows all available (uncommented) repositories at /etc/pacman.conf
  -c_is_c 'NAME' (or) 'URL'		Checks is [NAME] or Server=URL commented out at /etc/pacman.conf
  	-c_is_c 'URL' -i		Checks is Server=URL commented out at /etc/pacman.d/mirrorlist or <path> (if declared)
  	/ --check_is_commented
  -c_is_u 'NAME' (or) 'URL'		Checks is [NAME] or Server=URL uncommented at /etc/pacman.conf
  	-c_is_c 'URL' -i		Checks is Server=URL commented out at /etc/pacman.d/mirrorlist or <path> (if declared)
  	/ --check_is_uncommented
  -c_is_x 'NAME' (or) 'URL'		Checks is [NAME] or Server=URL exists at /etc/pacman.conf
  	-c_is_x 'URL' -i		Checks is Server=URL exist at /etc/pacman.d/mirrorlist or <path> (if declared)
  	/ --check_is_exists
  ```

# Exit codes:
1 - invalid argument(s) / script executed not as UID 0 \
2 - mirror exists \
3 - invalid address \
4 - repo exists \
5 - repo commented out \
6 - file not exists \
7 - repo not found \
8 - mirror not found

# Echo codes at -c\_is\_\* functions:
1-r - repo not(ok) ? \
1-u - url not(ok) ? \
0-r - repo is(ok) ? \
0-u - url is(ok) ?

# AUR git clone link:
https://aur.archlinux.org/pacadd.git
