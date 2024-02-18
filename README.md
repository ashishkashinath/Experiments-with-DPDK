# Experiments-with-DPDK
This repo captures the different experiments with DPDK on Logic Supply.

### Prerequisites

- Enable HUGEPAGES
    ```
    sudo su
    echo 1024 > /sys/kernel/mm/hugepages/hugepages-2048kB/nr_hugepages
    ```
- Install pkgconf
    ```
    sudo apt install pkgconf
    ```
### Compiling DPDK

+ First we go to the root of the `dpdk` and perform the following steps

    ```
    meson setup build
    cd build/
    ninja
    sudo meson install
    ```

+ Now, we can go into an example to compile it against `dpdk`. For example, `helloworld` can be compiled as:

    ```
    cd dpdk/examples/helloworld/build
    make
    sudo ./helloworld
    ```


+ A successful compilation and run would show the following:



