# WGT-Server

## Device Description
Raspberry Pi 5

Operating System: Raspian / Raspberry OS

Folder structure

    main applications /home/~name~/app/wgt-server
    data location /home/~name~/app/data

## Setup Activity:
- Confirmed RPI was updated
    - sudo app-get update
    - sudo apt-get upgrade
      
- Established Remote access
    - SSH - On by default from OS setting

## Setup git folder
    - from /home/~name~/app
    - git clone "http://github.com/kodemeex/wgt-server"

### Test git folder

    - from /home/~name~/app/wgt-server
    - git pull "https://github.com/kodemeex/wgt-server"

## Install PIP
    - in the terminal, type
    - sudo apt install python3-pip
    - after installed, reboot the pi.

## Install gpiozero
    - in the terminal, type
    - pip install gpiozero

## Install Flask
Make sure there was a virtual enviornment

    - from /home/~name~/app
    - in the terminal, type
    - pip install Flask
    - sudo apt install python3-venv  << to install virtual enviornment >>
    - python3 -m venv app << to create the virtual enviornment called app>>
    - . app/bin/activate  << to activate the virtual enviornment >>

## Test Flask
    - from /home/~name~/app
    - in the terminal, type
    - export FLASK_APP=server.py
    - flask run --host=0.0.0.0 --port=5005

    - go to a browser and type,
    - http://~ip address~:5005 << i.e. http://192.168.1.111:5005 or 10.0.0.1:5005 >>
    - the website response should be "Hello, this is the server!"
