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
<img width="356" height="55" alt="image" src="https://github.com/user-attachments/assets/ebbce637-8c99-4022-81b5-d111160536f8" />

cat < file2
## OUTPUT
<img width="619" height="77" alt="image" src="https://github.com/user-attachments/assets/6637f3e7-5b05-4f26-8b77-cb3e23f76282" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="480" height="85" alt="image" src="https://github.com/user-attachments/assets/79855671-4859-4e31-97f6-693dfcdf377c" />

comm file1 file2
 ## OUTPUT
<img width="577" height="100" alt="image" src="https://github.com/user-attachments/assets/98cc37f3-50fe-4e15-ab41-23f34dbf7bba" />

diff file1 file2
## OUTPUT
<img width="451" height="179" alt="image" src="https://github.com/user-attachments/assets/b7fd290a-7701-4f09-b651-eb22517fb4e5" />

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
<img width="336" height="101" alt="image" src="https://github.com/user-attachments/assets/62727234-cd11-4ef8-8687-97b73fa8b205" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="416" height="154" alt="image" src="https://github.com/user-attachments/assets/4e5339b8-e6ed-4af2-bb76-542944d501c1" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="339" height="128" alt="image" src="https://github.com/user-attachments/assets/ad31b9d0-ba00-4655-8d0f-1e9c5810e3e6" />

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
<img width="362" height="71" alt="image" src="https://github.com/user-attachments/assets/da23b62a-4347-4133-8cb9-240755cc2d94" />

grep hello newfile 
## OUTPUT
<img width="410" height="95" alt="image" src="https://github.com/user-attachments/assets/b68a8b64-1521-49ba-816f-bec931655b86" />

grep -v hello newfile 
## OUTPUT
<img width="380" height="77" alt="image" src="https://github.com/user-attachments/assets/88eb0370-7254-4ef1-a580-fd5d4c14b2d9" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="411" height="170" alt="image" src="https://github.com/user-attachments/assets/0fdf4e39-ba16-4fc0-8938-2e70466f9164" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="441" height="85" alt="image" src="https://github.com/user-attachments/assets/73722bd4-73e0-4bf5-a038-b54df753f82d" />

grep -R ubuntu /etc
## OUTPUT
<img width="738" height="362" alt="image" src="https://github.com/user-attachments/assets/0332f6d4-0e47-44ec-be3d-49c5be106f98" />

grep -w -n world newfile   
## OUTPUT
<img width="386" height="183" alt="image" src="https://github.com/user-attachments/assets/1081d7bf-31c7-4a82-9d12-3b18b4f8f5d9" />

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
<img width="433" height="150" alt="image" src="https://github.com/user-attachments/assets/478710e5-533f-4655-ab45-79ecbb94aa57" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="415" height="157" alt="image" src="https://github.com/user-attachments/assets/4eb3d530-6fff-402a-a0d2-3a34b0c58873" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="601" height="152" alt="image" src="https://github.com/user-attachments/assets/03a2ff44-0564-49e8-867b-e4746f77f641" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="420" height="122" alt="image" src="https://github.com/user-attachments/assets/21af34ce-5670-439f-ac45-71511e8c4dd6" />

egrep '(world$)' newfile 
## OUTPUT
<img width="461" height="171" alt="image" src="https://github.com/user-attachments/assets/9ba02223-93dd-4827-b021-f7fe9aff6abe" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="528" height="172" alt="image" src="https://github.com/user-attachments/assets/7b3804d0-3d7b-4294-9935-fd86c923560f" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="439" height="79" alt="image" src="https://github.com/user-attachments/assets/ee82709b-063b-48ae-9a93-97ba407af7c1" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="475" height="98" alt="image" src="https://github.com/user-attachments/assets/e174fee2-3241-4031-9dc5-cae907aa5103" />

egrep l{2} newfile
## OUTPUT
<img width="344" height="58" alt="image" src="https://github.com/user-attachments/assets/253ec69e-8abb-4bae-8d5d-8f0351bff091" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="424" height="125" alt="image" src="https://github.com/user-attachments/assets/b8896d22-ac5d-461b-b227-20b34b0aa165" />

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
<img width="405" height="96" alt="image" src="https://github.com/user-attachments/assets/72b291ff-50c6-4143-b38c-06791cbd21e5" />

sed -n -e '$p' file23
## OUTPUT
<img width="336" height="88" alt="image" src="https://github.com/user-attachments/assets/3a68b334-ed82-4c83-9a1d-af2e07ef9a65" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="411" height="178" alt="image" src="https://github.com/user-attachments/assets/50d97d65-894d-4fa4-8f18-15ee2d182ea6" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="412" height="166" alt="image" src="https://github.com/user-attachments/assets/371ba853-1ffd-41af-8d17-5bc96a307896" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="654" height="178" alt="image" src="https://github.com/user-attachments/assets/3b000b8e-3771-4ae4-8a53-463f18185a72" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="413" height="174" alt="image" src="https://github.com/user-attachments/assets/f9e050c8-9bbb-4ad3-ae7a-577a4847e1e2" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="435" height="150" alt="image" src="https://github.com/user-attachments/assets/4666b62e-939f-425e-bfb0-a796aaca543c" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="439" height="119" alt="image" src="https://github.com/user-attachments/assets/c02e6820-1dd3-4d99-ac0a-ea2b897b339a" />

seq 10 
## OUTPUT
<img width="380" height="297" alt="image" src="https://github.com/user-attachments/assets/9b6b39a4-a9b9-423b-800d-fb26f7db03ed" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="348" height="137" alt="image" src="https://github.com/user-attachments/assets/5b7777ae-4c90-41e9-8f1e-4eaeb714b770" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="380" height="148" alt="image" src="https://github.com/user-attachments/assets/5b175f57-9786-4f1e-ba24-9c3aa5f5f80c" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="377" height="149" alt="image" src="https://github.com/user-attachments/assets/06780e35-cb79-4385-831b-1128eb508541" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="316" height="154" alt="image" src="https://github.com/user-attachments/assets/b3444194-1af4-4d37-9f21-7ad83bdd62e5" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="336" height="141" alt="image" src="https://github.com/user-attachments/assets/ba2b3fe3-fee9-460c-9ac9-9834667effcf" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="507" height="154" alt="image" src="https://github.com/user-attachments/assets/24c7f66d-ef52-4cf5-a4be-d4315f0ea862" />

sed -n '2,4{s/$/*/;p}' file23
## OUPPUT
<img width="411" height="144" alt="image" src="https://github.com/user-attachments/assets/73b512fd-8035-4ed6-878e-1e0cd0509b5d" />

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
<img width="377" height="176" alt="image" src="https://github.com/user-attachments/assets/3af4d968-17af-44bc-9cd6-f99a6a5ab83e" />

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
<img width="374" height="173" alt="image" src="https://github.com/user-attachments/assets/7e8e8239-a625-4d2d-9943-25d7d0c2749e" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="516" height="162" alt="image" src="https://github.com/user-attachments/assets/b7098046-b704-4547-99a7-bd5ecb932d61" />

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
<img width="344" height="146" alt="image" src="https://github.com/user-attachments/assets/412035e5-86c9-4b28-8ae2-11630260d04f" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="432" height="117" alt="image" src="https://github.com/user-attachments/assets/b38aa810-61eb-404a-abfa-c68915303008" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="479" height="531" alt="image" src="https://github.com/user-attachments/assets/f52d4254-2ee2-4592-8ac5-c9314ee860a8" />

mkdir backupdir
 
mv backup.tar backupdir
## OUTPUT
<img width="631" height="541" alt="image" src="https://github.com/user-attachments/assets/f4aa0d31-6269-4f75-bd7f-e543823126c1" />

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="659" height="506" alt="image" src="https://github.com/user-attachments/assets/0e953760-5f1d-4dae-b5c7-8962fe8fab46" />

tar -xvf backup.tar
## OUTPUT
<img width="378" height="515" alt="image" src="https://github.com/user-attachments/assets/a72e7ea9-e024-4d22-9b60-c77831132b1c" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="446" height="57" alt="image" src="https://github.com/user-attachments/assets/de03759e-5bf9-4b60-9ad5-c21b30c5d125" />

gunzip backup.tar.gz
## OUTPUT
 <img width="685" height="149" alt="image" src="https://github.com/user-attachments/assets/f00f78c0-ae46-450c-a7f4-7cb7607089af" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="476" height="279" alt="image" src="https://github.com/user-attachments/assets/f1918833-d8f3-463b-8746-2898a89b6add" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="429" height="106" alt="image" src="https://github.com/user-attachments/assets/9d7d3a24-5d8f-438e-94ac-93b56d42b52a" />


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
<img width="542" height="214" alt="image" src="https://github.com/user-attachments/assets/19821f10-7685-43fc-a416-4d474ff596b6" />

 
ls file1
## OUTPUT
<img width="410" height="99" alt="image" src="https://github.com/user-attachments/assets/43b677cd-aa64-41a5-b969-e5bfec5bc1cf" />

echo $?
## OUTPUT 
<img width="311" height="103" alt="image" src="https://github.com/user-attachments/assets/a0fdb4bd-a9c7-4597-bf5a-42dddfcf2d97" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="311" height="103" alt="image" src="https://github.com/user-attachments/assets/4ce71b0e-e6ce-4165-937b-a0b47897cf68" />

abcd
 
echo $?
 ## OUTPUT
<img width="311" height="103" alt="image" src="https://github.com/user-attachments/assets/3fd1345e-1355-4ce8-b2d2-c3a2f846618b" />


 
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
## OUTPUT

<img width="502" height="243" alt="image" src="https://github.com/user-attachments/assets/34d79ab4-2f9f-4e7f-9cbc-bbbba9c28438" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="377" height="112" alt="image" src="https://github.com/user-attachments/assets/99ceaa36-cc07-42f6-bfde-e29289cafd7a" />


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
<img width="705" height="570" alt="image" src="https://github.com/user-attachments/assets/9f544b6b-d8f2-4dae-8b9f-2724305be17b" />

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
![image-61](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/7d9c90af-b7a3-4cf6-8965-40370727248e)



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
![image-62](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/f0646e68-4bbe-4c0e-bf34-7212526995d8)



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

![image-63](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/446feb99-72a9-496c-b9ac-42f9b0e0c6b6)


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

![image-64](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/a2ca4461-3b62-41b0-afa0-eb9523ebc501)


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

![image-65](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/8d68fc65-0b14-4777-af74-cefbc365c662)


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
 ## output

![image-66](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/bf4deead-473f-4b07-b440-bc1e6c3759dd)



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
 
 ## OUTPUT

![image-67](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/bacb7046-9079-489a-acff-43e650c8135d)

 
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
 

## OUTPUT


![image-68](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/34e7fcfa-aa6b-4a1b-a82c-a81ab7997f53)

 
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
 
 ## output:

![image-69](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/33272df2-f5b8-4bda-99f5-5a048690600c)

 
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
 
 ## output

![image-70](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/c51da2ea-8652-49c3-a893-f64acc51d52d)



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

##output

![image-71](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/ef2f1f17-feed-4357-a5a0-e63e33ea14be)




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

![image-72](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/3b304910-6ecf-4fa3-85ea-6dec124f087e)


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

![image-73](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/0a482550-5b9e-4ff8-9e33-54dc8ffa77a5)


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
![image-74](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/d60ca9a2-6750-4f0e-bd8a-bad4b996fbce)


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



$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
## OUTPUT

![image-75](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/978f2ab3-ba04-442a-b668-62aa2450402e)


cat forcontinue.sh 
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

![image-76](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/cd016d47-b62c-4697-8211-2ccbb4e91301)

 
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
![image-77](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/25960989-f3d5-4a74-9eeb-ad4e77ea6755)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT

![image-78](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/33663a39-1b90-46dc-a249-29cce8e18d43)



 
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
![image-79](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/a353a7b2-7b6e-447f-99d8-eff19742bb64)



 
 ./funcex.sh 1 2
 ## output:
![image-80](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/c1b2d17b-036c-4d8b-b615-a4ae510d1db3)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT

![image-81](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/dc93f107-da58-4069-8676-fa8001a53772)

 
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

![image-82](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/e260570a-740d-40d6-b3d0-650cf1e0bfe6)

 
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
![image-85 (copy)](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/22c9f9e9-ae69-4152-9768-0122fe2f2a21)

 
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
 
![image-84](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/538413e2-0bfb-498f-bd90-181bb3e71a69)


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

![image-86](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/736ba1b8-9102-4b04-bf53-666e03ad5961)


# RESULT:
The Commands are executed successfully.

