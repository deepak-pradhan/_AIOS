## Installation ARM : WIP

### [Prerequsites](#) : Met 

* Download and install [F-Droid](https://f-droid.org/)   
  , Open F-Droid:  Search for Termux & Install Termux ( Linux Emulator on Android )     

* Updata & Upgrade pakages
  ```bash
  $ pkg update
  $ pkg upgrade
  ```

  ```bash
  # Required
  $ pkg install python
  $ python -V
    Python 3.11.9
  $ pip -V
    pip 24.2
  $ curl -V
    curl 8.9.1
  
  # Optional: for FS
  # pkg install proot-distro
  # ..
  ```

  ```bash
  $ apt update
  $ apt upgrade
  ```

  ```bash
  # Install TMux
  apt install tmux
  ```

* Git : @TODO


### Build from source[#](https://aios.readthedocs.io/en/latest/get_started/installation.html#build-from-source "Permalink to this heading")

```bash
# Project Folder & V.Envr
# ---
```bash
$ mkdir Projects
$ cd Projects
$ mkdir _AIOS
$ cd _AIOS
$
$ pythom -m venv .venv
$ ls -al
  .
  ..
  .venv


# Prep: Git Enabled
# ---
```

