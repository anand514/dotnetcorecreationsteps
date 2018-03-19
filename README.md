# dotnetcorecreationsteps
## Linux Mint 17, Linux Mint 18 (64 bit)
## Remove any previous preview versions of .NET Core from your system.
## .NET Core 2.x
## .NET Core 1.x
  Register the Microsoft Product key as trusted.

## bash

Copy
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
Set up the desired version host package feed.

Ubuntu 17.10

bash

Copy
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-artful-prod artful main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-get update
Ubuntu 17.04

bash

Copy
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-zesty-prod zesty main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-get update
Ubuntu 16.04 / Linux Mint 18

bash

Copy
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-xenial-prod xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-get update
Ubuntu 14.04 / Linux Mint 17

bash

Copy
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-trusty-prod trusty main" > /etc/apt/sources.list.d/dotnetdev.list'
sudo apt-get update
Install .NET Core.

bash

Copy
sudo apt-get install dotnet-sdk-2.1.4
Run the dotnet --version command to prove the installation succeeded.

bash

Copy
dotnet --version
