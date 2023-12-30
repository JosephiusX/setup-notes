This setup assumes node and yarn are not already installed. If they are we need to uninstall them and restart the computer. 

Navigate to the nvm-windows github and download the desired version. I chose the setup exe file. Run the installer. Test it worked with 

        nvm -v

we shoud get the version number to confirm successful download and setup. 

How it works : 

        nvm list available
        nvm install <version>
        nvm use <version>
        node -v

for linux:

        curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash                                                                    