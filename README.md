# pacadd
A simple tool for managing repositories in Arch Linux

## How-to use:

**sudo pacadd -h**

## Usage: pacadd [options] NAME URL [options]
```
  -a, --add NAME URL			Adds [NAME] and Server=URL to /etc/pacman.conf
  	-a URL -i			Adds Server=URL to /etc/pacman.d/mirrorlist or <path> (if declared)
  	-a NAME -i			Adds [NAME] and Include=/etc/pacman.d/mirrorlist or <path> (if declared) to /etc/pacman.conf
  	-a NAME -s URL -i		Adds [NAME] and Include=/etc/pacman.d/mirrorlist to /etc/pacman.conf; Server=URL to /etc/pacman.d/mirrorlist
  	-a NAME -s URL -i <path>	Adds [NAME] and Include=<path> to /etc/pacman.conf;  Server=URL to <path>
	-a NAME -ts URL			Adds [NAME] and Server=URL/$repo/os/$arch to /etc/pacman.conf
  	-a URL -ts			Adds Server=URL/$repo/os/$arch to /etc/pacman.d/mirrorlist
  	-a URL -ts -i			Adds Server=URL/$repo/os/$arch to /etc/pacman.d/mirrorlist or <path> (if declared)
  	-a NAME -s URL -i <path> -ts	Adds [NAME] and Include=<path> to /etc/pacman.conf; Server=URL/$repo/os/$arch to /etc/pacman.d/mirrorlist
  -r, --remove NAME			Removes [NAME] from /etc/pacman.conf and /etc/pacman.d/mirrorlist
  	-r -m URL			Removes Server=URL from /etc/pacman.d/mirrorlist
  	-r -m URL <path>		Removes Server=URL from <path>
  -c, --comment NAME			Comment out the line of [NAME] from /etc/pacman.conf
  -u, --uncomment NAME			Uncomment the line of [NAME] from /etc/pacman.conf
  ```

# Exit codes:
1 - invalid argument(s) \
2 - mirror exists \
3 - invalid address \
4 - repo exists \
5 - repo commented out \
6 - file not exists \
7 - repo not found

# AUR git clone link:
https://aur.archlinux.org/pacadd.git
