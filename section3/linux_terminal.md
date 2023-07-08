## Create Container
```shell
  # Creating Ubuntu container in INTERACTIVE MODE (without image download)

  docker run -it ubuntu

  # Creating Ubuntu container (with image download)
  docker pull ubuntu
```

## Packages Manager Commands
```shell
  # Update all packages (this command must be run every time you boot with linux)
  apt update

  # List all installed packages
  apt list

  # Install package
  apt install {PACKAGE NAME}

  # Remove package
  apt remove {PACKAGE NAME}
```

## Basic Commands
```shell
  # Show the current user
  whoami

  # Print message
  echo hello

  # Print current dir
  echo $0

  # History of latests commands
  history

  # Clear shell
  clear
```

## Linux File Sistem

* Windows: C:\{PATH}  (ROOT = C:\)
* Linux: /{PATH}      (ROOT = /)

#### Folders of ROOT

* **bin:** binary commands to all of users (ls, cd, cat, ...)
* **dev:** device files
* [see more here](https://www.thegeekstuff.com/2010/09/linux-file-system-structure/)

#### Folders Navigation
```shell
  # List folders and files of current directory
  ls

  ls etc/alternatives

  ls -1 # Vertical list

  ls -l # More info

  ls -a # Show hidden folders

  # Show path of current folder
  pdw

  # Change directory
  cd {DIRECTORY NAME}
  
  cd ../..

  cd ~ # Go to home dir
```

#### Create, Edit or Remove Folders and Files
```shell
  # Create folder (directory)
  mkdir {DIRECTORY NAME}

  # Rename or Move directory
  mv {DIRECTORY NAME} {NEW FORDER NAME}

  # Create file
  touch {FILE NAME} {FILE NAME 2} ... {FILE NAME N}

  # Remove file
  rm {FILE NAME} {FILE NAME 2} ... {FILE NAME N}

  rm example* # Remove everything that starts with "example"

  # Remove directory
  rm -r {DIRECTORY NAME}
```

## Edit files with Nano package
```shell
  # Install nano package
  apt install nano

  # Create file .txt
  nano {FILE NAME}.txt

  # CTRL + O = Save file
  # CTRL + X = Exit

  # Show ALL file content
  cat {FILE NAME}

  cat /etc/debconf.conf

  # Show PART OF file content
  more {FILE NAME}

  more /etc/debconf.conf
```

## Concatenation
```shell
  # Concat content of files
  cat {FILE NAME 1} ... {FILE NAME N} > {FILE NAME WITH CONCATENATIONS}

  echo {TEXT} > {FILE NAME}

  echo hello world > hello.txt
```

## Regex with GREP
```shell
  # Finding word or sentence on the file (regex)
  grep {TEXT} {FILE NAME 1} ... {FILE NAME N}

  grep hello hello.txt
  
  grep hello -i -r . # All of files from current folder

  # See more in https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix
```

## Find Files
```shell
  # Find files from directory (or current directory)
  find {DIRECTORY OR FILE NAME}
  
  find {DIRECTORY OR FILE NAME} -type f # Only files
  
  find {DIRECTORY OR FILE NAME} -type d # Only directories

  find /etc/

  find -type f -name "{FILE NAME}"

  find -type f -name "hel*"
```

## Run multiple commands
```shell
  # Run multiple commands with ";" operator
  mkdir example ; cd example ; echo ok
  
  # Stop if there is an error when executing multiple commands with the "&&" operator
  mkdir example && cd example && echo ok
```

## Process Manager
```shell
  # List process
  ps

  # Simulate process
  sleep {SECONDS} &

  sleep 10 &

  # Kill process
  kill {PROCCESS ID} # The process ID can be obtained from the list of processes ("ps" command)
```

## Users, Groups and Permissions Manager
```shell
  # Create user
  useradd -m {USER NAME}

  # Modify user
  usermod

  # Delete user
  userdel

  # Show users
  cat /etc/passwd

  # Log in with new user
  docker exec -it -u {USER NAME} {CONTAINER ID} bash

  # List user goups
  cat /etc/group

  # View groups of user
  groups {USER NAME}
  
  # Create user group
  groupadd {GROUP NAME}

  # Modify user group
  groupmod

  # Delete user group
  groupdel

  # Add users on group
  usermod --groups {GROUP NAME} {USER NAME}

  # Permissões
  # r = Read
  # w = Write
  # x = Execute

  # Trocar uma permissão
  chmod u+{PERMISSION} {GROUP FILE}.txt
  
  chmod u+x jhon.txt
```
