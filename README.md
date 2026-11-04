<img width="1016" height="295" alt="image" src="https://github.com/user-attachments/assets/84fd720c-e307-4ff3-b1b0-0f44ef19aa23" /><img width="867" height="95" alt="image" src="https://github.com/user-attachments/assets/76e4198e-68d4-4815-9a52-6d9b22dd33a5" /><img width="690" height="108" alt="image" src="https://github.com/user-attachments/assets/aefbdc58-1e0a-43bf-af68-e1fc09041413" /># OS-Linux-commands-Shell-scripting
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

<img width="458" height="110" alt="Screenshot 2026-10-31 103454" src="https://github.com/user-attachments/assets/d6677571-6f3e-472d-8761-9f692bc5be80" />


cat < file2
## OUTPUT
<img width="490" height="136" alt="Screenshot 2026-10-31 103502" src="https://github.com/user-attachments/assets/d3e50421-c969-4e22-8dc2-31361064fad9" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="505" height="50" alt="Screenshot 2026-10-31 103607" src="https://github.com/user-attachments/assets/b362028d-17db-4bca-933c-1d7f758c6271" />

comm file1 file2
 ## OUTPUT
<img width="505" height="256" alt="Screenshot 2026-10-31 103636" src="https://github.com/user-attachments/assets/5bd5225b-c2d3-4d55-b1d5-8d1f603dc654" />

 
diff file1 file2
## OUTPUT
<img width="537" height="230" alt="Screenshot 2026-10-31 103654" src="https://github.com/user-attachments/assets/a4b4121d-28ee-430d-b0f6-77639306856f" />


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
<img width="525" height="70" alt="Screenshot 2026-10-31 103902" src="https://github.com/user-attachments/assets/9b8ee090-aed9-45de-8750-db5542998ea6" />





cut -d "|" -f 1 file22
## OUTPUT


<img width="611" height="97" alt="Screenshot 2026-10-31 104032" src="https://github.com/user-attachments/assets/a3c82e78-80ec-4490-bb6c-74599951193a" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="610" height="92" alt="Screenshot 2026-10-31 111106" src="https://github.com/user-attachments/assets/ca353258-f03a-4f50-b6d4-c8a0670ae203" />


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
<img width="615" height="50" alt="Screenshot 2026-10-31 111340" src="https://github.com/user-attachments/assets/9e286de5-d7a7-41b3-b218-388ce3773805" />



grep hello newfile 
## OUTPUT
<img width="577" height="47" alt="Screenshot 2026-10-31 111353" src="https://github.com/user-attachments/assets/4f4bc720-f24b-47ed-9099-9d2dcc7dd53d" />




grep -v hello newfile 
## OUTPUT
<img width="675" height="51" alt="Screenshot 2026-10-31 111403" src="https://github.com/user-attachments/assets/1c03777b-777d-4032-b825-489c3fbae870" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="751" height="67" alt="Screenshot 2026-10-31 111410" src="https://github.com/user-attachments/assets/16dc7406-8939-4c22-9a5f-883d93590721" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="805" height="46" alt="Screenshot 2026-10-31 111415" src="https://github.com/user-attachments/assets/c18300e7-b4d1-4754-8c7c-e42b08f7681c" />




grep -R ubuntu /etc
## OUTPUT

<img width="1358" height="108" alt="image" src="https://github.com/user-attachments/assets/35f04ce0-2436-402f-b4b6-8d820a2d0293" />


grep -w -n world newfile   
## OUTPUT
<img width="1912" height="908" alt="image" src="https://github.com/user-attachments/assets/5607465e-0417-4ecc-8b02-edb63faa103c" />


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
<img width="546" height="127" alt="image" src="https://github.com/user-attachments/assets/1bba5bc8-d2e9-4c72-a8e3-e4c6b9e3d429" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="745" height="113" alt="image" src="https://github.com/user-attachments/assets/023821fd-f027-4684-b161-4b6664456d93" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="818" height="110" alt="image" src="https://github.com/user-attachments/assets/0b8c444a-9b68-411f-ab65-ae5d16806d69" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="701" height="87" alt="image" src="https://github.com/user-attachments/assets/bc3f35d1-b994-44d7-bd8b-3ce37d133db4" />


egrep '(world$)' newfile 
## OUTPUT

<img width="690" height="108" alt="image" src="https://github.com/user-attachments/assets/94d6f308-829f-4210-8bf8-dfd7f969a85a" />


egrep '(World$)' newfile 
## OUTPUT
<img width="698" height="87" alt="image" src="https://github.com/user-attachments/assets/1eb9d341-e68c-440a-8eb5-ddd8d726c99a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="801" height="127" alt="image" src="https://github.com/user-attachments/assets/07fc2de3-22f0-485c-9126-a8512437b1b0" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="805" height="90" alt="image" src="https://github.com/user-attachments/assets/1c61a312-26da-4a12-970d-59fa1fdfb79d" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="867" height="95" alt="image" src="https://github.com/user-attachments/assets/0f83ab72-ba6d-486e-bb8d-0fd924b64ee5" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="770" height="90" alt="image" src="https://github.com/user-attachments/assets/d4547e16-4d78-46f5-8786-26328c891fba" />


egrep l{2} newfile
## OUTPUT
<img width="930" height="110" alt="image" src="https://github.com/user-attachments/assets/929dc146-92a8-4546-91e5-5d7b5e9dfe0e" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="842" height="137" alt="image" src="https://github.com/user-attachments/assets/f4032382-ad32-4fd6-af26-db122de066c8" />


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

<img width="691" height="87" alt="image" src="https://github.com/user-attachments/assets/e3d2a5c5-2dad-4039-a329-fe26638383d5" />


sed -n -e '$p' file23
## OUTPUT
<img width="653" height="87" alt="image" src="https://github.com/user-attachments/assets/12df7706-7f34-47da-b1e3-e2e57b969506" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="938" height="247" alt="image" src="https://github.com/user-attachments/assets/d7bc6acd-0817-4f2e-84df-c65b01e5d750" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="803" height="250" alt="image" src="https://github.com/user-attachments/assets/f4a68ce3-1160-42b9-8c49-49f7d80c7df7" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="986" height="247" alt="image" src="https://github.com/user-attachments/assets/7ec915fa-b7a1-4289-a12b-afb96e493bd4" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="827" height="177" alt="image" src="https://github.com/user-attachments/assets/c47c2e4c-6ccb-440b-83b3-f83934cc054d" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="760" height="130" alt="image" src="https://github.com/user-attachments/assets/efaf871e-b4f4-4e02-acb8-97449f6512c7" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="725" height="113" alt="image" src="https://github.com/user-attachments/assets/7b80cba8-74a6-46e0-bea1-c8f04848d423" />



seq 10 
## OUTPUT
<img width="1016" height="295" alt="image" src="https://github.com/user-attachments/assets/5bb68bb8-6294-42c9-b5fb-57093871d03e" />



seq 10 | sed -n '4,6p'
## OUTPUT




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="711" height="128" alt="image" src="https://github.com/user-attachments/assets/e6216e1e-7c4e-478c-b280-6af30cb3c178" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="737" height="150" alt="image" src="https://github.com/user-attachments/assets/9739ae26-a737-49e5-9a2c-871c6c75c22d" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="648" height="137" alt="image" src="https://github.com/user-attachments/assets/c50684c9-d1a5-4010-8992-374be797db0f" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="738" height="135" alt="image" src="https://github.com/user-attachments/assets/de92b56e-11e1-4650-a395-e7a4268ee620" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="740" height="138" alt="image" src="https://github.com/user-attachments/assets/691bee86-72b7-4748-90ba-f73b377d1237" />


sed -n '2,4{s/$/*/;p}' file23
<img width="817" height="137" alt="image" src="https://github.com/user-attachments/assets/a3ee4e8b-73c4-4405-89cd-d091d9c916ef" />


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
<img width="553" height="182" alt="image" src="https://github.com/user-attachments/assets/c2760be7-cff3-4340-adc5-172975f78c86" />


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
<img width="521" height="180" alt="image" src="https://github.com/user-attachments/assets/6f3780c5-b22e-435a-9c82-29b0e20ce7ee" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="758" height="252" alt="image" src="https://github.com/user-attachments/assets/a1db25c8-dd16-4298-9128-35acc990d1b4" />

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
<img width="696" height="138" alt="image" src="https://github.com/user-attachments/assets/946dc300-edf6-41ce-a71c-0509e5f1f84c" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="812" height="132" alt="image" src="https://github.com/user-attachments/assets/7750d643-cd16-4067-9217-8ac687375650" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="962" height="657" alt="image" src="https://github.com/user-attachments/assets/09d10f7c-b522-4824-a8c9-56f36af48cdd" />


mkdir backupdir
 

mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1115" height="733" alt="image" src="https://github.com/user-attachments/assets/266e3fea-64e6-4ccf-8be5-f8bb26367d71" />


tar -xvf backup.tar
## OUTPUT
<img width="958" height="661" alt="image" src="https://github.com/user-attachments/assets/b568d53b-6e7a-4902-ba48-c69ffd9baab2" />


gzip backup.tar

ls .gz
## OUTPUT
 <img width="907" height="83" alt="image" src="https://github.com/user-attachments/assets/2c067ce0-8ef4-4f94-8f17-108fe101593a" />

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
