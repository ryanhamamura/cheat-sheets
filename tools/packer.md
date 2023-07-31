# Packer
Create idempotent machine images for multiple platforms from a single configuration source. 

[Project Homepage](https://www.packer.io)
[Documentation](https://developer.hashicorp.com/packer/docs)
[Plugins](https://developer.hashicorp.com/packer/plugins)
---

## Installation

### macOS
```sh 
brew tap hashicorp/tap 
brew install hashicorp/tap/packer 
```

### Windows 
https://developer.hashicorp.com/packer/downloads


### Linux
#### Ubuntu/Debian 
```sh 
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install packer 
```



