# install git on rockylinux 9.4


**first of all we should install vital packages for build and compile, include:gcc, make,...**
```bash
dnf groupinstall "Development Tools" -y 
```
**we should install library packages for git**
```bash
dnf install curl-devel expat-devel gettext-devel openssl-devel perl-CPAN perl-devel zlib-devel wget tar -y
```

**download specific version of git from tarball**
```bash
wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.45.1.tar.gz
```
**extract from archive and unzip to specific path**
```bash
tar zxvf git-2.45.1.tar.gz
```
**change to git directory**
```bash
cd git-2.45.1/
```
**compile and build from source to specific path**
```bash
make prefix=/usr/local all
```
**install git from specific path**
```bash
make prefix=/usr/local install
```

