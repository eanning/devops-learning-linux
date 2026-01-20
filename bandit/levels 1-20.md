#OverTheWire Bandit Levels 1-20

## Level 1 
Command used: 
ssh bandit1@bandit.labs.overthewire.org -p 2220

## Level 2 
Used ls and cat to read a file with spaces. (cat ./-)

## Level 3
Used cat cat to read the file (cat./--spaces in this filename--)

## Level 4 
Used cd to go into directory and cat to view file

## Level 5 
Used file ./* to show only readable file in currect directory

## Level 6 
Used find . -type f -size 1033c ! -executable (to find non executable = ! / to show regular files = -type f)

## Level 7 
Used grep "millionth" data.txt

## Level 8
Used sort data.txt | uniq -u (Uniq -u Prints only lines that appear exactly once)

## Level 9
Used strings data.txt | grep "===" (strings extracts human-readable text from binary files)

## Level 10
Used base64 -d data.txt (Base64 is encoding, not encryption)

## Level 11 
Used cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m' (tr replaces each letter with the one 13 positions ahead)

## Level 12
xxd -r data.txt | while :; do file - | grep -q gzip && gunzip -c || grep -q bzip2 && bunzip2 -c || grep -q tar && tar -xO || break; done

## Level 13
scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
chmod 600 sshkey.private
ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

# Level 14 




