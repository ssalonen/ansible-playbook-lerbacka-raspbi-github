## Installation

1. install ansible >=2.0
2. setup inventory/hosts

	[pis]
	localhost ansible_port=5022     ansible_user=pi


3. ssh-copy-id pi@pihost -p 5022
4. sudo ansible-galaxy install -r requirements.yml



## Edit public and private key vault:

`ansible-vault --vault-password-file vault_password edit vars/id_rsa.yml`

````
---
public_key_content: "ssh-rsa foobar root@raspberrypi"
private_key_content: |
  -----BEGIN RSA PRIVATE KEY-----
  foobarfoobarfoobar
  foobarfoobarfoobar
  -----END RSA PRIVATE KEY-----
````

## Edit password vault:

`ansible-vault --vault-password-file vault_password edit vars/id_rsa.yml`

````
---
passwords:
  - user: pi
    password_sha_512: sha_512_hashed_password_here
  - user: root
    password_sha_512: sha_512_hashed_password_here
````