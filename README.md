# safe_skype

This is a wrapper around Skype for linux to prevent any UDP connections. This will enable you to use it in restricted environments (eg. at University / eduroam network / ...).

## Install
1. Clone the repo
2. Copy safe_skype to /usr/local/bin (or wherever you feel it's appropriate)
3. add a group named skype
4. add yourself to the the group skype

## How does it work?
The script simply injects iptables rules that block any outgoing UDP traffic of any program started with the group skype. Then it starts Skype with the gid of the skype group.
