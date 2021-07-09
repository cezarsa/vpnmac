# vpnmac

## Usage

Install and configure dependencies:

```
$ brew install openconnect
$ go get -u rsc.io/2fa
$ 2fa -add <vpn token name>
2fa key for <vpn token name>: <TOTP token secret>
```

Clone the repository:

```
git clone https://github.com/cezarsa/vpnmac.git
```

Create a .env file with your auth information:

```
cd vpnmac
echo 'VPN_HOST="<my.vpn.host>"' >>.env
echo 'USER="<vpn username>"' >>.env
echo 'PASSWORD="<vpn password>"' >>.env

# Optional if 2fa is required and rsc.io/2fa is used to manage 2fa tokens
echo 'TFA_NAME="<token name registered in 2fa>"' >>.env

# Optional if openconnect fails requiring a server fingerprint
echo 'SERVER_CERT="<server SHA1 fingerprint>"' >>.env
```
