# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# NAME : GHAVASKAR VR
# REG NO : 212225040093

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
<img width="322" height="175" alt="image" src="https://github.com/user-attachments/assets/898cfe0a-4f4b-4808-b56f-069cd821f7a3" />



cat < file2
## OUTPUT
<img width="360" height="206" alt="image" src="https://github.com/user-attachments/assets/d60e303b-0965-4818-a9d5-4c940a0c4a74" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="437" height="77" alt="image" src="https://github.com/user-attachments/assets/83b06810-dfb9-4913-ad64-218f5221079d" />

comm file1 file2
 ## OUTPUT
<img width="527" height="362" alt="image" src="https://github.com/user-attachments/assets/ff5f862e-e1b0-4337-aa41-77a882e7f5b1" />

 
diff file1 file2
## OUTPUT
<img width="517" height="281" alt="image" src="https://github.com/user-attachments/assets/17339b2b-ed84-460b-92e8-77dc38ceff19" />


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
<img width="312" height="135" alt="image" src="https://github.com/user-attachments/assets/26f9e43e-80a5-4f4d-a89f-78b6acb98bb7" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="390" height="162" alt="image" src="https://github.com/user-attachments/assets/60ed25a9-ed0a-4382-aac8-f949efb35f52" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="427" height="161" alt="image" src="https://github.com/user-attachments/assets/420d6aa5-ca34-425b-840c-999075a1492b" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world

grep hello newfile 
## OUTPUT
<img width="887" height="120" alt="image" src="https://github.com/user-attachments/assets/109316d5-2727-45a2-9030-fb9ad0ae43d5" />




grep -v hello newfile 
## OUTPUT
<img width="307" height="75" alt="image" src="https://github.com/user-attachments/assets/730202d7-be83-4591-93f6-edf1ed09e358" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="407" height="130" alt="image" src="https://github.com/user-attachments/assets/562ee199-422c-4b64-ac57-dfa78b2c5cf8" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="505" height="102" alt="image" src="https://github.com/user-attachments/assets/1804ebc8-b339-4a35-87d1-b4f93c3c7f06" />




grep -R ubuntu /etc
## OUTPUT
<img width="1447" height="801" alt="image" src="https://github.com/user-attachments/assets/d1fa9167-23ba-429b-a1d7-774cd1ddee11" />



grep -w -n world newfile   
## OUTPUT
<img width="402" height="130" alt="image" src="https://github.com/user-attachments/assets/2fde8ba4-e3cb-4b9d-8f46-29fb406d4656" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6630dd7a-d873-4a03-b9ca-6457837225be" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="377" height="132" alt="image" src="https://github.com/user-attachments/assets/19fb380f-839e-403b-9418-04fdb138acc0" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="442" height="130" alt="image" src="https://github.com/user-attachments/assets/17675ffe-086c-4944-a3a0-9c0aeddd28d2" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="352" height="97" alt="image" src="https://github.com/user-attachments/assets/66ff9a2a-d8a7-4be9-b870-f0333c9be579" />



egrep '(world$)' newfile 
## OUTPUT
<img width="417" height="142" alt="image" src="https://github.com/user-attachments/assets/93aa4147-941f-4a2a-82df-420ad4629bdb" />



egrep '(World$)' newfile 
## OUTPUT
<img width="902" height="107" alt="image" src="https://github.com/user-attachments/assets/ef5e2f28-8426-48f6-bd45-9ae12a67f9e2" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="530" height="126" alt="image" src="https://github.com/user-attachments/assets/9604b333-e87b-4616-99f6-21ba0d74ef41" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="928" height="97" alt="image" src="https://github.com/user-attachments/assets/6417e6a6-7f12-4451-a491-5f37a840ecff" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="867" height="97" alt="image" src="https://github.com/user-attachments/assets/87dcb88b-b3ff-4efe-b4e5-fb854659e75c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="867" height="97" alt="image" src="https://github.com/user-attachments/assets/ab201335-33e4-45d9-a735-1c77954b5e80" />


egrep l{2} newfile
## OUTPUT
<img width="907" height="147" alt="image" src="https://github.com/user-attachments/assets/7e814a64-8b19-4b29-927e-1b8b1fbdce90" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="887" height="181" alt="image" src="https://github.com/user-attachments/assets/2d248771-5cfa-49b1-bd29-fb300bfa0ae3" />


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
<img width="440" height="112" alt="image" src="https://github.com/user-attachments/assets/686e33cb-4415-4c39-979f-1f0cac7b450c" />




sed -n -e '$p' file23
## OUTPUT
<img width="895" height="83" alt="image" src="https://github.com/user-attachments/assets/fd147958-ec54-4e01-b6e6-6c3538924485" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="507" height="311" alt="image" src="https://github.com/user-attachments/assets/76b15684-6c10-4f6a-9cef-480694aa6033" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="412" height="290" alt="image" src="https://github.com/user-attachments/assets/f4de5a7b-fa99-4b55-b613-f780de61c624" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="461" height="310" alt="image" src="https://github.com/user-attachments/assets/807b1001-34d8-44b3-8cd9-c515b49e8482" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="351" height="215" alt="image" src="https://github.com/user-attachments/assets/4eb64eb9-22da-46c2-86b1-ed91e23505bd" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="425" height="162" alt="image" src="https://github.com/user-attachments/assets/98a5e63a-7f9b-4b39-b89e-c73e502051b7" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="547" height="130" alt="image" src="https://github.com/user-attachments/assets/d32bbddf-d559-4768-9fa1-6ff483eeb3c1" />



seq 10 
## OUTPUT
<img width="497" height="347" alt="image" src="https://github.com/user-attachments/assets/43062cfc-a2ff-49cc-979f-ad3290800d5e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="395" height="147" alt="image" src="https://github.com/user-attachments/assets/b97df233-ff40-4117-9de2-1671a28862c3" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="487" height="157" alt="image" src="https://github.com/user-attachments/assets/24b130a2-6990-41f1-90cc-9e244f39d3e1" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="355" height="180" alt="image" src="https://github.com/user-attachments/assets/cb0623a4-aa14-45f8-904d-2f9b687406de" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="357" height="165" alt="image" src="https://github.com/user-attachments/assets/c7873763-0130-4c8c-9c9a-523face5b4eb" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="377" height="156" alt="image" src="https://github.com/user-attachments/assets/bfffc952-67bb-47ef-b150-7aa28613980a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="432" height="156" alt="image" src="https://github.com/user-attachments/assets/c8bbcddc-4878-471e-949e-0204511b43b3" />



sed -n '2,4{s/$/*/;p}' file23
<img width="440" height="157" alt="image" src="https://github.com/user-attachments/assets/df982c67-f26c-4c38-8c23-24ec149a69bb" />


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
<img width="485" height="202" alt="image" src="https://github.com/user-attachments/assets/5e9f733d-bdeb-494d-9e73-57e4ea89c903" />


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
<img width="450" height="215" alt="image" src="https://github.com/user-attachments/assets/e86e3ace-5498-4994-aeed-8b72a2ecb9fe" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="607" height="300" alt="image" src="https://github.com/user-attachments/assets/dd8dd878-7754-4e17-9463-9ec6fe2e0af9" />

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
<img width="450" height="157" alt="image" src="https://github.com/user-attachments/assets/da6557dd-b8f2-4790-b67c-488650545bc3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="507" height="150" alt="image" src="https://github.com/user-attachments/assets/367602e3-2b13-4098-81b9-79be09e89f87" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="806" height="722" alt="image" src="https://github.com/user-attachments/assets/0136f0df-9ece-4a4e-9e41-5f50afccdd9e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1042" height="750" alt="image" src="https://github.com/user-attachments/assets/2b493a8f-e936-421b-82a0-098efdd2d9c8" />


tar -xvf backup.tar
## OUTPUT
<img width="730" height="750" alt="image" src="https://github.com/user-attachments/assets/7c4d3821-4023-4da9-9613-ab0c1a0f21fe" />

gzip backup.tar
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a113a096-5cc3-432c-ab87-22f286958fe9" />


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
<img width="1012" height="500" alt="image" src="https://github.com/user-attachments/assets/21f34314-6290-4ae8-9de9-d250e5d0de91" />

 
ls file1
## OUTPUT
<img width="405" height="77" alt="image" src="https://github.com/user-attachments/assets/e805fee1-57af-4802-a2ff-e5ecbed19431" />

echo $?
## OUTPUT
<img width="325" height="85" alt="image" src="https://github.com/user-attachments/assets/f91d62d4-38d1-44ef-bfb7-004acfe93b34" />
 
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
<img width="482" height="607" alt="image" src="https://github.com/user-attachments/assets/006c147d-1169-46d1-a5df-db3a6586f1f9" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/982ecdef-52d2-4c5c-9838-2ead232465c7" />



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
<img width="457" height="76" alt="image" src="https://github.com/user-attachments/assets/c8c3705e-058b-414b-8634-2f8ca159eeb8" />

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
<img width="547" height="77" alt="image" src="https://github.com/user-attachments/assets/ccef3fed-8bc7-4dac-bfcf-1350448b9b3a" />



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
<img width="1007" height="136" alt="image" src="https://github.com/user-attachments/assets/645e64e9-3586-4485-9f35-7ada2c6f48bf" />

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
<img width="946" height="127" alt="image" src="https://github.com/user-attachments/assets/b5ed3f65-8acb-44dc-b9ad-1fc0c16d233d" />

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
<img width="971" height="92" alt="image" src="https://github.com/user-attachments/assets/72f3422c-5dc0-4a5c-8d58-9ad1f2e63249" />


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
<img width="1006" height="77" alt="image" src="https://github.com/user-attachments/assets/c7930a21-cd22-4c12-9e76-7741b67b43ec" />

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
## OUTPUT
<img width="1052" height="285" alt="image" src="https://github.com/user-attachments/assets/b2d8c58f-44c2-4a61-bedb-aec888f85285" />


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
## Output

<img width="1002" height="205" alt="image" src="https://github.com/user-attachments/assets/c545a963-36f1-455a-89b2-67c33ca8923a" />



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

## Output

<img width="1002" height="205" alt="image" src="https://github.com/user-attachments/assets/3a7ad15c-aeb1-483f-8a9b-70a8a42f1c7b" />

 
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
<img width="1002" height="205" alt="image" src="https://github.com/user-attachments/assets/93cfc48a-5259-488c-a0da-7da930321b69" />

 
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
<img width="1002" height="205" alt="image" src="https://github.com/user-attachments/assets/c4a78c81-51e1-44b9-9697-fa5e6a9306c8" />


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

<img width="1043" height="287" alt="image" src="https://github.com/user-attachments/assets/f295c872-eba7-4038-82cc-4f0679047e5e" />


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
<img width="1043" height="287" alt="image" src="https://github.com/user-attachments/assets/14542b6b-87e5-478a-bd95-3ea813f6369b" />


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

<img width="1011" height="237" alt="image" src="https://github.com/user-attachments/assets/fd127685-4f61-4ec1-b5dd-1651e7e7019f" />


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
<img width="1045" height="258" alt="image" src="https://github.com/user-attachments/assets/4b4f3093-87f0-445c-8439-abc9ffd8b8a1" />


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
<img width="387" height="477" alt="image" src="https://github.com/user-attachments/assets/6b35ae43-1f6b-4e91-acde-bd269f85442b" />

 
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
<img width="831" height="437" alt="image" src="https://github.com/user-attachments/assets/e0cd7eaa-e5ab-446f-89fd-72efab2b7eeb" />


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
<img width="1022" height="202" alt="image" src="https://github.com/user-attachments/assets/6d76c32f-d55b-4afd-95b8-98b6495f2d30" />


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
<img width="832" height="125" alt="image" src="https://github.com/user-attachments/assets/7a5e7c36-3407-4c84-964b-1c52a5f2ff5b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="831" height="108" alt="image" src="https://github.com/user-attachments/assets/f1a09f35-887f-40ca-b1b3-99a80d8e4dca" />



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
<img width="1022" height="477" alt="image" src="https://github.com/user-attachments/assets/bfdb3987-5dcf-4717-ba35-26c0731daaf4" />

 
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
<img width="547" height="151" alt="image" src="https://github.com/user-attachments/assets/06fc91e7-8df8-4de9-878b-23013cfb941d" />


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

<img width="692" height="141" alt="image" src="https://github.com/user-attachments/assets/f97ade9c-5695-45ff-bd07-a7bbab914856" />


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

<img width="802" height="508" alt="image" src="https://github.com/user-attachments/assets/d7f985bb-0f7c-4ad0-8436-02707c1b8f6d" />

 
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
<img width="982" height="481" alt="image" src="https://github.com/user-attachments/assets/86d6497f-dc52-4773-bcbd-f7fec5b185b2" />


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
<img width="552" height="172" alt="image" src="https://github.com/user-attachments/assets/14cc5cea-3147-4fb2-b766-c8dfaf7ba3a7" />


# RESULT:
The Commands are executed successfully.
