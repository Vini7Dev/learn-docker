## Create Container

```shell
  # Creating Ubuntu container in INTERACTIVE MODE (without image download)

  docker run -it ubuntu

  # Creating Ubuntu container (with image download)
  docker pull ubuntu
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

## Nano Package (text editor)
```shell
  # Install nano package
  apt install nano

  # Create file .txt
  nano {FILE NAME}.txt

  # CTRL + O = Save file
  # CTRL + X = Exit
```
