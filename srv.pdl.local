# azskills
'''
apt install easy-rsa
'''
'''
cd /usr/share/easy-rsa/
'''
'''
./easyrsa init-pki
'''
./easyrsa build-ca
'''
'''
./easyrsa gen-req enta nopass
'''
'''
./easyrsa sign-req server enta
'''
'''
scp -i chave.pem /usr/share/easy-rsa/pki/issued/enta.crt ubuntu@10.0.9.101:/tmp
'''
'''
scp -i chave.pem /usr/share/easy-rsa/pki/private/enta.key ubuntu@10.0.9.101:/tmp
'''
