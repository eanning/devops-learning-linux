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

## Level 14 
Used cat bandit14 | nc localhost 30000 = view file and send it to local server on that port

## Level 15 
used cat /etc/bandit_pass/bandit15 | openssl s_client -connect localhost:30001 -quiet

## Level 16
Used nmap -p 31000-32000 localhost
opensll s_client -connect localhost 31790

## Level 17 
Used diff passwords.old passwords.new 

## Level 18
Used ssh bandit18@bandit.labs.overthewire.org -p 2220 ls
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme

## Level 19
Used ls -la
./bandit20-do ls /etc/bandit_pass
./bandit20-do cat /etc/bandit_pass/bandit20

## Level 20
echo -n 'GbKksEFF4yrVs6il55v6gwY5aVje5f0j' | nc -l -p 1234 &
./suconnect 1234
