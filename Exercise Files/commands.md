# Commands

These are the commands used in _Learning Linux Command Line_ from LinkedIn Learning.

## 02_03 - Write commands in a shell at the prompt

`ls`

`ls -l`

`ls`

`list` (invalid command)

`sjhfgasjk` (invalid command)

## 02_04 - Finding help for commands

`man ls`

`ls --help`

`apropos list`

## 02_05 - Helpful keyboard shortcuts in the terminal

`ls -l De` followed by the Tab key

`ls -l Do` followed by the Tab key twice

`ls -l Doc` followed by the Tab key

`a` followed by the Tab key

`clear` (used throughout the course)

## 03_03 - Navigating the file system

`cd ~/Documents/`

`pwd`

`ls`

`cd ExerciseFiles`

`ls`

`ls -R departments/`

`cd departments/hr/policies`

`cd ..`

`cd ..`

`cd hr/policies`

`cd ../../finance/documents`

`cd -`

`cd -`

`cd`

## 03_04 - Finding directory and file information

`ls`

`ls --color=always`

`cd Documents/ExerciseFiles`

`ls -l`

`ls -lh`

`file poems.txt`

`stat poems.txt`

## 03_05 - Create and remove directories

`mkdir newdir`

`ls -l`

`mkdir departments/customerservice`

`mkdir departments/customerservice/documents departments/customerservice/cases departments/customerservice/awards`

`mkdir -p departments/legal/contracts`

`rmdir departments/legal/contracts/`

`rmdir departments/customerservice/`

## 03_06 - Copy, move, and delete files and directories

`cp poems.txt poems2.txt`

`ls`

`cp simple_data.txt departments/hr/employee\ info/`

`ls -lh departments/hr/employee\ info/`

`mv poems2.txt departments/marketing`

`ls departments/marketing/`

`ls`

`mv departments/marketing/poems2.txt departments/marketing/literature.txt`

`ls departments/marketing/`

`mv departments/marketing/literature.txt .`

`ls`

`mv *.txt departments/marketing/`

`ls departments/marketing/`

`mv departments/marketing/* .`

`ls`

`rm literature.txt`

`ls`

`cp poems.txt poems3.txt`

`cp poems.txt poems4.txt`

`ls`

`rm poems?.txt`

`ls`

`rm departments/customerservice/`

`rm -r departments/customerservice/`

## 03_07 - Find files from the command line

`find . -name "poe*"`

`find . -name "*d*"`

`find . -iname "*d*"`

`find ~/Documents -name "*d*"`

## 03_08 - Understand user roles and sudo

`ls /root`

`sudo ls /root`

`sudo ls /root`

`sudo -k`

`sudo -i`

`pwd`

`exit`

## 03_10 - Modify file permissions

`ls`

`bash test.sh`

`ls -l test.sh`

`chmod +x test.sh`

`ls -l test.sh`

`stat test.sh`

`./test.sh`

`chmod 644 test.sh`

`./test.sh`

`bash test.sh`

`cat test.sh`

`chmod u-r test.sh`

`cat test.sh`

`chmod 755 test.sh`

`cat test.sh`

`./test.sh`

`touch newfile`

`ls -l`

`ls -l test.sh`

`nano test.sh`

`sudo chown root test.sh`

`nano test.sh`

`ls -l test.sh`

`sudo chown [username] test.sh` (replace `[username]` with your user name)

`ls -l test.sh`

## 03_11 - Create hard and symbolic links

`ln -s poems.txt writing.txt`

`ls -l`

`cat writing.txt`

`ln poems.txt words.txt`

`ls -l`

## 04_02 - Use pipes to connect commands together

`echo "hello"`

`echo "hello" | wc`

`echo "hello world from the command line" | wc`

## 04_03 - View text files with cat, head, tail, and less

`cat poems.txt`

`head poems.txt`

`tail poems.txt`

`head -n5 poems.txt`

`tail -n3 poems.txt`

`cat -n poems.txt | tail -n5`

`tail -n5 poems.txt | cat -n`

`less poems.txt`

`cat poems.txt | less`

## 04_04 - Search for text in files and streams with grep

`grep "the" poems.txt`

`grep -n "the" poems.txt`

`grep -n "The" poems.txt`

`grep -i "The" poems.txt`

`grep -vi "the" poems.txt`

`grep -E "[hijk]" poems.txt`

`grep -E "\w{6,}" poems.txt`

## 04_05 - Manipulate text with awk, sed, and sort

`cat simple_data.txt`

`awk '{print $2}' simple_data.txt`

`awk '{print $2"\t"$1}' simple_data.txt`

`awk '{print $2"\t"$1}' simple_data.txt | sort -n`

`cat simple_data.txt`

`sed s/Orange/Red/g simple_data.txt`

`cat simple_data.txt`

`sort simple_data.txt`

`sort -k2 -n simple_data.txt`

`cat dupes.txt`

`sort -u dupes.txt`

## 04_06 - Edit text with Vim

`vi`

`vi poems.txt`

## 04_07 - Edit text with nano

`nano`

`nano poems.txt`

## 04_08 - Working with tar and zip archives

`cd ..`

`tar -cvf myfiles.tar ExerciseFiles/`

`ls -l`

`tar -caf myfiles.tar.gz ExerciseFiles/`

`tar -caf myfiles.tar.bz2 ExerciseFiles/`

`ls -lh`

`mkdir unpack1`

`mv myfiles.tar.bz2 unpack1/`

`cd unpack1/`

`tar -xf myfiles.tar.bz2`

`ls -lh`

`cd ..`

`mkdir unpack2`

`tar -xf myfiles.tar.gz -C unpack2`

`zip -r exfiles.zip Exercise\ Files/`

`ls -lh`

`mkdir unpack3`

`mv exfiles.zip unpack3`

`cd unpack3`

`unzip exfiles.zip`

`ls -lh`

`mkdir ../unpack4`

`unzip exfiles.zip -d ../unpack4`

`ls -lh ../unpack4`

## 04_11 - Output redirection

`ls`

`ls 1> filelist.txt`

`cat filelist.txt`

`ls > filelist2.txt`

`cat filelist2.txt`

`ls notreal`

`ls notreal > filelist3.txt`

`ls notreal 2>filelist4.txt`

`cat filelist4.txt`

`>filelist4.txt`

`cat filelist4.txt`

`ls > filelist5.txt`

`echo "some appended text" >> filelist5.txt`

`cat filelist5.txt`

## 04_12 - Exploring environment variables and PATH

`env`

`echo $PATH`

`which ls`

`which less`

`echo $PATH`

`ls -lah`

`nano ~/.bash_profile`

## 05_01 - Find information about your Linux distribution

`ls -l /etc/*release`

`cat /etc/*release`

`uname -a`

## 05_02 - Find system hardware and disk information

`free -h`

`lscpu`

`cat /proc/cpuinfo`

`df -h`

`sudo du -hd1 /`

`sudo lshw | less`

`ip a`

## 05_03 - Install and update software with a package manager

`apt search tree`

`apt show tree`

`tree`

`sudo apt install tree`

`tree Documents/ExerciseFiles`

`man tree`

`sudo apt update`

`sudo apt upgrade`
