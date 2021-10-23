#Packages to install when installing debian
su
apt-get install sudo
sudo adduser <username> sudo

#Restart the machine
sudo apt-get install build-essentials synaptic thunderbird dconf-editor git terminator wireshark dirmngr linux-headers*

#If you can't install VBoxGuestAdditions
--> Go to /etc/fstab
--> Add exec after noauto

#TweakTool modifications
--> Go to your account of GNOME Shell
--> Download plugins for TweakTool

#Install Atom
--> https://atom.io/
--> dpkg -i atom*

#Install Spotify
  # wget http://security.debian.org/debian-security/pool/updates/main/o/openssl/libssl1.0.0_1.0.1t-1+deb8u6_amd64.deb
  # sudo dpkg -i libssl1.0.0_1.0.1t-1+deb8u6_amd64.deb

  # 1. Add the Spotify repository signing keys to be able to verify downloaded packages
  sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys BBEBDCB318AD50EC6865090613B00F1FD2C19886 0DF731E45CE24F27EEEB1450EFDC8610341D9410

  # 2. Add the Spotify repository
  echo deb http://repository.spotify.com stable non-free | sudo tee /etc/apt/sources.list.d/spotify.list

  # 3. Update list of available packages
  sudo apt-get update

  # 4. Install Spotify
  sudo apt-get install spotify-client
