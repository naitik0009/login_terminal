trap 'echo hey you cant bypass this login' SIGINT
while true 
do
	echo "enter your username : "|lolcat
	read username
	echo "enter your password  :"|lolcat
	read -s password
	if [[ $username == 'kali' && $password == 'kali' ]]
	then
		printf "welcome <your name>" | espeak
		clear
		

# ~/.bashrc: executed by bash(1) for non-login shells.

# Note: PS1 and umask are already set in /etc/profile. You should not
# need this unless you want different defaults for root.
# PS1='${debian_chroot:+($debian_chroot)}\h:\w\$ '
# umask 022

# You may uncomment the following lines if you want `ls' to be colorized:
# export LS_OPTIONS='--color=auto'
# eval "`dircolors`"
# alias ls='ls $LS_OPTIONS'
# alias ll='ls $LS_OPTIONS -l'
# alias l='ls $LS_OPTIONS -lA'
#
# Some more alias to avoid making mistakes:
# alias rm='rm -i'
# alias cp='cp -i'
# alias mv='mv -i'

printf "
 ██ ▄█▀▄▄▄       ██▓     ██▓
 ██▄█▒▒████▄    ▓██▒    ▓██▒
▓███▄░▒██  ▀█▄  ▒██░    ▒██▒
▓██ █▄░██▄▄▄▄██ ▒██░    ░██░
▒██▒ █▄▓█   ▓██▒░██████▒░██░
▒ ▒▒ ▓▒▒▒   ▓▒█░░ ▒░▓  ░░▓  
░ ░▒ ▒░ ▒   ▒▒ ░░ ░ ▒  ░ ▒ ░
░ ░░ ░  ░   ▒     ░ ░    ▒ ░
░  ░        ░  ░    ░  ░ ░  
                            \r\n" | lolcat
		break;
	elif [[ $username != 'kali' ]]
	then 
		echo "wrong username"
	elif [[ $password != 'kali' ]]
	then 
		echo "wrong password"
	else
		echo "something went wrong"
	fi
done
