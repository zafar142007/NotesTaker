#!/bin/bash
path=~/myNotes/
mkdir $path
serial="$(find $path -type f | wc -l)"
touch "$path"newNote"$serial".txt
j=1
while [ "`xclip -selection clipboard -o`" != "" ]; do
	if [ "$i" != "`xclip -selection clipboard -o`" ]; then
		if [ $j -gt 1 ]; then  #Ignore what is already in the clipboard (for j=1)
			echo "\n--------------Note $j---------------" >> "$path"newNote"$serial".txt
			echo "Time: `date`" >> "$path"newNote"$serial".txt
			echo "`xclip -selection clipboard -o`" >> "$path"newNote"$serial".txt
		fi
		j=$((j+1))
	fi
	i="`xclip -selection clipboard -o`"
	sleep 1
done
