On my new windows pc open terminal as admin. It's set to powershell by default. Update to latest wsl and install Ubuntu by default. 

        wsl.exe --install

Reboot for changes to take effect. After , I am promped to setup a Ubuntu username:first and password:my hearts nickname+middle.

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

I was to sign up to a Ubuntu One account using my x email, full name , username:josephiusx pw: same names as above devided by nonsense. 

Ill have to look into what this is actually for

        https://login.ubuntu.com/

Now I can take a look at my top process (just for the distro I believe)

        top

Now if I close and reopen the terminal I can access my ubuntu profile from the dropdown menu.

        sudo apt update : important before anything else. 
        apt install neofetch
        neofetch

I can run wsl commands from the powershell. Open windows powershell

        pwd
        wsl pwd
wsl is similar but slaches are the other way and its inside a mount directory. its easy enough to access linux via windows shell and windows via linux shells. 

Lets see what other linux distros are available. In Powershell:

        wsl --list --online

lets say I want Kali-linux :

        wsl --install -d kali-linux
Seems reboot wasn't nessessary this time around. After user and pw set info is printed.:

        ┃ This is a minimal installation of Kali Linux, you likely
        ┃ want to install supplementary tools. Learn how:
        ┃ ⇒ https://www.kali.org/docs/troubleshooting/common-minimum-setup/

Updateing wsl (still from windows powershell):

        wsl --update
        wsl --update rollback : undo update
        wsl --shutdown : shuts down instances
Ubuntu is the default. To default to Kali:

        wsl --set-default kali-linux
and of course much much more.... 

Don't forget the vsCode wsl extention. 
A LOT OF INFORMATION ON THAT EXTENTION TO DIGEST!!