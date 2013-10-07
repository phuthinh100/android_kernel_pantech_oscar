1. How to build Kernel source of P8010_JB

    - Firstly Get Toolchain from android git server and etc ¡¦
        GCC correct version is arm-eabi-4.6.x
    - modify build_kernel shell script.
        edit "CROSS_COMPILE" to toolchain path ( You downloaded )
        ex) CROSS_COMPILE=$(your download directory)/prebuilts/gcc/linux-x86/arm/arm-eabi-4.6/bin/arm-eabi-
    - run build_kernel.sh
        $./build_kernel.sh
         

2.	Output File Location
    - kernel : ./obj/KERNEL_OBJ/arch/arm/boot/zImage
    - module : ./kernel/obj/KERNEL_OBJ/drivers/*/*.ko
    - bootimg : ./mkbootimg/boot.img
      
3.	How to Clean Kernel object files
    - run clean_kernel.sh
        $./clean_kernel.sh


Kernel source:
Based in kernel source published by Pantech and Qualcomm's tag M8960AAAAANLYA1744J,
inserted into the history for traceability:
https://www.codeaurora.org/cgit/quic/la/kernel/msm/tree/?id=M8960AAAAANLYA1742J
