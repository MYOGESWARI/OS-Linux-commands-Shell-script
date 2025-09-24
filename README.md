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

<img width="562" height="151" alt="image" src="https://github.com/user-attachments/assets/fb03e13a-f1f6-431c-88f8-3ad8dfcc2786" />



cat < file2
## OUTPUT

<img width="592" height="167" alt="image" src="https://github.com/user-attachments/assets/e00bcddb-5c09-4dce-93eb-6e5fab019c0c" />


# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="559" height="43" alt="image" src="https://github.com/user-attachments/assets/9f4594e6-4f76-460a-b8c6-e98fdf63bcba" />

comm file1 file2
 ## OUTPUT

<img width="524" height="244" alt="image" src="https://github.com/user-attachments/assets/c15ed44a-b27a-4107-8084-bbe4aebf887a" />

 
diff file1 file2
## OUTPUT

<img width="526" height="244" alt="image" src="https://github.com/user-attachments/assets/9b049804-af66-4093-95d2-df4e3e1633fa" />


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

<img width="508" height="67" alt="image" src="https://github.com/user-attachments/assets/422b414e-04e3-49a3-a8d8-35e9dfb0f3f4" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="562" height="86" alt="image" src="https://github.com/user-attachments/assets/210ff4e3-503e-4bd8-8eda-947128f8de14" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="560" height="85" alt="image" src="https://github.com/user-attachments/assets/7c7a8477-016c-4d8d-8a5d-8d2b64b00af4" />


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

<img width="539" height="44" alt="image" src="https://github.com/user-attachments/assets/c7731a74-1022-4e24-abb5-2338700b48a8" />


grep hello newfile 
## OUTPUT

<img width="530" height="47" alt="image" src="https://github.com/user-attachments/assets/8bbb0b3e-c4aa-456e-82bc-c32ddeb0d830" />



grep -v hello newfile 
## OUTPUT

<img width="552" height="44" alt="image" src="https://github.com/user-attachments/assets/e76f4cea-99d6-4b84-b908-262d3fef9bfa" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="595" height="89" alt="image" src="https://github.com/user-attachments/assets/0283a3b0-6653-4893-824f-4dca3d3ea789" />


cat newfile | grep -i -c "hello"
## OUTPUT


<img width="595" height="89" alt="image" src="https://github.com/user-attachments/assets/2321d799-d953-4536-917f-2b1e506eb5f4" />


grep -R ubuntu /etc
## OUTPUT

<img width="599" height="602" alt="image" src="https://github.com/user-attachments/assets/98dced4e-b51e-478f-a7e9-a19321304867" />


grep -w -n world newfile   
## OUTPUT

<img width="589" height="67" alt="image" src="https://github.com/user-attachments/assets/eee5fc5b-2831-40a0-b639-c81e0c0b8e65" />


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

<img width="600" height="90" alt="image" src="https://github.com/user-attachments/assets/6f6b2730-9231-4feb-a311-d75395901186" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="595" height="86" alt="image" src="https://github.com/user-attachments/assets/1ee770a6-e9a6-4221-aa1a-3727099573c2" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="600" height="89" alt="image" src="https://github.com/user-attachments/assets/5fb1d3e9-2e3e-4928-acd3-18f340fc1ba8" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="587" height="47" alt="image" src="https://github.com/user-attachments/assets/4f6c1d0f-c73d-47af-844a-7f9bc85ff283" />


egrep '(world$)' newfile 
## OUTPUT

<img width="586" height="68" alt="image" src="https://github.com/user-attachments/assets/6e52742b-ef4b-4dd8-a747-182f11a50cb8" />



egrep '(World$)' newfile 
## OUTPUT

<img width="594" height="45" alt="image" src="https://github.com/user-attachments/assets/8abdb582-2a62-40d8-b57c-a3bdb5d48b2a" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="598" height="112" alt="image" src="https://github.com/user-attachments/assets/e8923a3a-7a9d-4daa-91c1-0f0ee69cd7c3" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="573" height="53" alt="image" src="https://github.com/user-attachments/assets/bb3fb208-8f4c-4064-8285-c48dbf97e5a7" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="591" height="72" alt="image" src="https://github.com/user-attachments/assets/663be04d-4c4c-48f8-9eff-371eb7b5834c" />



egrep 'Linux.*World' newfile 
## OUTPUT

<img width="598" height="71" alt="image" src="https://github.com/user-attachments/assets/72841afc-5b22-404a-8267-98382c4dda4e" />

egrep l{2} newfile
## OUTPUT

<img width="536" height="69" alt="image" src="https://github.com/user-attachments/assets/2932b9b2-ecd4-4e2e-b49a-664cf148d71e" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="549" height="41" alt="image" src="https://github.com/user-attachments/assets/4be251d3-0464-430f-9f9c-55a8686ec373" />


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

<img width="569" height="86" alt="image" src="https://github.com/user-attachments/assets/11981c35-bf8a-4174-b1f8-d097e81e9938" />


sed -n -e '$p' file23
## OUTPUT

<img width="553" height="43" alt="image" src="https://github.com/user-attachments/assets/7be4cdd7-9dbb-4fda-97f5-900f11fde195" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="597" height="219" alt="image" src="https://github.com/user-attachments/assets/4e4fc419-a95d-4d5f-98fd-7603653ae9b2" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="593" height="221" alt="image" src="https://github.com/user-attachments/assets/03383b39-80bc-4b0b-9760-1244962c2992" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="596" height="220" alt="image" src="https://github.com/user-attachments/assets/9ff6251e-452e-4926-b447-c4fc0907d4e0" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="571" height="134" alt="image" src="https://github.com/user-attachments/assets/bd5e0020-3ba1-4efe-a1fb-5862478df393" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="594" height="110" alt="image" src="https://github.com/user-attachments/assets/43d0f97b-3c5a-4603-871b-daab4f85d796" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="596" height="93" alt="image" src="https://github.com/user-attachments/assets/247589a2-9829-48f9-b9f4-d2b29c899042" />


seq 10 
## OUTPUT

<img width="407" height="245" alt="image" src="https://github.com/user-attachments/assets/833387b0-22a3-47da-91c2-e75e158901b3" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="559" height="90" alt="image" src="https://github.com/user-attachments/assets/d0a9264d-ce67-4929-b2a1-6f70bb7f5e4d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="575" height="91" alt="image" src="https://github.com/user-attachments/assets/db52da12-0aae-4cac-b6f1-b8207c476337" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="568" height="117" alt="image" src="https://github.com/user-attachments/assets/9d59d0db-937f-43c0-b77c-95c5b5ac4e85" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="559" height="92" alt="image" src="https://github.com/user-attachments/assets/4244cd4a-6e8f-40fd-914a-5269e359a4b1" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="583" height="90" alt="image" src="https://github.com/user-attachments/assets/4413d980-c55e-4399-bc54-9fa750d227ac" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="595" height="111" alt="image" src="https://github.com/user-attachments/assets/e9d515da-57d6-4989-823e-679efdf6632c" />


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

<img width="458" height="134" alt="image" src="https://github.com/user-attachments/assets/998424af-5f19-4472-bdbe-74c39c426823" />


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

<img width="454" height="136" alt="image" src="https://github.com/user-attachments/assets/c857b2f8-4f62-48ce-b2c6-250af70bff2e" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="602" height="223" alt="image" src="https://github.com/user-attachments/assets/36b88228-06e4-4785-a81a-8602b6b4b99d" />

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

<img width="586" height="113" alt="image" src="https://github.com/user-attachments/assets/4e6c8443-cea7-4121-a7a7-8603763d2cdf" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="593" height="118" alt="image" src="https://github.com/user-attachments/assets/e44be66d-3fea-443a-ba28-8ecc6fbd7e1a" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="558" height="200" alt="image" src="https://github.com/user-attachments/assets/ab6fa622-5330-44d4-a405-86b81b3f98f2" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="598" height="226" alt="image" src="https://github.com/user-attachments/assets/77caacbc-959f-4880-a7ac-714e1b0c7150" />

tar -xvf backup.tar
## OUTPUT

<img width="591" height="220" alt="image" src="https://github.com/user-attachments/assets/e1358f88-fc0e-4ab2-afae-b9965f028d1c" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="560" height="48" alt="image" src="https://github.com/user-attachments/assets/77b9cc64-471f-403d-bc77-b76b1199b065" />


 
gunzip backup.tar.gz
## OUTPUT

<img width="606" height="113" alt="image" src="https://github.com/user-attachments/assets/98daee37-230e-4841-8bbc-349366038c22" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="593" height="92" alt="image" src="https://github.com/user-attachments/assets/b0b6a21c-d0d1-46dc-9410-8c020dfdc1b9" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="526" height="87" alt="image" src="https://github.com/user-attachments/assets/03bd2de6-747c-44d7-adb1-5437653ad5a3" />


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

<img width="598" height="353" alt="image" src="https://github.com/user-attachments/assets/6fb59a5f-56f3-40c7-8478-9142e0fb0a1c" />

 
ls file1
## OUTPUT

<img width="434" height="48" alt="image" src="https://github.com/user-attachments/assets/26bcdd67-01b5-49ab-8e40-8a8c511e58a5" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT

 <img width="411" height="44" alt="image" src="https://github.com/user-attachments/assets/873ddcf4-60d8-40ba-9ad8-bbca96372946" />

abcd
 
echo $?
 ## OUTPUT

<img width="427" height="43" alt="image" src="https://github.com/user-attachments/assets/157fc5fd-8b91-4d43-875d-e7c0853a8625" />

 
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

<img width="546" height="162" alt="image" src="https://github.com/user-attachments/assets/8768a792-38a0-4261-9516-b436a92f661e" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="565" height="91" alt="image" src="https://github.com/user-attachments/assets/234a6bf5-272b-4cb3-b117-6de71d174c52" />


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

<img width="565" height="91" alt="image" src="https://github.com/user-attachments/assets/eac52321-3228-42dd-a5d5-9ebcf3b9c23a" />


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

<img width="548" height="135" alt="image" src="https://github.com/user-attachments/assets/3fa509ee-75aa-486b-a65e-2d18f7ff3987" />


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


<img width="554" height="110" alt="image" src="https://github.com/user-attachments/assets/302f6bb3-5b10-41dc-b94e-a45f0326530d" />

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


<img width="555" height="138" alt="image" src="https://github.com/user-attachments/assets/293c4178-d089-4080-a2c8-9cf4335c0e00" />

 
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

<img width="567" height="90" alt="image" src="https://github.com/user-attachments/assets/697b8585-5f3f-431c-a33b-3972b68bab86" />


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

<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/5f2ad90a-88dd-43eb-937a-00418243feea" />



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

<img width="547" height="204" alt="image" src="https://github.com/user-attachments/assets/e1835123-bdc4-4172-bdf7-e074a7811248" />


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

<img width="587" height="218" alt="image" src="https://github.com/user-attachments/assets/0338f0c8-7914-411b-abee-5849eb1e2cec" />

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

<img width="562" height="153" alt="image" src="https://github.com/user-attachments/assets/234a7d42-aa26-4c36-8459-c47f97612dce" />


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
<img width="572" height="155" alt="image" src="https://github.com/user-attachments/assets/92b6779a-a04b-4c8f-98ee-255c6f1a4aa0" />

 
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
<img width="565" height="305" alt="image" src="https://github.com/user-attachments/assets/a2fbda42-26b2-4f76-944e-c362de8a4930" />

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
 <img width="544" height="93" alt="image" src="https://github.com/user-attachments/assets/632079f3-5f05-4076-8948-8a3feec77f04" />

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

<img width="546" height="71" alt="image" src="https://github.com/user-attachments/assets/70411e39-568a-4852-8956-9512d9f1e1cf" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="583" height="179" alt="image" src="https://github.com/user-attachments/assets/15945517-6b8c-4560-b1ae-2a092cc23a11" />


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
<img width="548" height="91" alt="image" src="https://github.com/user-attachments/assets/bc9e0b2a-9687-436c-9ea8-0e74af6bd525" />

<img width="519" height="47" alt="image" src="https://github.com/user-attachments/assets/78744316-0269-4782-8949-ad3ace4e1223" />

 
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
 <img width="570" height="93" alt="image" src="https://github.com/user-attachments/assets/a67f0ad7-9702-4dc0-b051-2d1d35c24f12" />

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
 <img width="571" height="110" alt="image" src="https://github.com/user-attachments/assets/4772da53-ad7d-4b79-8e7b-96c02d25e65a" />

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
 
 <img width="568" height="329" alt="image" src="https://github.com/user-attachments/assets/e4fcff70-d14a-4486-9097-fd6df2b36c6e" />

 
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

<img width="557" height="309" alt="image" src="https://github.com/user-attachments/assets/59d65039-df94-4452-87e3-db3a5fd5e4d0" />

 
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

<img width="582" height="112" alt="image" src="https://github.com/user-attachments/assets/48eb790f-db88-4963-816d-625e117110e1" />


# RESULT:
The Commands are executed successfully.
