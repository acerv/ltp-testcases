# LTP testcases

Dependences:

- [ltp-core](https://github.com/acerv/ltp-core)

Supported testcases:

- cve

In order to compile our testing suites, use the following procedure:

```sh
# make sure libltp has been installed inside the system
# setup build folder
meson setup builddir && cd builddir

# compile tests
meson compile

# install tests inside /opt/ltp/testcases/bin
sudo meson install
```
