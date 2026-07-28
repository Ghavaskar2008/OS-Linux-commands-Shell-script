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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/56c30c14-9fbe-459a-9089-e5304aad0ac7" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fd89f0a9-de0d-4b9b-bdf5-f0f7076de303" />

comm file1 file2
 ## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/ab35d79b-bab1-4bba-8d49-57f1d282227e" />

 
diff file1 file2
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/567bbde5-7c16-41ed-8e32-2d0f954acce1" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a5437cf8-2115-433f-a12e-9d62a77c600f" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/20f09b79-32cd-4f50-a5a3-3cffb8d806f3" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/30e6e19b-44f4-40c9-b5cd-23bf459edfce" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/480f9bb6-db70-4607-b81b-71bee5ea65e0" />



grep hello newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fbe743c3-a6b4-4ecd-b9bf-f91868eb45d2" />




grep -v hello newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/46627150-6462-4099-8129-2c922f3ed9a3" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/21de3496-48bf-434e-8e22-b4293a8285ba" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fd827ba0-696d-4fdf-91d1-c3a3f1aa2553" />




grep -R ubuntu /etc
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/00620140-2493-4d22-9c05-42cbd43bd9de" />



grep -w -n world newfile   
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/45ad30f2-6b72-466e-8978-119c103c7229" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c217e70e-fada-4e32-896a-9e87f89477e1" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9d052d10-2034-4bfd-a926-77d4d1ad7726" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a70dec7b-ad47-416a-81f5-bd28b7cab4ab" />



egrep '(world$)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6350a6bb-d1d9-42d7-a0d6-6ecba3b9783e" />



egrep '(World$)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/13c46d70-cf1c-4301-97a2-1de6a7bda257" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/2b59d084-74fd-41cc-a665-7cc41c9e300d" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/7e97af7d-e314-473f-89dc-b29149594cff" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/78f63646-36d9-48f9-82fc-e1803f4537ed" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fdd49b5e-f3b7-4fd4-a9b5-63e6c3d7b407" />


egrep l{2} newfile
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/7d3578a0-8c36-4b60-a84f-ea1a6b9b1e18" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6b48eea3-796f-4032-9e1c-d75facd5d855" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/e524f55a-c8cb-4f1e-8ebe-2773fec12d60" />




sed -n -e '$p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/821db9bf-29d2-4725-a671-906d34c73ef2" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/5739e2a9-a1ea-4266-8215-f8d6e9ae18f7" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/bd79259c-63a6-4175-8a46-16df841fd6ec" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/1e6f0c85-649f-46e8-96c3-b1395eb04720" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/14d9bf54-4155-4cc9-b07a-fe3780a41304" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6d2bcbc1-2ea3-4dc8-b5cb-e1134b7baba3" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9bade399-2ce5-4db5-a697-7730d8c711c5" />



seq 10 
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/8b3acd63-e797-4a7e-a097-522d3c2281ef" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4520c084-6f75-4626-a7d8-f3cceede5f25" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a8027f15-f206-4391-a88f-01ff59194e02" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/ca436fb1-4571-426c-a199-457c93625383" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/15cba869-aaab-443d-ad90-f95086bf8c32" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/aea85226-c1ad-42c1-9ffa-3809a825330d" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/9c9bd90c-fe5f-48fb-9482-7c80a6f291bc" />



sed -n '2,4{s/$/*/;p}' file23
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/43173f29-c6c0-4d67-bae0-d3c9cda1c2fd" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c3ba941d-12f8-4e2a-93ec-15662137ba38" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6af563c9-9e5f-4d9b-a326-efb911779c55" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/180840b1-ad53-4ffe-8b19-ab4e58402db7" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/8f5e51bb-a6f1-4c5b-a28d-fa6e21db7dc4" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/333926a8-d9cf-4afe-8a75-ee97f1a73107" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f1bca336-4aa7-45ad-a7f4-8d73b1765f82" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f27e99b4-cc7e-431e-be80-5e1fe34a723b" />


tar -xvf backup.tar
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fc2a5c56-24b4-4a8b-a28b-0bb4567fb4e8" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/b3884c45-0d9c-4126-ae3f-45bab2848b94" />

gunzip backup.tar.gz
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d7e10a52-2921-4a4e-b090-82ff523a428b" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/03f3e939-53e2-40fa-9840-6a3a10f26308" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a475fe9b-9cb4-4946-a8ae-235528f6fce1" />

 
ls file1
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/a3001c1e-7e67-4ea7-be2c-8022237bab49" />

echo $?
## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/5e570d85-693f-4e1d-9a27-70e680af21eb" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/cc276edc-de08-4d1b-8a18-9295b9a1e3cf" />


abcd
 
echo $?
 ## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/58be4653-d150-4ed7-9de6-21f35abbdf0e" />


 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/f788a603-c637-48f6-83bf-793bffdbf8ec" />



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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/5d6b683c-a4fa-40d0-bdad-8b5495c0ec6d" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c877fff6-5ad9-446f-aa46-abae0bb50f0d" />



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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/8bbc6aab-8c8b-423d-9c41-7cb2e4a59936" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/90f47e5e-1754-464c-93f7-2b3268b05108" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/0faa7d17-bcd8-4eb9-a20f-54ba73440805" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/09aa2440-a52e-443d-a51b-2d4b7efa6a38" />

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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4421aaa1-95b4-48ce-9f48-186164899428" />


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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4f4d72f1-73c9-456e-a7f1-c13b28f1f026" />



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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/189cb902-abf6-4de5-96fa-dfc629f431c3" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d958b53e-4b40-42d3-94e8-bc31b2e1ab30" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/fa43529c-62e6-4eba-9920-6df662612a9e" />


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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4ace258f-3aae-469c-b868-9e6b3bb77910" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/e4ca6630-1525-43aa-93ad-62e9a74f1d08" />


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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/cd212a03-fcb5-4668-ad75-afdc1b38241a" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/835cf890-bcf9-42b2-8658-858d1e5ec2ef" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/23f7c3fb-bcc9-4eee-aed1-e35c124f2e59" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/b732e75b-6bb6-4128-81c4-bc0ee4f1aaa7" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/5f963c66-8ad3-4206-be6d-7b907151e926" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/b0bed0c5-b276-40af-a90b-861eebe4813f" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/70a7e2e2-ed9e-4f4e-a174-9d6a3638edc6" />



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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/4df4efcc-7c51-467e-b4f1-4316be86cc37" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/908b159b-0094-420f-b4b9-25e70dded946" />


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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/d33a06a5-73b8-46c3-a099-5265b2687542" />


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

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/6b6bbd77-8784-47db-9451-189b7f7f27a0" />

 
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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/c9627697-d667-484a-a1b7-f80373d36b04" />


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
<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/32f7f797-1a06-4c25-900f-885817d8777e" />


# RESULT:
The Commands are executed successfully.
