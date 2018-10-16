Patches for CentOS 7.5-alt linux-4.14.0-49.2.2.el7a kernel.

CentOS7.5 for P9 kernel linux-4.14.0-49.2.2.el7a kernel already included patches in https://github.com/liyi-ibm/linux/tree/hostos-4.14.y.
There are two patches missing. The kernel spec file is changed to include these two patches.

To build:

1. $ wget http://vault.centos.org/7.5.1804/updates/Source/SPackages/kernel-alt-4.14.0-49.2.2.el7a.src.rpm
2. $ rpm -ihv kernel-alt-4.14.0-49.2.2.el7a.src.rpm
3. $ cp *.patch ~/rpmbuild/SOURCES/
4. $ cp kernel-alt.spec ~/rpmbuild/SPEC/
5. $ rpmbuild -ba ~/rpmbuild/SPECS/kernel-alt.spec --without kabichk --nodeps

This will build *kernel-alt-4.14.0-49.2.2.el7a.1.src.rpm* and *kernel-4.14.0-49.2.2.el7a.1.ppc64le.rpm*
