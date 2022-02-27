# 在vmware中创建自己的操作系统

## 使用-arch Linux

1. 安装qemu

    sudo pacman -S qemu

2. 使用qemu转换格式

    qemu-img convert -O XXX.img XXX.vmdk
