# Awesome Alternative CLI
> a list of programs to replace the ancient Coreutils

# Common Commands

## alias
This is being mentinoned as a sort of pre resqiuite to everything else. You'll probably want whatever you switch to to keep working like you're used to, so using aliases can help. To make them persistant you'll likely need to put them in your shell's config file, so your `.bashrc`, `.zshrc`, or whatever depending on what shell you use. This is particularly powerful when you consider that these alises can include flags (ex: `alias ls="lsd -la"`) or be basically full scripts (ex: `alias cb="git branch | fzf | sed 's/\* //g' | xargs -I '{}' git checkout {}"`)

it's also worth mentioning that these scripts themselves can be used as aliases in a way using using **functions**

for example with this,

```bash
function timer() {
  total=$1
  for ((i=total; i>0; i--)); do sleep 1; printf "Time remaining $i secs \r"; done
  echo -e "\a"
}
```

in the shell config file you can run `timer 10` directly or use it as part of other scripts

finally, if you need an 'alias' that can work across shells would an option is to drop an executable script somewhere in your path.

## uname

> uname is used to get info on the kernel version and system architecture

For a fancy system information display:

**[screenfetch](https://github.com/KittyKatt/screenFetch)** -

**[lemongrab](https://github.com/Aareon/lemongrab)** -

**[neofetch](https://github.com/dylanaraps/neofetch/)** -

For actually getting debug infor about the kernel:

`cat /proc/version` or `dmesg | grep -i "linux version"` but neither provided any info left out from `uname -a`. 

you may be able to find more information about your kernel by digging around in `/lib/modules/[kernel version]`

depending on your bootloader, you may find more info in `/boot/loader/entries/[yourOS].conf` 

## awk, sed, tr, and cut
> awk, sed, tr, and cut are often used for shell scripting as data is piped from the output from one command to another.
>
> see also [grep](#grep/egrep)

**[choose](https://github.com/theryangeary/choose)** -

## cal

> okay, so cal itself isn't even a core util, but I'm counting it anyway dangit. It just displays a cute lil' terminal calendar. Lightweight, sure, but there's better out there:

**[khal](https://github.com/pimutils/khal)** -

## cat
> cat is supposed to be short for concatenate, so that you can use `cat file1 file2` to merge two files onto stdout, but, really most people just use it to quickly read a file in the terminal and it pretty much sucks for that.

**[bat](https://github.com/sharkdp/bat)** -

**[mdcat](https://github.com/lunaryorn/mdcat)** -

**[hexyl](https://github.com/sharkdp/hexyl)** -

## cfdisk

## cd
See [Directory Navigation]

## cp
rsync

## cron

## curl & wget

## date

## dc (desk calculator) & bc
> dc, a calculator that you have to look up to figure out how to use.
> bc, a better but still pretty lame calculator

**[qalc](https://github.com/Qalculate/libqalculate)** - Qalculate!
**[bitwise](https://github.com/mellowcandle/bitwise)** -

...python? - I mean, python's interactive shell makes for a great caculator too.

Honorable mention: **[speedcrunch]()** - speedcrunch is gui based, but not in the god-awful way that a lot of gui calculators are. It works really well. If you've got a display server running and can it's worth it.

## dd

## df
**[duf](https://github.com/muesli/duf)** -

## diff
diff-so-fancy
icdiff
delta

## dig

## dmesg

## du
ncdu

## echo
echoowo
lolcat
figlet
toilet
banner

## env
https://direnv.net

## file

## find
fd

## gcc

## gdb
gef

## git
radicle

## grep/egrep
ripgrep

## history
resh

## ip / ifconfig

## ls
lsd
exa

lsof
lsusb
lstopo
lshw
lsblk
lsns
lspci

## make

## man

## mkdir

## mv

## nc (netcat)

## netstat

## nice

## ping
**[prettyping](https://github.com/denilsonsa/prettyping)** -

## ps

## rm/rmdir

## screen
tmux

## sleep

## sort

## ssh

**[mosh](https://mosh.org)** - 

## tar/gzip/bzip/etc

## trap

## time

## top
htop
ghtop

## traceroute

## uniq

**[runiq](https://github.com/whitfin/runiq)** -

## wc

# Shells
zsh
fish
xonsh

## Shell scripting
up (ultimate plumber)
rat

# Networking
scapy

# Text editors
## vim
spacevim
neovim

# Directory navigation
nnn
ranger
autojump

# New basic Tools
moreutils
hr
fltrdr
irssi
jq
crex
entr
noti
pandoc
uxy

# Task Managment
taskwarrior

# Security Realted

# Overclocking
stress-ng
dmidecode

# Communication
irssi
lx
gist

# Multimedia
orca-c
waifu-2x
mpd+ncmpcpp

# Internet
lynx
w3m
browsh
youtube-dl

# other
wttr
