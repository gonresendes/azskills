# INSTALAÇÃO E CONFIGURAÇÃO DO EASY-RSA
## SRV.PDL.LOCAL
Os seguintes comandos estão em sequência para a instalação e configuração do easy-rsa no servidor pdl:

1. Instala o easy-rsa;
```
apt install easy-rsa
```
2. Acede á seguinte pasta do easy-rsa;
```
cd /usr/share/easy-rsa/
```
3. Inicia o pki;
```
./easyrsa init-pki
```
4. Cria o certificado, neste passo é importante dar um nome referido á localização da máquina;
```
./easyrsa build-ca
```
5. Gera um pedido, aqui insere o nome que deste ao server;
```
./easyrsa gen-req enta nopass
```
6. Assina o certificado;
```
./easyrsa sign-req server enta
```
7. Passa o certificado para a máquina que necessita do certificado;
```
scp -i chave.pem /usr/share/easy-rsa/pki/issued/enta.crt ubuntu@10.0.9.101:/tmp
```
8. Passa a key para a máquina que necessita da key;
```
scp -i chave.pem /usr/share/easy-rsa/pki/private/enta.key ubuntu@10.0.9.101:/tmp
```
