# trabalhando-com-flutter

## Instalação
Repositório com dicas para se trabalhar com Flutter

1) Instalar Android Studio
2) Instalar plugin do Flutter para o Android Studio

### Pós Instalação do Flutter
- Rodar o `flutter doctor`


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
