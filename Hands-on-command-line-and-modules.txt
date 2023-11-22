# listing files and directories
ls

ls -a

ls -l

ls -lat

ls -latr

# retriving the current directory:
pwd

# navigating to your $SCRATCH directory
cd $SCRATCH
# checking the current directory
pwd

# creating a new directory (mkdir) with a unique name and changing directory to it (cd):
timestamp=`date "+%F_%H-%M"`; mkdir $HOME/H2HH_$timestamp; cd $HOME/H2HH_$timestamp
# checking the current directory
pwd
# moving out of the directory:
cd ..
# checking the current directory
pwd
# removing the directoy (rmdir)
rmdir $HOME/H2HH_$timestamp
# checking that the directory is gone:
ls $HOME/H2HH_$timestamp

# more than one way to navigate to $HOME:
cd $HOME 
# checking the current directory
pwd
or:
cd ~
# checking the current directory
pwd

# Environmental variables any string preceeded by "$", examples: $HOME, $SCRATCH, $PATH, $LD_LIBRARY_PATH, etc.

# to show the content of a variable use "echo":
echo $HOME

echo $SCRATCH  # Hoffman2-specific

echo $PATH

echo $LD_LIBRARY_PATH

echo $SHELL

# you can define a local variable with, for example:
timestamp=`date "+%F_%H-%M"`
# and check its value with:
echo $timestamp

# "date" is a unix command that reruns the current date, you can format it in various way (see: "man date"):
date

date "+%F_%H-%M"

man date  # (enter "q" to exit the manual display)

# checking hte content of a file (less, more, cat):
less $HOME/.bashrc    

more $HOME/.bashrc  

cat $HOME/.bashrc

head $HOME/.bashrc

head -n 5 $HOME/.bashrc

tail $HOME/.bashrc

tail -n 5 $HOME/.bashrc

tail -f $SGE_ROOT/$SGE_CELL/common/accounting   # Control-C to interrupt


# editing a file (nano, emacs, vi - use nano if not sure):
nano myfile.txt # control X to exit

# what software is available on Hoffman2?
module av --no-pager

# what versions of matlab?
module av matlab

# what versions of python?
module av python

# what versions of R?
module av R

# some modules are not visible under a particular set of compilers loaded; to see all modules:
modules_lookup -a  # this may take a couple of minutes

# to look for a particular application:
modules_lookup -m R

# is R loaded in my environment?
which R

# versions of R under current set of compilers loaded in environment:
module av R

# to see all possible versions:
modules_lookup -m R

# load the latest version (and the companion version of the gcc):
module load gcc/10.2.0; module load R/4.3.0

# what R executable is now in my $PATH?
which R

# start R:
R  # q() to exit 

# which python version is loaded?
which python
python --version


# what modules are loaded?
module av python

# load a particular version of python:
module load python/3.9.2

# check version:
which python
python --version

# using anaconda:
module load anaconda3

# check version of python:
which python
python --version


