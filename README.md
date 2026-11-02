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
<img width="270" height="167" alt="image" src="https://github.com/user-attachments/assets/9083b856-5a5f-4533-99ba-5997c2e60466" />



cat < file2
## OUTPUT

<img width="257" height="172" alt="image" src="https://github.com/user-attachments/assets/92fbd454-79d7-45fa-bdc2-5ccf1b4a83b6" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/3ec71c68-6331-468d-b9d0-c3c7efe8c26c" />

comm file1 file2
 ## OUTPUT
<img width="327" height="282" alt="image" src="https://github.com/user-attachments/assets/62c4db74-0561-4e51-9a06-8743c2755e1a" />

 
diff file1 file2
## OUTPUT
<img width="317" height="317" alt="image" src="https://github.com/user-attachments/assets/aed2abf9-c878-4892-ada0-2cb1edc8f907" />


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


<img width="323" height="143" alt="image" src="https://github.com/user-attachments/assets/15ec8634-1697-4c0a-9558-91372f8ad2c2" />


cut -d "|" -f 1 file22
## OUTPUT


<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/074a533f-5624-4e6a-8ea8-92b0420326ab" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/94b7bcfc-c39b-4177-adea-be149ad6cb88" />


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


<img width="345" height="92" alt="image" src="https://github.com/user-attachments/assets/25e2e9d3-6962-4e18-87f2-be1ddc1e51bb" />

grep hello newfile 
## OUTPUT


<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/ff843fca-4b6a-4dbb-8900-2a3a90ec31b2" />


grep -v hello newfile 
## OUTPUT

<img width="377" height="97" alt="image" src="https://github.com/user-attachments/assets/52a1c417-5779-49d0-99b7-57d7eb340e02" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/feb53ebd-6b33-4e85-b5eb-e401bcb2bf61" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="498" height="77" alt="image" src="https://github.com/user-attachments/assets/030aeefa-f8c9-4907-b8dc-1cdf8a8478d7" />



grep -R ubuntu /etc
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/b3509025-4b78-4f91-aa95-9a7a7772043e" />


grep -w -n world newfile   
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/8aa8cbb1-5934-4765-acf2-d1ad12889d1d" />

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


<img width="461" height="98" alt="image" src="https://github.com/user-attachments/assets/af46831c-f1e7-4be3-ae9c-fe6a88ea539c" />

egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="450" height="90" alt="image" src="https://github.com/user-attachments/assets/073b4ffc-dbfe-4c5b-afad-dbca85c3f777" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/81a41e26-68d1-4f82-82db-96a3de4b9aa6" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="425" height="76" alt="image" src="https://github.com/user-attachments/assets/231761f5-d2aa-40fd-bbaa-6d2c8ddcc315" />



egrep '(world$)' newfile 
## OUTPUT

<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/badfb49b-11a3-45de-b298-e487c3488147" />


egrep '(World$)' newfile 
## OUTPUT

<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/00b5acc7-22ed-4953-b436-beafc7197c69" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="442" height="117" alt="image" src="https://github.com/user-attachments/assets/8ee4b47b-2af7-4987-b379-d7a3ddd50b64" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="368" height="67" alt="image" src="https://github.com/user-attachments/assets/fa9cc143-b9b4-4427-b56f-9d796d511260" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/94bc19b6-b910-4e2b-a488-a0b11eb8f534" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/a30da3d3-cc1c-4cbe-a478-827728f41332" />


egrep l{2} newfile
## OUTPUT


<img width="353" height="92" alt="image" src="https://github.com/user-attachments/assets/3a2c1dc7-ad35-4369-a8d4-9f005ee4246c" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="396" height="120" alt="image" src="https://github.com/user-attachments/assets/9da1a8de-5f12-4a32-bbe0-43e6cfcce2d8" />


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


<img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/2b6cf0bd-5a3b-4b30-bc74-66c6f827af08" />


sed -n -e '$p' file23
## OUTPUT


<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/2baffa56-c1cc-4a9a-a113-0c9d956a4456" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="465" height="251" alt="image" src="https://github.com/user-attachments/assets/8375a375-20cf-4ca1-a097-4444a0b76f62" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/6a159171-2e53-4492-95ca-8f53ff6c669b" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="477" height="250" alt="image" src="https://github.com/user-attachments/assets/b654d151-bdbc-4bff-9e2e-8f9175be897b" />


sed -n -e '1,5p' file23
## OUTPUT



<img width="410" height="163" alt="image" src="https://github.com/user-attachments/assets/3122594d-26f0-4417-8413-1142429222dd" />

sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="428" height="120" alt="image" src="https://github.com/user-attachments/assets/92e28da6-9152-4afc-b8c6-d16a790afdbc" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="486" height="95" alt="image" src="https://github.com/user-attachments/assets/bd55e784-6a15-47b8-a358-8400fb14b993" />


seq 10 
## OUTPUT


<img width="297" height="265" alt="image" src="https://github.com/user-attachments/assets/dd3942ab-4431-49d3-a6c7-124f74ccefc7" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="376" height="113" alt="image" src="https://github.com/user-attachments/assets/b46242db-4741-4b99-8b67-8e200a28c483" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="402" height="115" alt="image" src="https://github.com/user-attachments/assets/8dbdd39f-1e1f-4e48-b728-784f2b0e1cbe" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="400" height="148" alt="image" src="https://github.com/user-attachments/assets/ec401591-6643-4107-8810-2bd5d81408b4" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/847f4560-53ea-4fc6-a738-6ae7f19eaf32" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="407" height="125" alt="image" src="https://github.com/user-attachments/assets/c089e637-694c-4d16-8e72-d07a855f5a6e" />
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="462" height="112" alt="image" src="https://github.com/user-attachments/assets/b81c6cfd-3ba0-443f-a719-36b003747909" />



sed -n '2,4{s/$/*/;p}' file23


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="327" height="177" alt="image" src="https://github.com/user-attachments/assets/08831779-49c8-4a1d-8f5f-898cd7e24b93" />

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

<img width="423" height="150" alt="image" src="https://github.com/user-attachments/assets/8e17cadc-b5b2-4d9a-a082-c23bf9319b85" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="532" height="242" alt="image" src="https://github.com/user-attachments/assets/3719c421-6882-4b80-b9ac-46611772c31e" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="427" height="153" alt="image" src="https://github.com/user-attachments/assets/65d1afeb-db87-4dfe-b972-29b5e1916df5" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/4543677b-103f-4e6d-871a-38f8ba627c9a" />

tar -xvf backup.tar
## OUTPUT
<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/8e74568b-9e8b-4b72-ad93-f8c66250d1ab" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="645" height="305" alt="image" src="https://github.com/user-attachments/assets/3d87a41b-c6eb-446e-9004-a22aa0b2162e" />
 
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

 <img width="438" height="245" alt="image" src="https://github.com/user-attachments/assets/989e5dc9-eaba-4372-a06a-aac1eb3a1c76" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="136" alt="image" src="https://github.com/user-attachments/assets/30bb3c53-cc05-4796-bad8-97c350f57627" />


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

 <img width="503" height="865" alt="image" src="https://github.com/user-attachments/assets/bfbdf819-00c0-43d9-b0a4-1b93e7d8ce20" />

ls file1
## OUTPUT
<img width="633" height="375" alt="image" src="https://github.com/user-attachments/assets/ffc57711-76d8-4676-8074-c021a7a74729" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="247" height="85" alt="image" src="https://github.com/user-attachments/assets/6f5a792c-125f-45c9-965e-3ab5550294ac" />

echo $?
## OUTPUT 
 <img width="220" height="67" alt="image" src="https://github.com/user-attachments/assets/20c58bf1-cb50-4d26-abaf-b2b6d2007e3f" />

abcd
 
echo $?
 ## OUTPUT

<img width="302" height="87" alt="image" src="https://github.com/user-attachments/assets/267bd3ca-ea0d-4169-9e4d-bdd083f30596" />

 
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

<img width="411" height="200" alt="image" src="https://github.com/user-attachments/assets/b97047b4-159c-4a7b-92f8-64af8a4e8b83" />


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
<img width="362" height="111" alt="image" src="https://github.com/user-attachments/assets/57ccc4e0-a464-46cc-96bf-8977740df3a4" />

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

<img width="428" height="90" alt="image" src="https://github.com/user-attachments/assets/31464748-e9dd-4193-a4a3-0c94a7483bdd" />


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
<img width="393" height="127" alt="image" src="https://github.com/user-attachments/assets/721985f1-57ec-4cd5-bb62-2dc8def7e73a" />

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

<img width="422" height="133" alt="image" src="https://github.com/user-attachments/assets/5bbd1ab8-92b2-4da2-9ee6-cca9ba7a1a3a" />

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
<img width="430" height="182" alt="image" src="https://github.com/user-attachments/assets/20b9b542-9535-48c8-91da-b657cdece9c8" />

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
<img width="438" height="110" alt="image" src="https://github.com/user-attachments/assets/36a6cc0a-8717-433e-9bbf-7983c3676141" />


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
<img width="385" height="210" alt="image" src="https://github.com/user-attachments/assets/1fafdc77-57a3-40cd-a5e7-34175f0e4471" />


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
<img width="298" height="71" alt="image" src="https://github.com/user-attachments/assets/8c788e22-787e-4c09-a45d-1ca603d2018b" />

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
<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/65e213ea-bb6c-435c-81ee-8263a5e6ba55" />

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

<img width="392" height="191" alt="image" src="https://github.com/user-attachments/assets/dffcd605-b90f-4939-872c-506b092e8e74" />

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
<img width="437" height="335" alt="image" src="https://github.com/user-attachments/assets/f0c0feaa-d06b-4bc6-9f59-e95784201aac" />

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
 <img width="393" height="142" alt="image" src="https://github.com/user-attachments/assets/da03b024-292b-412b-9223-a8d49e9f2ae7" />

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
<img width="412" height="182" alt="image" src="https://github.com/user-attachments/assets/fd62ab30-dc57-4fb8-98eb-c29f59dd9bc9" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="322" height="97" alt="image" src="https://github.com/user-attachments/assets/5687413a-e9a3-4646-b4ae-fa77fdb635c2" />


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

 <img width="322" height="97" alt="image" src="https://github.com/user-attachments/assets/9c859193-a2d1-44b8-899e-5ab6a9ec0f40" />

 ./funcex.sh 1 2
<img width="376" height="97" alt="image" src="https://github.com/user-attachments/assets/85b28a9b-fcaf-4005-84ed-199c19194daa" />

 
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
 <img width="396" height="143" alt="image" src="https://github.com/user-attachments/assets/0d0bd836-3eb7-41eb-b8c0-588645862a2a" />

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
<img width="405" height="142" alt="image" src="https://github.com/user-attachments/assets/2509a884-aff6-4b22-bbdc-d2d6598b893b" />

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
 
 <img width="407" height="350" alt="image" src="https://github.com/user-attachments/assets/31415b6c-0038-441f-acee-14072c2b22af" />

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
<img width="376" height="65" alt="image" src="https://github.com/user-attachments/assets/47c6f84d-c645-4e11-8491-de946481ffb3" />

 
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
<img width="407" height="138" alt="image" src="https://github.com/user-attachments/assets/b1a9eebb-4151-4a22-8b45-485ef1dc6761" />


# RESULT:
The Commands are executed successfully.
