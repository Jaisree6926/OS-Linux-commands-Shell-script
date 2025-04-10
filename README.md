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



cat < file2
## OUTPUT


# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT

 
diff file1 file2
## OUTPUT


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

<img width="1581" alt="cut-c1-c3file11" src="https://github.com/user-attachments/assets/33499fa8-f8f5-4442-b47e-19d500c99c90" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="1669" alt="cut-d-f1file22" src="https://github.com/user-attachments/assets/f55cd541-7017-43df-8777-0a50467cfb3f" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="1669" alt="cut-d-f2file22" src="https://github.com/user-attachments/assets/eca77afe-8077-40f0-936f-36ee66c96d92" />


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
<img width="1669" alt="grepHello" src="https://github.com/user-attachments/assets/b5c64c1f-492e-4c21-bbf7-d4520b67c4ba" />



grep hello newfile 
## OUTPUT

<img width="1669" alt="grep_hello" src="https://github.com/user-attachments/assets/1e3b5f39-0bc2-4f5e-a29a-b1871018691a" />



grep -v hello newfile 
## OUTPUT

<img width="1669" alt="grep-v" src="https://github.com/user-attachments/assets/6251f364-26a4-432a-920d-25bda63694c3" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="1781" alt="catgrepi" src="https://github.com/user-attachments/assets/a7de0754-2243-417e-a139-2a5bef521ca4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1827" alt="catgrepic" src="https://github.com/user-attachments/assets/7495ca3c-1f3f-490e-8069-aef71e798a25" />



grep -R ubuntu /etc
## OUTPUT

<img width="1039" alt="grep -r ubuntu" src="https://github.com/user-attachments/assets/fd1949b3-916c-41e2-af34-4de87dbd4684" />


grep -w -n world newfile   
## OUTPUT
<img width="1108" alt="grep newworld" src="https://github.com/user-attachments/assets/6d602708-baef-4a4e-bde5-577596a60a5a" />


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

<img width="1172" alt="egrep1" src="https://github.com/user-attachments/assets/f9574e75-3817-4480-bded-dbb06572c3fd" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1172" alt="egrep2" src="https://github.com/user-attachments/assets/83e95c51-c42a-4581-9dda-1520e2b203e6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1191" alt="egrep3" src="https://github.com/user-attachments/assets/1e8c6c11-fdc4-4f03-b30b-7f3fb5fd587b" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="1191" alt="egrep4" src="https://github.com/user-attachments/assets/f9dc924a-c92c-4509-8808-50e58febb55d" />



egrep '(world$)' newfile 
## OUTPUT
<img width="1191" alt="egrep5" src="https://github.com/user-attachments/assets/82c66f14-4052-4380-9057-521b87ccd353" />



egrep '(World$)' newfile 
## OUTPUT
<img width="1191" alt="egrep6" src="https://github.com/user-attachments/assets/6898268a-8687-46f1-9e71-52611121b23a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1191" alt="egrep7" src="https://github.com/user-attachments/assets/087804bb-2821-43d2-afc2-050597161237" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1191" alt="egrep8" src="https://github.com/user-attachments/assets/767abe01-2eae-40dd-aaf0-6a0ac4d042e5" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1191" alt="egrep9" src="https://github.com/user-attachments/assets/49db3d66-0da1-40be-b2da-0bd30cce728a" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1191" alt="egrep10" src="https://github.com/user-attachments/assets/3459bf83-9d9e-45a4-85a6-84172f54c27b" />

egrep l{2} newfile
## OUTPUT

<img width="1191" alt="egrep11" src="https://github.com/user-attachments/assets/bafa4818-8cf5-484e-b357-e8a6a1969dfe" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1191" alt="egrep12" src="https://github.com/user-attachments/assets/7d930fae-3e70-483c-91be-cd14134fdeeb" />

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

<img width="1191" alt="sed1" src="https://github.com/user-attachments/assets/a7f71eef-607f-4191-8d30-6b85a46743e4" />


sed -n -e '$p' file23
## OUTPUT
<img width="1191" alt="sed2" src="https://github.com/user-attachments/assets/c8ee4604-bc0d-46fb-9300-6fb7a0c0d2fc" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed3" src="https://github.com/user-attachments/assets/0b02cb03-2b1c-470e-82e2-defd74241702" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1191" alt="sed4" src="https://github.com/user-attachments/assets/0d1a0c98-e153-45b1-aba4-6eb5ab83bc34" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1191" alt="sed5" src="https://github.com/user-attachments/assets/bd7845e5-116b-4e38-92ce-425ce135ed1c" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="1191" alt="sed6" src="https://github.com/user-attachments/assets/a1bc110c-e558-464f-ac7d-2e1683263d0a" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed7" src="https://github.com/user-attachments/assets/037367f3-c993-46b3-ba07-d159985495ea" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1191" alt="sed8" src="https://github.com/user-attachments/assets/e5672e37-a29e-418c-89da-b116172352c0" />


seq 10 
## OUTPUT

<img width="1191" alt="seq1" src="https://github.com/user-attachments/assets/f02988bd-ef5a-498b-ae90-45e177cdaae2" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1191" alt="seq2" src="https://github.com/user-attachments/assets/39c252cc-de5a-43ae-bd94-2b975a757654" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1191" alt="seq3" src="https://github.com/user-attachments/assets/8be210b0-0eb6-42a3-8501-f0f70bbd76dd" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1191" alt="seq4" src="https://github.com/user-attachments/assets/744a5404-cfc8-4805-bea5-8eacbb2b31e6" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="1191" alt="seq5" src="https://github.com/user-attachments/assets/1192cb8c-e95b-48a3-bf4d-b0e2eeef6969" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1191" alt="seq6" src="https://github.com/user-attachments/assets/60d3bea2-6bec-4ee1-abc7-34c917493574" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1191" alt="seq7" src="https://github.com/user-attachments/assets/e7031b73-b4f9-40c1-9c42-b028e779f6bb" />


sed -n '2,4{s/$/*/;p}' file23
https://github.com/heyitsgautham/OS-Linux-commands-Shell-script/blob/main/img/seq8.png

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
<img width="1191" alt="sort" src="https://github.com/user-attachments/assets/4d578742-2031-4c12-b65c-196e1d96224d" />


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

<img width="1191" alt="uniq" src="https://github.com/user-attachments/assets/8ac5d789-df19-4a26-bcdd-1cdc4ca7c867" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1220" alt="catfile23" src="https://github.com/user-attachments/assets/076137c6-f4b1-4080-a33e-c79dee9a2a00" />

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

<img width="1150" alt="caturl1" src="https://github.com/user-attachments/assets/68d31547-427b-4238-8580-a9a31eb40956" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1262" alt="caturl2" src="https://github.com/user-attachments/assets/98df1772-3849-43ff-ba09-1e81f6a74aea" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="983" alt="tar1" src="https://github.com/user-attachments/assets/e052bff7-def9-4144-bfcb-68ef211e5317" />


mkdir backupdir
 
mv backup.tar backupdir

<img width="983" alt="mv1" src="https://github.com/user-attachments/assets/2b65dc03-f65a-4180-8c2a-78834580ccd4" />

 
tar -tvf backup.tar
## OUTPUT
<img width="983" alt="tar2" src="https://github.com/user-attachments/assets/46b36285-70ba-4405-9733-55152961bf5f" />


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 <img width="983" alt="ls1" src="https://github.com/user-attachments/assets/badeb09d-181f-4667-97e0-dbc3b876bcc3" />

gunzip backup.tar.gz
## OUTPUT

 <img width="1112" alt="ls2" src="https://github.com/user-attachments/assets/192150e9-7975-4398-b236-a60f8f4c415a" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="1303" alt="echo1" src="https://github.com/user-attachments/assets/9f90502d-065f-41ca-8a12-b283759dffd9" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1303" alt="catherecheck" src="https://github.com/user-attachments/assets/f8fca031-4dca-4573-a4dd-d0a94826be24" />


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

 <img width="1303" alt="catscriptcheck" src="https://github.com/user-attachments/assets/6bef0b3b-33c7-4ecd-a399-5c86e65a4ed1" />

ls file1
## OUTPUT
<img width="1303" alt="ls_1" src="https://github.com/user-attachments/assets/b9ec87ce-088b-4749-bcc8-12563a16ec99" />

echo $?
## OUTPUT 

<img width="1303" alt="echo_1" src="https://github.com/user-attachments/assets/a1df15c9-2584-4b29-b169-4325d8f89f8e" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1303" alt="echo_3" src="https://github.com/user-attachments/assets/ae8ec6cd-47bd-42c5-bffe-ea7990da94a5" />

abcd
 
echo $?
 ## OUTPUT

<img width="1303" alt="echo_2" src="https://github.com/user-attachments/assets/ab9568ed-f69c-4e58-a372-4e411a098be2" />

 
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

<img width="1303" alt="cat_Strcmp" src="https://github.com/user-attachments/assets/6c35b396-39ff-43ee-b7d0-7ed1d8cc5ed5" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="1303" alt="strcmp" src="https://github.com/user-attachments/assets/cfecb279-f503-4d86-b866-54973b79466a" />

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
<img width="1303" alt="psswdperm" src="https://github.com/user-attachments/assets/5ae7107a-9431-439a-a0f3-978f9ec389d9" />

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


<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/34bd26ef-b889-44f4-a4ef-565362a9766e" />

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
<img width="1303" alt="iftest" src="https://github.com/user-attachments/assets/ea1cb16a-6dcc-4f1b-9f06-c4302438b440" />

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
<img width="1303" alt="ifnested" src="https://github.com/user-attachments/assets/d05ec7ec-dcdd-4cef-af41-c64c391cc9a4" />

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
<img width="1303" alt="elifcheck" src="https://github.com/user-attachments/assets/5af6afab-1ada-4c42-bbfd-bfc7da658203" />


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
<img width="1303" alt="ifcompound" src="https://github.com/user-attachments/assets/df31df5e-a023-41ef-8804-5261954c0259" />

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
 <img width="1303" alt="casecheck" src="https://github.com/user-attachments/assets/9eb26071-6ba1-42b5-addc-f1990bbaf2e2" />

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
 
 <img width="1303" alt="whiletest" src="https://github.com/user-attachments/assets/8e1af61c-ef0b-46bc-84d5-bec0050120ae" />

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
 
 <img width="1303" alt="untiltest" src="https://github.com/user-attachments/assets/2ee92932-d6a5-4a5f-886d-485c05ac015f" />

 
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
 
 <img width="1303" alt="forin1" src="https://github.com/user-attachments/assets/87d467e8-1f15-4df2-a2c7-ae19aed02811" />

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
 <img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/f29fa399-2cc1-4e75-a8da-dc8faf4e2169" />

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
 <img width="1303" alt="forin2" src="https://github.com/user-attachments/assets/c4844f38-3fc2-4394-bae9-926ef20d668f" />

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

<img width="1303" alt="forin3" src="https://github.com/user-attachments/assets/4ff8473d-ef34-40a2-bc14-e8a2b5bd951a" />

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

<img width="1303" alt="forinfile" src="https://github.com/user-attachments/assets/f4995fb2-a9df-4cac-9514-baab14296108" />

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

<img width="1303" alt="forctype" src="https://github.com/user-attachments/assets/e1530a59-7527-4b0f-a04d-5b44e8ec50a0" />

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
<img width="1303" alt="forctype1" src="https://github.com/user-attachments/assets/0323825f-e7b3-42c9-9d3f-80b8dd5f21f1" />

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
<img width="1303" alt="forneseted1" src="https://github.com/user-attachments/assets/80cae216-7e9b-45f1-ae63-00854326bf5b" />

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

 <img width="1303" alt="forbreak" src="https://github.com/user-attachments/assets/e550d34b-67d0-4e06-a3d8-3b5834fcdedc" />

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
 <img width="1303" alt="forcontinue" src="https://github.com/user-attachments/assets/61b16f1e-9603-4356-b4c3-ecc7d24114db" />

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
 <img width="1303" alt="exread" src="https://github.com/user-attachments/assets/844a409d-c177-49a3-bdcb-eb81af76c984" />

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
<img width="1303" alt="exread1" src="https://github.com/user-attachments/assets/4599fda7-41dd-4e22-bfdb-d69822b7506c" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="1303" alt="exread1" src="https://github.com/user-attachments/assets/40fdda14-376a-4f6b-badc-c8c16064d97a" />


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
<img width="1303" alt="funcex" src="https://github.com/user-attachments/assets/6c041ddc-5ac7-42b0-b431-9f0a5b8f2c16" />

 
 ./funcex.sh 1 2
<img width="1303" alt="funcex123" src="https://github.com/user-attachments/assets/17a3e445-8e2e-43de-a419-3c78be83a51c" />

 
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
 <img width="1303" alt="argshift" src="https://github.com/user-attachments/assets/1939bd9d-2fc1-4789-a0cc-f923835d02e8" />

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

<img width="1303" alt="argshift1" src="https://github.com/user-attachments/assets/9d27df39-7791-4f09-a971-2c0b219ff151" />

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
 
 <img width="1303" alt="argshift3" src="https://github.com/user-attachments/assets/54ad6bce-0971-43e1-8fe7-c3c5d5e2e14e" />

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
<img width="1303" alt="awk" src="https://github.com/user-attachments/assets/efefc03c-27f1-45c3-b921-cef649e712a6" />
 
 
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

<img width="1303" alt="pallindrome" src="https://github.com/user-attachments/assets/3ab35bf8-5a48-4d5f-9a66-fb34b416897f" />

# RESULT:
The Commands are executed successfully.
