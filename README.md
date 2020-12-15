# debian-openssl

This repository provides openssl debianized source package for Debian Jessie.

Source repository - https://salsa.debian.org/debian/openssl

## Install build requirements:

```
apt-get -qq update && apt-get -y install build-essential debhelper devscripts dpkg-dev fakeroot git m4 bc
```

## Clone this branch to your build server:

```
cd /root
git clone https://github.com/kautMaks/debian-oenssl.git
```

## Get openssl sources:

```
wget https://www.openssl.org/source/openssl-1.1.1i.tar.gz
tar -xvf openssl-1.1.1i.tar.g && mv openssl-1.1.1i/* debian-openssl/
cd  debian-openssl/
```

## Build openssl with enabled tests:

```
debuild -us -uc -b
```
