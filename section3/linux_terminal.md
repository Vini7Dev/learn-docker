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

  # Show path of current folder
  pdw

  # Change directory
  cd {FOLDER NAME}
  
  cd ../..

  cd ~ # Go to home dir
```

#### Create, Edit or Remove Folders and Files

```shell
  # Create folder (directory)
  mkdir {FOLDER NAME}

  # Rename or Move directory
  mv {FOLDER NAME} {NEW FORDER NAME}

  # Create file
  touch {FILE NAME} {FILE NAME 2} ... {FILE NAME N}

  # Remove file
  rm {FILE NAME} {FILE NAME 2} ... {FILE NAME N}

  rm example* # Remove everything that starts with "example"

  # Remove directory
  rm -r {FOLDER NAME}
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

## Nano Package (text editor)
```shell
  # Install nano package
  apt install nano

  # Create file .txt
  nano {FILE NAME}.txt

  # CTRL + O = Save file
  # CTRL + X = Exit
```
