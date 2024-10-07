# Essential CLI Checklist for your Windows Setup Pt. 1/2

`Install`

  - Powershell 7.4.x `Windows Store`
  - Terminal `Windows Store`
  - Virtualbox + Extension Pack 
    - https://www.virtualbox.org
  - VMware Workstation
    - [VMware with Personal License](vmw-notes.md)

`More Optional Apps here :)` -> [windows-apps-checklist Pt. 2/2](windows-apps-checklist.md)

## Chocolatey

`Install`

https://chocolatey.org/install

`Use example`

    choco list

    choco search <package_name>

    choco upgrade -y <package_name>

    choco uninstall -y <package_name>

    choco install -y 7zip

- <package_name>
  - awscli
  - awssamcli
  - azure-cli
  - Cmder
  - gh
  - git
  - opentofu  
  - terraform
  - vault
  - crc
  - openshift-cli
  - Minikube
  - k9s
  - kubernetes-helm
  - kubernetes-helmfile
  - kubernetes-kops
  - vagrant
  - vagrant-vmware-utility
  - serverless
  - go
  - javadecompiler-gui
  - python3
  - sqlitestudio
  - nvm
  - liberica8jdk
  - liberica11jdk
  - liberica17jdk
  - openjdk --version=21.0.2
  - kotlinc --version=1.5.20
  - maven
  - gradle
  - flutter 
  - dotnet-6.0-sdk

## Vagrant

`Use example`

    vagrant plugin list    
    vagrant plugin install vagrant-vmware-desktop
    vagrant plugin update vagrant-vmware-desktop

    vagrant init bento/ubuntu-20.04

    vagrant up --provider=virtualbox db01 // Multiple VMs
    vagrant up --provider=vmware_desktop
    vagrant up db01
    
    vagrant ssh db01

    vagrant halt db01
    vagrant reload db01

    vagrant status
    vagrant global-status
    vagrant global-status --prune

    vagrant destroy db01

    vagrant box list
    vagrant box remove bento/ubuntu-20.04
    vagrant box remove --all bento/ubuntu-20.04
    vagrant box remove --provider=virtualbox bento/ubuntu-20.04
    vagrant box remove --provider=vmware_desktop bento/ubuntu-20.04

## Pip

`Use example`

    pip install checkov
    
    pip install -U checkov

    checkov -d . //<folder_path/project_name>

## Variables

`Java`

> Sys

    JAVA_HOME: C:\Program Files\BellSoft\LibericaJDK-17
    MAVEN_HOME: C:\ProgramData\chocolatey\lib\maven\apache-maven-3.9.9
    GRADLE_HOME: C:\ProgramData\chocolatey\lib\gradle\tools\gradle-8.10.1

> Path

    %JAVA_HOME%\bin
    C:\Program Files\BellSoft\LibericaJDK-8\bin\
    C:\Program Files\BellSoft\LibericaJDK-11\bin\
    C:\Program Files\OpenJDK\jdk-21.0.2\bin\
    %MAVEN_HOME%\bin
    %GRADLE_HOME%\bin

`Databases`

> Path

    C:\Program Files\MongoDB\Server\6.0\bin
    C:\Users\jorge\AppData\Local\Programs\mongosh
    C:\Program Files\PostgreSQL\16\bin
    C:\Program Files\MySQL\MySQL Server 8.4\bin