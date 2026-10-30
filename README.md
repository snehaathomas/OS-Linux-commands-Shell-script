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
<img width="300" height="89" alt="image" src="https://github.com/user-attachments/assets/de45af52-6362-4b1c-bcf6-97e1d46301a6" />



cat < file2
## OUTPUT
<img width="321" height="135" alt="image" src="https://github.com/user-attachments/assets/68394c80-358b-4d7a-87e4-0f7103399004" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/d5dfac8c-dfd8-4edc-8cf8-a434549f3a94" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/b4dd41d2-ba40-4a45-b2fa-f27990b49783" />

 
diff file1 file2
## OUTPUT
<img width="402" height="248" alt="image" src="https://github.com/user-attachments/assets/25d45a2a-e949-4aa6-8aef-999b4983fda8" />


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




cut -d "|" -f 1 file22
## OUTPUT
<img width="325" height="77" alt="image" src="https://github.com/user-attachments/assets/4767b8c7-6a6f-4d4f-9cfd-64919c55e629" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="367" height="96" alt="image" src="https://github.com/user-attachments/assets/add3e7a0-90ab-46cf-b2c0-dae63dea0878" />

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
<img width="365" height="50" alt="image" src="https://github.com/user-attachments/assets/7745d957-45fa-4ebf-b44c-2930dca88c45" />



grep hello newfile 
## OUTPUT
<img width="366" height="51" alt="image" src="https://github.com/user-attachments/assets/a776a00e-2ad2-452a-bcd1-11504d0d6205" />




grep -v hello newfile 
## OUTPUT
<img width="373" height="57" alt="image" src="https://github.com/user-attachments/assets/e66d46a0-e833-4539-b2c3-1ea2ccd74bb1" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="471" height="72" alt="image" src="https://github.com/user-attachments/assets/fe474a5c-572d-4961-89ee-8449301fb8de" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="491" height="54" alt="image" src="https://github.com/user-attachments/assets/b259c14d-5eb6-4540-8a24-eccecb5170a3" />



grep -R ubuntu /etc
## OUTPUT
<img width="567" height="180" alt="image" src="https://github.com/user-attachments/assets/be160f60-b130-4bac-ac4a-6be9c2b220b8" />



grep -w -n world newfile   
## OUTPUT

<img width="564" height="73" alt="image" src="https://github.com/user-attachments/assets/25b7409a-fb96-4a14-87e1-97f310c992d7" />

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

<img width="533" height="79" alt="image" src="https://github.com/user-attachments/assets/36b06d3d-0857-4806-8823-cee89f0e193b" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="541" height="70" alt="image" src="https://github.com/user-attachments/assets/5ebaf342-1fe3-46f2-8abd-76587e44fb36" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="538" height="75" alt="image" src="https://github.com/user-attachments/assets/ea5d6afb-63f7-4ee1-8c46-683f1f84c872" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="541" height="60" alt="image" src="https://github.com/user-attachments/assets/fe89fcb8-62b9-464c-bf0f-0f59e848e9be" />



egrep '(world$)' newfile 
## OUTPUT
<img width="541" height="54" alt="image" src="https://github.com/user-attachments/assets/482793a6-6ddd-49cd-94e9-bf734d4800fd" />



egrep '(World$)' newfile 
## OUTPUT
<img width="541" height="54" alt="image" src="https://github.com/user-attachments/assets/c540e5c9-6db1-4e42-be96-54429d1da099" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="543" height="75" alt="image" src="https://github.com/user-attachments/assets/17ca0acd-e4da-45ec-8ebc-3bdce2c6966c" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="545" height="57" alt="image" src="https://github.com/user-attachments/assets/a9502bf0-d4a1-4063-a4a0-c998e52d09b7" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="545" height="57" alt="image" src="https://github.com/user-attachments/assets/02514bb3-5af7-4480-8fad-43ff7b3f751d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="545" height="57" alt="image" src="https://github.com/user-attachments/assets/9264df64-5a70-484a-9c00-df71157b9c43" />


egrep l{2} newfile
## OUTPUT
<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/ededa3a2-f9c8-459c-bd00-c5020e81ea46" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="545" height="97" alt="image" src="https://github.com/user-attachments/assets/1a913348-50db-41b2-915e-91dd50320500" />


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
<img width="381" height="52" alt="image" src="https://github.com/user-attachments/assets/08b30a2d-9411-4d4d-b9e7-5cee0a45c69e" />



sed -n -e '$p' file23
## OUTPUT
<img width="428" height="49" alt="image" src="https://github.com/user-attachments/assets/84f43daa-8b11-416d-92d8-98c9d4d639ab" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="424" height="200" alt="image" src="https://github.com/user-attachments/assets/d0310263-a201-4385-9f83-ceec5e9fe32e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="424" height="200" alt="image" src="https://github.com/user-attachments/assets/93976364-21ef-49f7-b08c-bdde10796ff9" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="469" height="203" alt="image" src="https://github.com/user-attachments/assets/df4f8569-854e-4a5a-8fb7-0df5a81056b2" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="470" height="139" alt="image" src="https://github.com/user-attachments/assets/46e6907d-679b-421a-a08c-899d9b4d3929" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="469" height="93" alt="image" src="https://github.com/user-attachments/assets/7533f3da-c781-48b7-b4b0-7340830d2e20" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="468" height="69" alt="image" src="https://github.com/user-attachments/assets/5a915641-b129-49c2-bf4a-b477a3d00c53" />



seq 10 
## OUTPUT
<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/4e71b44a-b07c-413c-8e54-1db14a67c05e" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/5961fdbe-3360-40fd-adbf-521d7954e4d9" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/feacd147-d572-46bb-95e7-f707f1517d67" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/98bc2052-aada-472e-ae04-1cdd91b39ce7" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/2c0275b4-5c31-4a49-8a67-b20f623f44a3" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/c0277abf-4d2b-408d-9959-40548487c174" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/b746208d-5fcd-42ee-ad9e-d7fb4065dc82" />



sed -n '2,4{s/$/*/;p}' file23
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/fac00ebe-e256-4835-9ed6-b9c1ef0096ad" />


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
<img width="310" height="141" alt="image" src="https://github.com/user-attachments/assets/cc54b901-415f-44fb-8bb4-f93e46a7a76b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="565" height="200" alt="image" src="https://github.com/user-attachments/assets/8755dcc3-e795-44a6-bfde-f6761ebd0ca2" />

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
<img width="572" height="95" alt="image" src="https://github.com/user-attachments/assets/00384622-2fc4-4e75-91d2-f84faa3758ae" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="566" height="93" alt="image" src="https://github.com/user-attachments/assets/488eecf9-5e68-4d60-81cb-793e70736a81" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="284" height="116" alt="image" src="https://github.com/user-attachments/assets/30d542e0-f0c9-40a2-91fa-14f97d330c17" />


tar -xvf backup.tar
## OUTPUT
<img width="644" height="140" alt="image" src="https://github.com/user-attachments/assets/33efee16-66aa-4455-b552-d8bfbfb376ce" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="648" height="196" alt="image" src="https://github.com/user-attachments/assets/5a8f15df-082e-40e5-b5a1-7bf8c55dfa97" />

gunzip backup.tar.gz
## OUTPUT
<img width="393" height="140" alt="image" src="https://github.com/user-attachments/assets/cdca5591-90ee-4711-b163-87ee5c51b062" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="651" height="272" alt="image" src="https://github.com/user-attachments/assets/8574f059-8986-46c2-855f-590047a72211" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/d34ced33-a82c-4995-9d73-10d16feaf323" />


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
<img width="430" height="331" alt="image" src="https://github.com/user-attachments/assets/c4543ae7-067c-4011-a1b1-60c6101c6105" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/416ee407-d5c9-455a-9e0e-3bb538d4fdbe" />


echo $?
## OUTPUT 

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/61565881-6286-4151-adba-f3434b7b907b" />
 
abcd
 
echo $?
 ## OUTPUT

<img width="469" height="221" alt="image" src="https://github.com/user-attachments/assets/704d90cc-8bf6-4a1e-8cef-527ceb6af199" />

 
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
<img width="476" height="243" alt="image" src="https://github.com/user-attachments/assets/e87e0503-ec67-4825-8b77-4d6ff0bf21fa" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="605" height="187" alt="image" src="https://github.com/user-attachments/assets/792fab0a-6c4f-4ba6-98c0-3e075bb35c28" />


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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/d52e943d-83a7-4108-b2ff-55e099956712" />

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
<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/e5d3ff39-2f3d-45e6-9fab-093e4133437e" />



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
## OUTPUT
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/7bddc68a-9ed6-4ee4-bd4c-2451219b8519" />

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
## OUTPUT
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/633ae7ba-7f64-499c-903d-c49b3aae50af" />

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
<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/ddde3c12-2557-47e3-b5ca-88cf47546447" />


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
<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/4914476a-8216-443e-8614-e0f2f7661842" />

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
<img width="446" height="201" alt="image" src="https://github.com/user-attachments/assets/fd229792-8c07-4a49-8783-70e5f3a2b27e" />


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
<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/f1818684-dfb5-48e1-b217-81c10ffe7044" />

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
<img width="412" height="201" alt="image" src="https://github.com/user-attachments/assets/bcddb02e-5531-4142-8974-7fe93293b3bb" />

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
<img width="753" height="287" alt="image" src="https://github.com/user-attachments/assets/0003bcd0-ed23-415b-b22d-eee958b73574" />

 
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
<img width="753" height="287" alt="image" src="https://github.com/user-attachments/assets/49d0ab38-c471-4d9b-9fb8-389dbc53a828" />

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
 <img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/88234b50-f442-402a-98ad-c1d9eb1b4f9c" />

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
<img width="481" height="144" alt="image" src="https://github.com/user-attachments/assets/53268cf4-9231-4531-9423-67e7455adfa6" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="774" height="137" alt="image" src="https://github.com/user-attachments/assets/fa42561d-3993-44ac-b6c5-ed564eaad02c" />



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
<img width="755" height="44" alt="image" src="https://github.com/user-attachments/assets/fb5624ab-34a1-4528-beb8-7088c9cab01d" />

 
 ./funcex.sh 1 2
<img width="762" height="38" alt="image" src="https://github.com/user-attachments/assets/6d0d93a7-6b02-4958-8e0e-1954d8600c36" />

 
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
<img width="758" height="63" alt="image" src="https://github.com/user-attachments/assets/421fd7a3-e416-4d6e-82b8-54ebd13acee5" />

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
 <img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/548a7ced-7d7d-4b91-bd54-f1eac5b1d9cc" />

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
 <img width="765" height="327" alt="image" src="https://github.com/user-attachments/assets/0722f884-ff7b-4707-bb7b-ac5bc787df84" />

 
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
 <img width="783" height="218" alt="image" src="https://github.com/user-attachments/assets/7638ec4e-f157-4943-9cc9-d6d34284777b" />

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
<img width="772" height="70" alt="image" src="https://github.com/user-attachments/assets/c224597e-9852-43bd-bd80-ff798c87fe07" />


# RESULT:
The Commands are executed successfully.
