# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="492" height="93" alt="image" src="https://github.com/user-attachments/assets/481fd1e4-4944-4252-af61-63d9fdd0709c" />
cat < file2
## OUTPUT
<img width="492" height="36" alt="image" src="https://github.com/user-attachments/assets/b61c0f1c-c76f-4919-b072-5b8aa67a6143" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="492" height="36" alt="image" src="https://github.com/user-attachments/assets/5716d4e4-497c-44d6-b923-48b7b060b173" /> 

comm file1 file2
## OUTPUT
<img width="492" height="165" alt="image" src="https://github.com/user-attachments/assets/a512dd73-45c7-49d5-8586-d92e5067eec6" />

diff file1 file2
## OUTPUT
<img width="492" height="238" alt="image" src="https://github.com/user-attachments/assets/c84b981e-671e-4efb-ab3e-e39def235fb6" />
#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
cut -c1-3 file11
## OUTPUT
<img width="492" height="77" alt="image" src="https://github.com/user-attachments/assets/e79363c8-49c3-4f16-a8d6-6c9a3597b712" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="669" height="147" alt="image" src="https://github.com/user-attachments/assets/ac177dc8-ecf3-495e-97ca-8a790a2b1a1f" />

cut -d "|" -f 2 file22
## OUTPUT

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
<img width="546" height="59" alt="image" src="https://github.com/user-attachments/assets/19b8dade-1e07-4131-bf19-d2969aafb14d" />
grep hello newfile 
## OUTPUT
grep -v hello newfile 
## OUTPUT
<img width="546" height="59" alt="image" src="https://github.com/user-attachments/assets/8750c7b5-2fd5-40f3-a15d-b6da60665b83" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="603" height="81" alt="image" src="https://github.com/user-attachments/assets/52bf4013-f362-47ea-8c67-876681ecc8d9" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="635" height="62" alt="image" src="https://github.com/user-attachments/assets/8846717f-78c0-4583-a432-e9c71073ea13" />
grep -R ubuntu /etc
## OUTPUT
<img width="1199" height="465" alt="image" src="https://github.com/user-attachments/assets/81478f36-cc1e-4927-a470-9a5c84600243" />
grep -w -n world newfile   
## OUTPUT
<img width="620" height="61" alt="image" src="https://github.com/user-attachments/assets/d0df10c7-57cd-4cf0-940f-c5f3ee640ceb" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="628" height="59" alt="image" src="https://github.com/user-attachments/assets/d002fee0-3629-43db-8bf7-0824f992ab6b" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="676" height="58" alt="image" src="https://github.com/user-attachments/assets/722ccf1d-9a8a-44b5-8fb7-e41e1701edf0" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="628" height="59" alt="image" src="https://github.com/user-attachments/assets/04e54d86-90ef-4cdd-ab32-31d0298285fe" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="628" height="59" alt="image" src="https://github.com/user-attachments/assets/efcf9e18-7616-4552-81f4-d39985c937ed" />

egrep '(world$)' newfile 
## OUTPUT
<img width="632" height="79" alt="image" src="https://github.com/user-attachments/assets/6c9581a7-a7db-4e9d-8bef-607793891073" />

egrep '(World$)' newfile 
## OUTPUT
<img width="628" height="59" alt="image" src="https://github.com/user-attachments/assets/78e11e86-ef52-4372-88af-3ad07a618d4b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="631" height="74" alt="image" src="https://github.com/user-attachments/assets/ba2d1259-fd1e-4baf-8714-af849901138a" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="635" height="46" alt="image" src="https://github.com/user-attachments/assets/3f1ebd29-175e-4251-a319-922c9636f0cd" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="635" height="46" alt="image" src="https://github.com/user-attachments/assets/e69681b9-5ab9-4cab-aa50-24fc219b55c0" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="635" height="46" alt="image" src="https://github.com/user-attachments/assets/cac98caf-9e3f-484d-8f11-3cd9b4ae64dd" />


egrep l{2} newfile
## OUTPUT

<img width="637" height="59" alt="image" src="https://github.com/user-attachments/assets/afdb9a7a-4d04-458a-806b-8f99045bab52" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="637" height="82" alt="image" src="https://github.com/user-attachments/assets/ad8a4add-efb5-4eb1-b600-634839089159" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="554" height="44" alt="image" src="https://github.com/user-attachments/assets/e5a1e3ba-812b-46d1-af22-fee0f1c7a6ff" />



sed -n -e '$p' file23
## OUTPUT

<img width="554" height="44" alt="image" src="https://github.com/user-attachments/assets/e674cf27-f580-4fc6-a956-2de2d27e523c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="590" height="166" alt="image" src="https://github.com/user-attachments/assets/dc0d1e3a-15b8-4ecc-aaa0-c57372e5bf71" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="590" height="166" alt="image" src="https://github.com/user-attachments/assets/8c46568b-564e-4dce-93f9-43bfb95dbeed" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="619" height="166" alt="image" src="https://github.com/user-attachments/assets/fe0adf54-6d39-4a93-9790-09d8acef6309" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="600" height="114" alt="image" src="https://github.com/user-attachments/assets/93873f8f-5aae-46e6-af1f-f88082163bab" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="604" height="153" alt="image" src="https://github.com/user-attachments/assets/7ae7fff4-45ac-4a5f-b8c3-8eec0c61564a" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="629" height="133" alt="image" src="https://github.com/user-attachments/assets/973fb025-0b16-4116-bf51-ee3f84859f7e" />


seq 10 
## OUTPUT
<img width="618" height="205" alt="image" src="https://github.com/user-attachments/assets/0a993c6d-83fa-4792-b45f-3cfc9823d033" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="632" height="99" alt="image" src="https://github.com/user-attachments/assets/4ab60d7b-f4b1-4f34-b1ab-809b851aa349" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="632" height="99" alt="image" src="https://github.com/user-attachments/assets/1e4d2f60-d8ef-49d7-93ff-6585a8349de8" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="637" height="115" alt="image" src="https://github.com/user-attachments/assets/2cc57cf9-c0d9-44f8-b539-e654cb63379c" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="638" height="98" alt="image" src="https://github.com/user-attachments/assets/37a0d8c5-d9b1-4def-9c0b-81ad03cb1ffc" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="638" height="98" alt="image" src="https://github.com/user-attachments/assets/ea6e2da5-abe2-4c1d-af80-01a9484e669e" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="638" height="98" alt="image" src="https://github.com/user-attachments/assets/d6e66154-1644-4b3c-a147-397f676f9f99" />


sed -n '2,4{s/$/*/;p}' file23

<img width="638" height="98" alt="image" src="https://github.com/user-attachments/assets/c1184d47-32bc-4475-97a1-f9dc5514e23a" />

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="457" height="110" alt="image" src="https://github.com/user-attachments/assets/2f4c6dea-c7cb-496f-9e2e-17e7d2d790bf" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="451" height="117" alt="image" src="https://github.com/user-attachments/assets/285d89b1-b310-4a0a-9058-b244d6ea4b44" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="659" height="188" alt="image" src="https://github.com/user-attachments/assets/c69d2355-0067-451e-bc67-bcc452a31732" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="602" height="154" alt="image" src="https://github.com/user-attachments/assets/51e817cf-3fc8-4b3c-b631-e1d310736bfd" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="677" height="78" alt="image" src="https://github.com/user-attachments/assets/f7a45cf7-8d69-428e-b67d-3350498e1e21" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="808" height="710" alt="image" src="https://github.com/user-attachments/assets/ab740d3c-b61d-42ed-bcdd-9412a86cb3c2" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="808" height="710" alt="image" src="https://github.com/user-attachments/assets/9df25f2e-e99b-4476-ba09-c2eef36241a3" />


tar -xvf backup.tar
## OUTPUT
<img width="810" height="496" alt="image" src="https://github.com/user-attachments/assets/7b150955-0627-4525-8b84-db992c954892" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
