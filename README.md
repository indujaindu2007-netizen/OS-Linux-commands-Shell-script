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
<img width="454" height="210" alt="Screenshot from 2026-01-31 07-46-02" src="https://github.com/user-attachments/assets/32347995-2488-4f94-8520-54bd4f9b504b" />



cat < file2
## OUTPUT
<img width="333" height="165" alt="Screenshot from 2026-01-31 07-48-55" src="https://github.com/user-attachments/assets/f9024708-fba8-4665-a542-152ddd897f9f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="412" height="84" alt="Screenshot from 2026-01-31 07-49-59" src="https://github.com/user-attachments/assets/ff49e9cc-eb92-451a-9b85-d79b4bd57833" />

comm file1 file2
 ## OUTPUT
<img width="428" height="265" alt="Screenshot from 2026-01-31 07-51-05" src="https://github.com/user-attachments/assets/042f6bb2-3141-48ac-920e-dcf2eb51ce90" />

 
diff file1 file2
## OUTPUT
<img width="428" height="265" alt="Screenshot from 2026-01-31 07-51-37" src="https://github.com/user-attachments/assets/2281ef64-e5d8-49bf-b183-4fdf6cc6f1e9" />


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
<img width="452" height="128" alt="Screenshot from 2026-01-31 08-08-29" src="https://github.com/user-attachments/assets/1b4ac8d1-2daa-4706-9c76-eb4fd20f9d4e" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="459" height="110" alt="Screenshot from 2026-01-31 08-34-21" src="https://github.com/user-attachments/assets/1a9dcaa7-b244-42c1-823a-208242826495" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="452" height="137" alt="Screenshot from 2026-01-31 08-20-46" src="https://github.com/user-attachments/assets/18208778-8a73-4ba2-ae6f-39ef60d3ef5e" />


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
<img width="459" height="110" alt="Screenshot from 2026-01-31 08-43-17" src="https://github.com/user-attachments/assets/2c855430-d74c-4794-bd2b-8fcceeb2ba87" />



grep hello newfile 
## OUTPUT
<img width="459" height="110" alt="Screenshot from 2026-01-31 08-42-56" src="https://github.com/user-attachments/assets/8c414458-0c7b-42e8-9fcb-e5104126150b" />




grep -v hello newfile 
## OUTPUT
<img width="459" height="110" alt="Screenshot from 2026-01-31 08-43-39" src="https://github.com/user-attachments/assets/2344c261-2222-4b95-8796-1b3a98b5c3f3" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="471" height="103" alt="Screenshot from 2026-01-31 08-47-05" src="https://github.com/user-attachments/assets/9df09a6c-004f-466f-82d1-f09012908d53" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="467" height="84" alt="Screenshot from 2026-01-31 08-44-06" src="https://github.com/user-attachments/assets/1f2a9706-8203-4e3d-8112-eb65306411d7" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


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
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-13-14" src="https://github.com/user-attachments/assets/06cc7274-cba0-4d78-bc5b-47d75d14e271" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="471" height="103" alt="Screenshot from 2026-01-31 09-05-50" src="https://github.com/user-attachments/assets/f4378db4-5ed4-4de1-9330-076837c0efda" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="479" height="78" alt="Screenshot from 2026-01-31 09-06-29" src="https://github.com/user-attachments/assets/a06d7a45-9d37-442d-9e6d-39eddae58a2d" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="479" height="78" alt="Screenshot from 2026-01-31 09-06-34" src="https://github.com/user-attachments/assets/fcb81a79-b3e8-4682-bb9d-91945ab3f89a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="479" height="78" alt="Screenshot from 2026-01-31 09-06-52" src="https://github.com/user-attachments/assets/876ecccf-49fd-4ab0-999a-ac29fd65f584" />



egrep '(World$)' newfile 
## OUTPUT
<img width="479" height="78" alt="Screenshot from 2026-01-31 09-07-05" src="https://github.com/user-attachments/assets/1c717b55-21ab-459f-99a6-978f14ade0d4" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-07-30" src="https://github.com/user-attachments/assets/c56ef57b-8f63-4ef9-b6f1-4788454040e9" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-07-43" src="https://github.com/user-attachments/assets/f6608557-9b57-4a3e-b0d2-7439b163c520" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-07-57" src="https://github.com/user-attachments/assets/60ce9888-b783-4625-9188-00aded59e169" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-08-13" src="https://github.com/user-attachments/assets/111338fb-b4b8-4bc6-a9a8-07b0fb31eb02" />


egrep l{2} newfile
## OUTPUT
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-08-32" src="https://github.com/user-attachments/assets/4ba9865f-3078-4098-9d04-24a817dc567b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-08-48" src="https://github.com/user-attachments/assets/66f709ef-b0a9-45d8-b6d0-1ce3298c7229" />


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
<img width="482" height="89" alt="Screenshot from 2026-01-31 09-15-57" src="https://github.com/user-attachments/assets/1d50ed57-72b8-42eb-8588-8ff0994a284d" />



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="490" height="225" alt="Screenshot from 2026-01-31 09-17-48" src="https://github.com/user-attachments/assets/400a449c-230c-4a26-aa31-df82f69df909" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="490" height="225" alt="Screenshot from 2026-01-31 09-18-06" src="https://github.com/user-attachments/assets/130be888-2e24-437b-9415-bc473d49fa57" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="490" height="225" alt="Screenshot from 2026-01-31 09-18-18" src="https://github.com/user-attachments/assets/48d4d673-e8dd-44db-a0d2-78eaf0210011" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="491" height="157" alt="Screenshot from 2026-01-31 09-18-37" src="https://github.com/user-attachments/assets/f74b1f68-a920-4aef-9780-d9b70d6b85c8" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="496" height="114" alt="Screenshot from 2026-01-31 09-18-55" src="https://github.com/user-attachments/assets/1c6cfc43-7a81-4445-bfb3-1e995ad370b6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="502" height="92" alt="Screenshot from 2026-01-31 09-19-09" src="https://github.com/user-attachments/assets/d18a4c89-6240-4588-be69-deb239b6fd05" />



seq 10 
## OUTPUT
<img width="492" height="241" alt="Screenshot from 2026-01-31 09-19-28" src="https://github.com/user-attachments/assets/f13387a5-edda-43fd-9c31-335de32f5b96" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="478" height="95" alt="Screenshot from 2026-01-31 09-19-45" src="https://github.com/user-attachments/assets/19211808-f36d-4b49-8631-39726b5987fd" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="478" height="95" alt="Screenshot from 2026-01-31 09-19-57" src="https://github.com/user-attachments/assets/21bf803c-8b28-46e1-9d51-e275aa4243ab" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="483" height="101" alt="Screenshot from 2026-01-31 09-20-18" src="https://github.com/user-attachments/assets/326ef1e0-3f54-4661-b898-731b13f1fd52" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="483" height="101" alt="Screenshot from 2026-01-31 09-20-33" src="https://github.com/user-attachments/assets/fa481932-6351-4d7d-b72b-772296cfaab3" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="483" height="101" alt="Screenshot from 2026-01-31 09-20-54" src="https://github.com/user-attachments/assets/ae3a5be8-7f34-4244-8751-edc2b9d1e4a8" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="483" height="101" alt="Screenshot from 2026-01-31 09-21-06" src="https://github.com/user-attachments/assets/4de42057-8466-4a56-8896-49718d17a05f" />


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
<img width="327" height="171" alt="Screenshot from 2026-02-01 12-04-07" src="https://github.com/user-attachments/assets/70e7a0e4-dba2-49f3-b5ff-ed651c756bf5" />


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
<img width="327" height="165" alt="Screenshot from 2026-02-01 12-07-05" src="https://github.com/user-attachments/assets/6fb9944a-cb3f-494b-96fc-040d8c93a953" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="522" height="226" alt="Screenshot from 2026-02-01 12-08-19" src="https://github.com/user-attachments/assets/ff13a10f-ecae-4766-8a65-241c9cc0a823" />

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
<img width="510" height="115" alt="Screenshot from 2026-02-01 12-12-00" src="https://github.com/user-attachments/assets/50f01f8e-f6e3-4e74-9be0-8849fc1f6265" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="510" height="115" alt="Screenshot from 2026-02-01 12-11-31" src="https://github.com/user-attachments/assets/9621c099-b366-4d3d-bd09-4881d1de5900" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="964" height="996" alt="Screenshot from 2026-02-01 14-18-43" src="https://github.com/user-attachments/assets/ec377b00-0994-4cf6-9758-1234e62a7e34" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="964" height="996" alt="Screenshot from 2026-02-01 14-18-43" src="https://github.com/user-attachments/assets/ea93b212-b2b8-4786-9fb4-87d8d6732aae" />


tar -xvf backup.tar
## OUTPUT
<img width="1850" height="986" alt="Screenshot from 2026-02-01 14-20-25" src="https://github.com/user-attachments/assets/d8d7051a-5562-43b8-a4cf-e714203c2b40" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="523" height="65" alt="Screenshot from 2026-02-01 22-48-29" src="https://github.com/user-attachments/assets/978c0c41-c88a-4bc6-b5ef-5385bfb2b8ed" />

gunzip backup.tar.gz
## OUTPUT
<img width="807" height="292" alt="Screenshot from 2026-02-01 22-58-01" src="https://github.com/user-attachments/assets/c3bac62c-da2e-4ca9-a1fa-e5250a1446ca" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```

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
<img width="531" height="98" alt="Screenshot from 2026-02-01 23-20-22" src="https://github.com/user-attachments/assets/eabf9f86-f9a8-4a1b-85f3-bbfc21ded67d" />


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
<img width="499" height="150" alt="Screenshot from 2026-02-01 23-25-09" src="https://github.com/user-attachments/assets/51d1fa4f-f3b4-48af-b6e5-aacf0b6ed44e" />

 
ls file1
## OUTPUT
<img width="496" height="80" alt="Screenshot from 2026-02-01 23-25-50" src="https://github.com/user-attachments/assets/9f255044-d1b1-4d29-b909-f7bf59f23302" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="496" height="80" alt="Screenshot from 2026-02-01 23-27-53" src="https://github.com/user-attachments/assets/0e699410-eff3-4362-a001-47ef9d4c14c8" />

echo $?
## OUTPUT 
<img width="441" height="52" alt="Screenshot from 2026-02-01 23-30-46" src="https://github.com/user-attachments/assets/b64cb2f1-3966-466f-8203-64aad7e3a4f2" />

abcd
echo $?
 ## OUTPUT
<img width="465" height="252" alt="Screenshot from 2026-02-01 23-31-14" src="https://github.com/user-attachments/assets/54b8e530-6b69-418c-abe1-ae99c5c6d70c" />


 
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

<img width="517" height="532" alt="Screenshot from 2026-02-01 23-32-37" src="https://github.com/user-attachments/assets/820c4fc6-60fd-4bc3-b98e-7d42753d1cb4" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="654" height="326" alt="image" src="https://github.com/user-attachments/assets/d97951e2-09c6-4446-b715-a97694c38ab0" />


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

<img width="678" height="54" alt="image" src="https://github.com/user-attachments/assets/681347bd-0c7d-4033-93bd-defdbcaa89c1" />



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
