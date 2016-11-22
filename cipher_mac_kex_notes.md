# Cipher and Message Authentication Code Support

For systems that don't list all supported ciphers, mac and kex in the documentation, the approach described http://superuser.com/a/869005/385596 will help:
- strings /usr/sbin/sshd |grep mac

- strings /usr/sbin/sshd |grep aes
- strings /usr/sbin/sshd |grep blowfish
- strings /usr/sbin/sshd |grep 3des
- strings /usr/sbin/sshd |grep arc

- strings /usr/sbin/sshd |grep diffie

## Ubuntu 4.10 (Warty Warthog)

### Ciphers
- aes128-cbc
- 3des-cbc
- blowfish-cbc
- cast128-cbc
- arcfour
- aes192-cbc
- aes256-cbc
- aes128-ctr
- aes192-ctr
- aes256-ctr

Default (client): aes128-cbc,3des-cbc,blowfish-cbc,cast128-cbc,arcfour,aes192-cbc,aes256-cbc

Default (server): aes128-cbc,3des-cbc,blowfish-cbc,cast128-cbc,arcfour,aes192-cbc,aes256-cbc, aes128-ctr,aes192-ctr,aes256-ctr

### MACs
- hmac-md5
- hmac-sha1
- hmac-ripemd160
- hmac-sha1-96
- hmac-md5-96

Default (client): hmac-md5,hmac-sha1,hmac-ripemd160,hmac-sha1-96,hmac-md5-96

Default (server): hmac-md5,hmac-sha1,hmac-ripemd160,hmac-sha1-96,hmac-md5-96

### Key Exchange Algorithm
- diffie-hellman-group-exchange-sha1
- diffie-hellman-group1-sha1

Default (client): Not explicitly listed

Default (server): Not explicitly listed


## Ubuntu 16.04 (Xenial Xerus)

### Ciphers
- 3des-cbc
- blowfish-cbc
- cast128-cbc
- arcfour
- arcfour128
- arcfour256
- aes128-cbc
- aes192-cbc
- aes256-cbc
- rijnael-cbc@lysator.liu.se
- aes128-ctr
- aes192-ctr
- aes256-ctr
- aes128-gcm@openssh.com
- aes256-gcm@openssh.com
- chacha20-poly1305@openssh.com

Default order (client): chacha20-poly1305@openssh.com,aes128-ctr,aes192-ctr,aes256-ctr,aes128-gcm@openssh.com,aes256-gcm@openssh.com,aes128-cbc,aes192-cbc,aes256-cbc,3des-cbc

Default order (server): chacha20-poly1305@openssh.com,aes128-ctr,aes192-ctr,aes256-ctr,aes128-gcm@openssh.com,aes256-gcm@openssh.com

### MACs
- hmac-sha1
- hmac-sha1-96
- hmac-sha1-256
- hmac-sha1-512
- hmac-md5
- hmac-md5-96
- hmac-ripemd160
- hmac-ripemd160@openssh.com
- umac-64@openssh.com
- umac-128@openssh.com
- hmac-sha1-etm@openssh.com
- hmac-sha1-96-etm@openssh.com
- hmac-sha2-256-etm@openssh.com
- hmac-sha2-512-etm@openssh.com
- hmac-md5-etm@openssh.com
- hmac-ripemd160-etm@openssh.com
- umac-64-etm@openssh.com
- umac-128-etm@openssh.com

Default order (client): umac-64-etm@openssh.com,umac-128-etm@openssh.com,hmac-sha2-256-etm@openssh.com,hmac-sha2-512-etm@openssh.com,hmac-sha1-etm@openssh.com,umac-64@openssh.com,umac-128@openssh.com,hmac-sha2-256,hmac-sha2-512,hmac-sha1

Default order (server): umac-64-etm@openssh.com,umac-128-etm@openssh.com,hmac-sha2-256-etm@openssh.com,hmac-sha2-512-etm@openssh.com,hmac-sha1-etm@openssh.com,umac-64@openssh.com,umac-128@openssh.com,hmac-sha2-256,hmac-sha2-512,hmac-sha1

### Key Exchange Algorithm
- diffie-hellman-group1-sha1
- diffie-hellman-group14-sha1
- diffie-hellman-group-exchange-sha1
- diffie-hellman-group-exchange-sha256
- ecdh-sha2-nistp256
- ecdh-sha2-nistp384
- ecdh-sha2-nistp521
- curve25519-sha256@libssh.org

Default order (client): curve25519-sha256@libssh.org,ecdh-sha2-nistp256,ecdh-sha2-nistp384,ecdh-sha2-nistp521,diffie-hellman-group-exchange-sha256,diffie-hellman-group-exchange-sha1,diffie-hellman-group14-sha1

Default order (server): curve25519-sha256@libssh.org,ecdh-sha2-nistp256,ecdh-sha2-nistp384,ecdh-sha2-nistp521,diffie-hellman-group-exchange-sha256,diffie-hellman-group-exchange-sha1,diffie-hellman-group14-sha1


## Fedora Core 1

### Ciphers
- aes128-cbc
- 3des-cbc
- blowfish-cbc
- cast128-cbc
- arcfour
- aes192-cbc
- aes256-cbc

Default order (client): aes128-cbc,3des-cbc,blowfish-cbc,cast128-cbc,arcfour,aes192-cbc,aes256-cbc
Default order (server): aes128-cbc,3des-cbc,blowfish-cbc,cast128-cbc,arcfour,aes192-cbc,aes256-cbc

### MACs
- hmac-sha1
- hmac-sha1-96
- hmac-md5
- hmac-md5-96
- hmac-ripemd160
- hmac-ripemd160@openssh.com

Default order (client): Not given
Default order (server): Not given

### Key Exchange Algorithm
- diffie-hellman-group-exchange-sha1
- diffie-hellman-group1-sha1
- diffie-hellman-group-exchange-sha1
- diffie-hellman-group1-sha1

Default order (client): Not given
Default order (server): Not given
