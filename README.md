# trabalhando-com-flutter

## Instalação
Repositório com dicas para se trabalhar com Flutter

1) Instalar Android Studio
2) Instalar plugin do Flutter para o Android Studio

### Pós Instalação do Flutter
- Rodar o `flutter doctor`


#### Failed to install the following Android SDK packages as some licences have not been accepted.
Precisa aceitar as licenças do SDK
```
yes | sudo ~/Android/Sdk/tools/bin/sdkmanager --licenses
```

Somente funciona se você estiver usando versão do java 10 ou inferior, se não mostrarar um erro de java ` Exception in thread "main" java.lang.NoClassDefFoundError: javax/xml/bind/annotation/XmlSchema`

O java permite você trocar a versão default, nesse caso você precisará instalar o java 10 ou inferior e trocar a versão default para ele, depois retorne para a versão mais atual.

Optei pelo Java8 pois foi o que instalou de primeira sem outras configurações

Baixe aqui a versão 8 https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html

Siga essas orientações lembrando de trocar o caminho dos arquivos: https://askubuntu.com/questions/56104/how-can-i-install-sun-oracles-proprietary-java-jdk-6-7-8-or-jre

Rode esses comandos para aceitar:
https://github.com/flutter/flutter/issues/22361#issuecomment-452505781


### Rodando o Emulador

#### Falha de permissão no kvm
No Linux mostrava que meu usuário na tinha permissão para executar o kvm.
Toda vez que reinicia o computador, ele volta a pertencer ao usuário root.

Para resolver

```sh
sudo apt install qemu-kvm
sudo adduser $USER kvm
```
Cheque se o dono do arquivo é o root e o grupo kvm, dessa forma irá passar a funcionar uma vez que o seu usuário está no grupo do kvm

```sh
ls -la /dev/kvm
```

#### Unable to lacte adb:
```
sudo apt update && sudo apt install android-sdk
```
Faça o download https://developer.android.com/studio/releases/platform-tools e descompact na pasta `~/Android`

Depois faça os seguintes comandos para colocar a platform tools no path
```sh
cd ~/Android
export PATH="$PATH:`pwd`/platform-tools"
```

