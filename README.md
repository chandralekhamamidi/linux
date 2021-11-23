# Asssignment 2 CMPE 283

## Contributions
We connected over a zoom call to run the updated kernel code with the functionalities. We resolved the errors in this process together.

### Himaja Chandaluri

I was responsible for cloning the kernel and building it. In the process I faced errors with the RSA certificate's. 
I resolved it by creating a certificate file and changing the .pem certificate reference in the .config file to the new certificate created.
Created the VM on top of the ubuntu system. Built a test file to test the kernel code. Executed the kernel code.

### Chandra Lekha Mamidi

## Steps followed

1. Forked the torvalds/linux tree
2. Cloned the forked repo into an ubuntu machine
3. Downloaded important libraries for building the kernel
4. Executed `sudo cp /boot/{config-name} ./.config`
5. Executed `sudo make oldconfig`
6. Edited code in `cpuid.c` and `vmx.c`, to satify the leaf nodes `0x4fffffff` ans '0x4ffffffe` requirments
7. Executed `sudo make -j 8 modules`
8. Executed `sudo make -j 8`
9. Executed `make INSTALL_MOD_STRIP=1 modules_install`
10. Loaded kvm using the command `modprobe kvm` and `modprobe kvm_linux`
11. Created a VM using VirtManager
12. Created a test file and executed it to see the results


