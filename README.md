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
![435988080-8029ac56-7e4d-43a7-9918-bc0b87f8fe44](https://github.com/user-attachments/assets/15f6ee34-f8e8-4199-b937-096ab5b9ccd6)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ cat < file1
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty


cat < file2
## OUTPUT
![435988159-a23101bc-968b-4abb-8fea-55ef8d41458e](https://github.com/user-attachments/assets/0a5545ce-bee1-4ae3-b8c5-19fee7a7cf20)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ cat < file2
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta


# Comparing Files
cmp file1 file2
## OUTPUT
![435988272-33514cdd-ddcd-4ef6-8dda-149c0ed87da1](https://github.com/user-attachments/assets/5b76445e-9979-4c06-9d9b-df1afe9a1c27)

 (base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ cmp file1 file2
file1 file2 differ: byte 1, line 1
comm file1 file2
 ## OUTPUT
 ![435988389-410fdd16-1f43-4a5d-9526-db0fd3326d7e](https://github.com/user-attachments/assets/ebe9e408-ab26-4671-9d6b-78cbb199a577)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ comm file1 file2
	anil aggarwal
	barun sengupta
chanchal singhvi
		c.k. shukla
	lalit chowdury
		s.n. dasgupta
comm: file 2 is not in sorted order
	
sumit chakrobarty
comm: input is not in sorted order
 
diff file1 file2
## OUTPUT
![435988493-9e57fd50-b4f9-4af8-ab7f-9e5f0adf0d39](https://github.com/user-attachments/assets/1da10c27-79df-4487-8519-f13c6a1a5c8b)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ diff file1 file2
1c1,2
< chanchal singhvi
---
> anil aggarwal
> barun sengupta
2a4
> lalit chowdury
4c6
< sumit chakrobarty
---
> 


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
![435988620-32da0433-5f19-48b6-aa72-c888dd8d1afd](https://github.com/user-attachments/assets/d025be30-7001-42dc-a5b6-f5549b1efe8d)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ cut -c1-3 file11
Hel
Thi




cut -d "|" -f 1 file22
## OUTPUT
![435988710-bae9e5d3-8dd8-4630-8b41-099bfa12bab1](https://github.com/user-attachments/assets/1e45e45c-70a9-454b-9d1b-cef046ffdb56)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ cut -d "|" -f 1 file22
1001 
1002 
1003 



cut -d "|" -f 2 file22
## OUTPUT
![435988778-220838aa-a87c-410c-b83a-47ec63e29675](https://github.com/user-attachments/assets/053f310a-4e3c-4dec-8f22-61cf221b72b3)

(base) sec@sec-ThinkPad-E15-Gen-4:~/ramesh_krishnan$ cut -d "|" -f 2 file22
 Ram 
 tom 
 Joe 

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
![435988864-93e85e41-6482-496b-baa3-0da4c1f3ff97](https://github.com/user-attachments/assets/74918ff8-9bd9-47f3-868f-b0db8c6263b6)



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT

![435989372-53cb71c2-f381-40a8-a384-2d19a7d52be4](https://github.com/user-attachments/assets/4e648e4f-21f1-4805-9e14-9d090d3a1912)


cat newfile | grep -i "hello"
## OUTPUT

![435989465-0e443306-1902-4fd8-b7f1-95fc68466c9d](https://github.com/user-attachments/assets/4cd4b819-466d-4b2e-950b-a24f9d404358)



cat newfile | grep -i -c "hello"
## OUTPUT

![435989545-ede9acb2-5076-4da2-8715-7cdb51a2fb9c](https://github.com/user-attachments/assets/b1b5e0db-692f-4d80-bee7-57b9639e704f)



grep -R ubuntu /etc
## OUTPUT
![435989678-bc50fc2d-79f4-4c52-a238-2a0b685b0690](https://github.com/user-attachments/assets/9a2e520d-e460-4b35-ac80-f33a16ff9754)



grep -w -n world newfile   
## OUTPUT

![435989759-7638ecfc-5363-4798-a21e-a877eb877e8f](https://github.com/user-attachments/assets/78ba3c3d-043b-43f7-983e-6937e9bc1522)

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

![435989956-c52199ff-5060-4890-943b-8820b7b6925c](https://github.com/user-attachments/assets/6c798905-c0c3-4d5e-85b1-be04b8920cdb)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![435990036-96a2981e-471b-4577-8cc4-cae3e0ece3c6](https://github.com/user-attachments/assets/2a3ac50e-65bd-4392-b966-f10c9ad403cb)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![435990176-bf8ea764-1454-420d-b840-a1be70002c80](https://github.com/user-attachments/assets/20a2fc6f-a559-431c-9168-ca3a2b9be800)




egrep '(^hello)' newfile 
## OUTPUT

![435990275-0e4dabea-0bed-4883-af25-8f914a7ba353](https://github.com/user-attachments/assets/9e9d1dec-af96-4a79-923a-ce5d94d50c2a)


egrep '(world$)' newfile 
## OUTPUT
![435990405-3c0ece1e-32d3-4b74-a789-c6bc7ce7d353](https://github.com/user-attachments/assets/41231aab-5ed6-44af-9435-101a340cf111)



egrep '(World$)' newfile 
## OUTPUT
![435990521-0ca309ef-91c1-40a9-8d89-fe872470026e](https://github.com/user-attachments/assets/c5a95b6e-48d7-4d28-a1a3-822bba4e9f6d)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![435990653-4599b623-7f25-4352-ab65-b2a47555fecf](https://github.com/user-attachments/assets/d744a30e-3084-48a4-bd4d-93c2c09851a4)


egrep '[1-9]' newfile 
## OUTPUT

![435990781-66702da5-8561-480b-9f51-894e7372527d](https://github.com/user-attachments/assets/cb61d4f0-a79b-4162-b1e0-e24d3801bed7)


egrep 'Linux.*world' newfile 
## OUTPUT
![435991183-0c2e0a52-53b2-4212-a513-3ae5fca32c9c](https://github.com/user-attachments/assets/ecaa5f88-83be-4771-abd3-5da2c34c294e)


egrep 'Linux.*World' newfile 
## OUTPUT
![435991370-3871088c-8e58-4920-8012-d5dca65e6ffd](https://github.com/user-attachments/assets/3b47cf59-3ffb-4707-8df9-720ed8f23dec)


egrep l{2} newfile
## OUTPUT

![435991370-3871088c-8e58-4920-8012-d5dca65e6ffd](https://github.com/user-attachments/assets/e2836a08-60a2-4544-b7b3-74145d329abe)


egrep 's{1,2}' newfile
## OUTPUT 
![435991475-839712c0-8866-4e6e-ad70-d4350affd5f9](https://github.com/user-attachments/assets/10157bfd-0bd0-414e-be9b-84c4a557f226)


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
![435991586-118ff71a-c5be-41bb-b423-2cf1584e748a](https://github.com/user-attachments/assets/67bf87d7-fc79-495a-95bb-981a508e22a1)



sed -n -e '$p' file23
## OUTPUT
![435991666-b60a3812-a734-4847-83d9-ef398460f15f](https://github.com/user-attachments/assets/e1efa2a4-ba62-4e2a-9b8b-aefe9c1fae31)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![435991751-db487fe1-00ad-437d-b472-56abc7964672](https://github.com/user-attachments/assets/21a43261-587e-482e-80a7-4f932fd24156)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![435991849-fec12e86-7b66-4929-802c-72105d23cc1c](https://github.com/user-attachments/assets/03a41438-e72f-4915-9d58-172bde2abff2)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![435992113-8880b8f8-cac7-40f9-bc6a-caf76244839e](https://github.com/user-attachments/assets/705a62a9-f596-4132-818e-f5a7b115f79a)


sed -n -e '1,5p' file23
## OUTPUT

![435992290-5e019337-6d5a-4c9f-b494-8a6d1f4f30d4](https://github.com/user-attachments/assets/41756f29-e20c-466b-b656-99cfee9698d0)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![435992619-7ad10650-d502-4355-acf8-1d9e238b054b](https://github.com/user-attachments/assets/074873c8-5d42-43e8-81bf-fa7066859b83)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![435992717-4b9c1007-4d47-423e-9a1d-90861c6ecc4d](https://github.com/user-attachments/assets/a9fa9182-bc5d-48f7-b71c-4b4fdcfeb133)


seq 10 
## OUTPUT

![435992909-f7da28c4-c498-4441-acee-7899a0af0160](https://github.com/user-attachments/assets/9c70137a-c1f9-4f07-a346-0a1b5470b7b8)


seq 10 | sed -n '4,6p'
## OUTPUT

![435993008-04af3201-e3d3-4c9a-a944-b75d6c1cfdfb](https://github.com/user-attachments/assets/ff81ab65-63b8-437a-b176-c82e04b79d97)


seq 10 | sed -n '2,~4p'
## OUTPUT
![435993151-76038ca0-76b6-48ee-a783-f9876a1fca9e](https://github.com/user-attachments/assets/939010e7-f1ed-4a2b-844b-f77c56be8f5a)



seq 3 | sed '2a hello'
## OUTPUT

![435993250-8ebbcf19-0926-4ea9-8250-f97fe7db21d8](https://github.com/user-attachments/assets/cda59015-760f-4701-a8bf-cafc6ecc6e69)


seq 2 | sed '2i hello'
## OUTPUT
![435993378-66dc5b06-716a-4d6d-beff-d569472da11e](https://github.com/user-attachments/assets/784ca356-4d81-4c47-a3de-8bd9820fd00b)


seq 10 | sed '2,9c hello'
## OUTPUT
![435993510-2241bf16-7cec-4b42-b7e6-f8d123570255](https://github.com/user-attachments/assets/b1bdf375-06d5-494e-900a-bf5a8d5711d4)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![435993660-76f017ef-3e0c-4ce4-ae73-79b0acdc9df1](https://github.com/user-attachments/assets/307b5eba-0739-4563-bb35-2091e1a83ff5)


sed -n '2,4{s/$/*/;p}' file23
![435993830-bbabe181-a9ee-414e-b869-4a5f0e393aa4](https://github.com/user-attachments/assets/a6efdc2b-6f65-4218-80d8-f48e7785ce48)


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


![435994026-410d3f4c-6c39-45ae-8d3f-77c27203390e](https://github.com/user-attachments/assets/98f467cb-7e24-49c8-add7-bb2022ed930d)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![435994163-da018c16-5e8c-467f-ae30-7095b5901456](https://github.com/user-attachments/assets/9edec203-b4e7-433b-bae6-4de430439222)

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

![435994258-e617db96-fce1-436d-9fe0-41f35ed083cc](https://github.com/user-attachments/assets/fdbd65d7-86b3-48db-9dde-024f4a0ab825)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![435994522-bcf83c13-33e3-48fb-90ed-7a55a7b75aa0](https://github.com/user-attachments/assets/73d04279-e778-4582-aed5-a70441c358ad)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image](https://github.com/user-attachments/assets/4401e992-51e1-47d4-962b-d977a35a6dd7)

mkdir backupdir
 
mv backup.tar backupdir
 ![image](https://github.com/user-attachments/assets/b0e2f90e-6dc1-4a52-81db-ac0daa4050ac)

tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/814dbf38-c784-4d95-a0fe-4cf30e58ed15)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/a1247c09-8f8f-41bc-8cae-b07308d204b8)

gzip backup.tar

ls .gz
## OUTPUT
 ![435995798-6181de5f-05bb-4725-8f80-608999f94138](https://github.com/user-attachments/assets/abf4072b-dcbc-457e-9b21-10f6cd1239d2)

gunzip backup.tar.gz
## OUTPUT
![435995878-719b3d0d-18fc-4ed7-9dc5-db698fc8bc0c](https://github.com/user-attachments/assets/b1df7bd7-523b-4dc5-926c-0304bcfb7199)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![435995963-b1348641-2974-42a9-bf03-f3eb66ad7c4c](https://github.com/user-attachments/assets/13aba772-88d6-46e2-b157-d570a5547c9a)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![435996046-84742458-2423-4883-8125-fbdff9904663](https://github.com/user-attachments/assets/f83ed0ed-163c-47b9-aa25-406d126709cd)


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
![435996183-ed0d58ba-6d11-49ce-a525-e8ccd29fee64](https://github.com/user-attachments/assets/9d1b501a-6e16-4de6-a43d-5b681dbc389e)

 
ls file1
## OUTPUT
![435996241-5c9a1a29-9f59-4b3a-abba-c189e817d48c](https://github.com/user-attachments/assets/4a9833f3-4a48-4f47-9163-d59a6d620efe)

echo $?
## OUTPUT 
![435996357-accc7ac1-d2e6-4432-9f19-f564067ea229](https://github.com/user-attachments/assets/4b9b53d1-86b1-497a-8531-70aa2128472e)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![435996457-29ed365e-c001-46cf-86d9-9cb9d2e2b0d4](https://github.com/user-attachments/assets/3e71aef3-668d-45e6-8e56-6c95ddc349a6)

abcd
 
echo $?
 ## OUTPUT
![435996599-b612ffcf-c9bc-4067-8031-9a455df30894](https://github.com/user-attachments/assets/e3f13dcd-6f5e-4c43-9099-f5ceebc003ea)


 
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

![435997022-d9bc106e-0791-4922-9bfd-5805cabfdf40](https://github.com/user-attachments/assets/5621af23-efd4-4ebd-bb04-de0f6bd45edd)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![435999174-22cecc8a-b0ce-461e-919d-30bd1eee22c8](https://github.com/user-attachments/assets/2b0caad3-4bbb-4f00-8934-c00cb902f3fb)


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
![435999264-9e0840f0-393b-44ae-95a7-bff3bbb98824](https://github.com/user-attachments/assets/b4899b5d-7bd6-4bb0-9a8a-6b18a8075087)

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

![435999387-17dd1995-2421-42ac-b5e9-8d36ac5889b9](https://github.com/user-attachments/assets/7e6573e7-a636-4a28-b34c-9653e96ec8e6)


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
![435999772-5d1d4c76-0e62-462f-aeca-f8856ce9bd2a](https://github.com/user-attachments/assets/a0b7a52a-f8b0-4a70-af39-2fff8dff202b)

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
![435999876-704a8138-da04-4e6d-9e7c-d57cebd03f12](https://github.com/user-attachments/assets/ec6568de-89c4-4ba0-ba73-72b5ae188cc4)


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
![435999956-e320f6f7-1d8c-40a6-ae26-22e9bb492693](https://github.com/user-attachments/assets/2402969d-14f2-4416-a09a-16a0ee1b5b6c)

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
 ![436000507-e1e50e41-ca0d-46b4-9511-c19c6c948dfb](https://github.com/user-attachments/assets/fc4169ad-3f7a-4f67-9dea-f614573e9afd)

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
 
 ![436000617-8e9cfc14-5b7b-4a44-9a52-f602265a3b6b](https://github.com/user-attachments/assets/f07e7635-bc8b-4d69-a2d1-553409e7d2ab)

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
 ![436000739-c6276731-bfc0-4923-9395-0174767314ea](https://github.com/user-attachments/assets/cd544ca7-85df-439a-96b7-78418ba10fb2)

 
 
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
 
 ![436000822-21495f41-b787-49c4-866b-c750cd004372](https://github.com/user-attachments/assets/7b97c4bc-2245-4d1b-966b-be3b9abe3837)

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
 ![436000822-21495f41-b787-49c4-866b-c750cd004372](https://github.com/user-attachments/assets/43b51603-17a8-4e98-8281-e8c4058758df)


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
 ![436000944-b110ca89-7bb4-40a2-ae7e-9e955cd5bb8a](https://github.com/user-attachments/assets/8b709bb6-fe3e-41b3-89c2-4ea635b32730)

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
![437660415-2d6442e7-f0b8-4703-b39e-362a2cd2ca95](https://github.com/user-attachments/assets/f879c75b-8209-4ed0-addc-326ec5c75515)

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
![437660397-1a551ddf-899d-4b54-8cdd-9bca556fc323](https://github.com/user-attachments/assets/3fab3135-ecf3-4855-8f55-5c75b11ae389)


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
![437660380-39f1b427-8058-4fa8-86bd-4938e6e93a0c](https://github.com/user-attachments/assets/fc5f40f3-a842-402e-af20-d1c8c92986f3)

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
![437660331-7575775e-8de8-41e3-ac19-4f22ef794827](https://github.com/user-attachments/assets/e5d551cd-5acf-4d84-acdc-0e1c24ca32e7)

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
![437660283-e73bc102-01c6-447b-94ee-628c97afd6f9](https://github.com/user-attachments/assets/3b7be927-19fd-4b6c-bdeb-9e0dbc1e2596)

 
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
![437660213-9c772da4-1d47-4e05-9d64-1f21e7366fb6](https://github.com/user-attachments/assets/51fc8a8c-db4a-4d1d-b95f-7498fbd97599)

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
 ![437660174-ba08a53c-75f2-4d42-8200-b95e96202b60](https://github.com/user-attachments/assets/70bf1441-5f33-4e5e-9994-d29fc7cc9794)

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

![437660166-757cf856-8760-4cad-8015-8ac27cea4c56](https://github.com/user-attachments/assets/1e2e7343-aa68-4def-9427-406a5c1424c0)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![437660153-0d6a0e74-5611-4d24-b5d5-5ce22356c84e](https://github.com/user-attachments/assets/83baa651-f6a3-462b-9ae6-c5cea0185f60)



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
![437660106-82c45f2a-3a14-494a-b82e-64c5711578b2](https://github.com/user-attachments/assets/8b946ff0-3a95-4a80-9b62-e0862ee102ec)

 
 ./funcex.sh 1 2

 ![437660114-a2795737-fd0b-48f0-9f73-3e1a8f79451e](https://github.com/user-attachments/assets/b85ded30-0646-4760-8412-d07c7f35e0b7)

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
![437660087-8c1fadd2-03e3-4340-8ed4-e6fe845f5776](https://github.com/user-attachments/assets/ede4654e-d558-4e9e-bb85-c4e17fa4eb7f)

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
![437660070-5a0ddfc4-b9fa-4d72-8d3e-99452643ed5a](https://github.com/user-attachments/assets/57f6c6f1-253d-4c63-b2fc-84f12fb2038c)

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
![437660062-dcccd7d9-9525-4da4-86fc-eb10879c3e9f](https://github.com/user-attachments/assets/16497103-3958-4a14-b967-52b61ada9713)

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
 ![437660013-dc8f5288-ef79-4ed1-9d80-62c354d4cd33](https://github.com/user-attachments/assets/73c969a8-f397-4c8b-bc3a-132ccddc2fe1)

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
![437659972-c2f94730-818a-4041-b143-a6606c643a94](https://github.com/user-attachments/assets/ad47c95f-f333-406d-91a2-ffd0351cf631)


# RESULT:
The Commands are executed successfully.
