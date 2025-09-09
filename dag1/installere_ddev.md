# Hvordan installere ddev

For å kjøre ddev så trenger man Docker og eventuelt WSL installert

https://docs.ddev.com/en/stable/users/install/docker-installation/

https://docs.ddev.com/en/stable/users/install/ddev-installation/

## Windows


1. Installer WSL med en linux-distribusjon (Ubuntu i dette tilfelle) gjennom powershell (som admin). Du kan alternativt laste ned fra windows store.

        wsl --install -d Ubuntu-24.04

2. Vi anbefaler å bruke Windows Terminal ( kan også finnes i Windows store)
https://learn.microsoft.com/en-us/windows/terminal/install

https://github.com/microsoft/terminal/releases

3. Start opp wsl og konfigurer din linuxdistro (sett brukernavn og passord).

4. Installer docker

  https://docs.docker.com/engine/install/debian/

  Fjern eksisterende pakker for sikkerhets skyld
      
      for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done      

  Installer docker
      
      # Add Docker's official GPG key:
      sudo apt-get update
      sudo apt-get install ca-certificates curl
      sudo install -m 0755 -d /etc/apt/keyrings
      sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
      sudo chmod a+r /etc/apt/keyrings/docker.asc

      # Add the repository to Apt sources:
      echo \
        "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
        $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
        sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
      sudo apt-get update

      # Install docker
       sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

       # Verify docker install

      sudo docker run hello-world

Restart wsl (wsl --shutdown) i powershell

        # Add you user to docker group
        sudo usermod -aG docker your_username


5. Installer ddev

        # Add DDEV’s GPG key to your keyring
        sudo sh -c 'echo ""'
        sudo apt-get update && sudo apt-get install -y curl
        sudo install -m 0755 -d /etc/apt/keyrings
        curl -fsSL https://pkg.ddev.com/apt/gpg.key | gpg --dearmor | sudo tee /etc/apt/keyrings/ddev.gpg > /dev/null
        sudo chmod a+r /etc/apt/keyrings/ddev.gpg

        # Add DDEV releases to your package repository
        sudo sh -c 'echo ""'
        echo "deb [signed-by=/etc/apt/keyrings/ddev.gpg] https://pkg.ddev.com/apt/ * *" | sudo tee /etc/apt/sources.list.d/ddev.list >/dev/null

        # Update package information and install DDEV
        sudo sh -c 'echo ""'
        sudo apt-get update && sudo apt-get install -y ddev

        # One-time initialization of mkcert
        mkcert -install


## Mac OS

1. Install docker

https://docs.docker.com/desktop/setup/install/mac-install/

2. Install ddev

https://docs.ddev.com/en/stable/users/install/ddev-installation/#ddev-installation-macos
