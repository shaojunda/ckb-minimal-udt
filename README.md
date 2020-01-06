CKB minimal UDT
===============

## Prepare

### Pull `ckb-riscv-gnu-toolchain` image

```
docker pull nervos/ckb-riscv-gnu-toolchain:xenial
```

## Develop

### Build

```
cd src
docker run --rm -it -v `pwd`:/code nervos/ckb-riscv-gnu-toolchain:xenial bash
root@3ede059e304b:/# cd /code
root@3ede059e304b:/code# riscv64-unknown-elf-gcc -Os udt_info.c -o udt-info
root@3ede059e304b:/code# riscv64-unknown-elf-gcc -Os udt_data.c -o udt-data
root@3ede059e304b:/code# exit
```
