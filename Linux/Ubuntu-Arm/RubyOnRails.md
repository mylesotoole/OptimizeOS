## 1. Installing RVM:

[Add Repo](https://github.com/rvm/ubuntu_rvm/blob/531e67a9903a593d2c9c1f3cb9b6ee4ec332fad2/README.md):
``` 
sudo apt-add-repository -y ppa:rael-gc/rvm
```

[Add Key Import Utility](https://rvm.io/):
```
sudo apt install gnupg2
```

[Add GPG Keys](https://rvm.io/):
``` 
gpg2 --keyserver keyserver.ubuntu.com --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

Install RVM:
```
sudo apt-get install rvm -y
```

[Append it to your shell](https://github.com/rvm/ubuntu_rvm/blob/531e67a9903a593d2c9c1f3cb9b6ee4ec332fad2/README.md):
```
echo 'source "/etc/profile.d/rvm.sh"' >> ~/.bashrc
```


## [2. Installing Ruby](https://www.railstutorial.org/book)

Use RVM:
``` 
rvm get stable
```

```
rvm install 3.1.2
```

```
rvm --default use 3.1.2
```

Check Version:
```
ruby -v
```

## Installing Rails

Configure the __.gemrc__ file to skip the installation of Ruby documentation
```
echo "gem: --no-document" >> ~/.gemrc
```

Install Rails:
```
gem install rails -v 7.0.4
```

Check Version:
```
rails -v
```

Check Version:
```
rails -v
```

## Install Bundler:

```
gem install bundler -v 2.3.14
```
