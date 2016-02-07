#!/bin/bash
mkdir ~/myNotes
serial="$(find ~/myNotes/myNotes -type f | wc -l)"
touch ~/myNotes/newNote"$serial".txt
j=1
while [ "`xclip -selection clipboard -o`" != "" ]; do
	if [ "$i" != "`xclip -selection clipboard -o`" ]; then
		if [ $j -gt 1 ]; then  #Ignore what is already in the clipboard (for j=1)
			echo "\n--------------Note $j---------------" >> newNote"$serial".txt
			echo "Time: `date`" >> newNote"$serial".txt
			echo "`xclip -selection clipboard -o`" >> newNote"$serial".txt
		fi
		j=$((j+1))
	fi
	i="`xclip -selection clipboard -o`"
	sleep 1
done
