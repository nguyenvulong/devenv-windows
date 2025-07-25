# devenv-windows

## Prerequisites
Make sure `VT-x` or `AMD-V` is enabled in your BIOS/UEFI Settings.

Open PowerShell (`Run as Administrator`)
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
Then restart.
```
wsl.exe --install or wsl.exe --update
wsl --set-default-version 2
```

## Distros
Select and install your Linux distros
```
wsl --list --online # List all available distros
wsl --install -d Debian # Install Debian
wsl --list --all # List all local distros
```

Make sure to remember your Linux username and password.

## Fonts & Colorschemes

Get your nerdfonts [here](https://www.nerdfonts.com/font-downloads)
Open **Terminal** app > **Settings** > **Debian** 

Then at **Additional settings**, select **Appearances** > **Text**

Change colorscheme, font face, and font size as you wish

**Save**.

## Linux Environment
Open the WSL Terminal, access your Linux, and run
```sh
sudo apt update
sudo apt install git
```

Then, follow the tutorial of [devenv-linux](https://github.com/nguyenvulong/devenv-linux). 
Or you can get things running with the followin commands.

```sh
git clone https://github.com/nguyenvulong/devenv-linux.git
cd devenv-linux
chmod +x install.sh
./install.sh
```

And that's about it.

References
- https://learn.microsoft.com/en-us/windows/wsl/install-manual
- https://github.com/nguyenvulong/devenv-linux
- https://github.com/nguyenvulong/devenv-macos



