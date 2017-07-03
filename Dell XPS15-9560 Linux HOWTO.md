# Install Ubuntu 16.04 on Dell XPS 15-9560 (2017)

Well - never managed to finish the docs as nothing particular special was required. I use this device with Ubuntu 16.04 as my daily driver. So this instructions only contain the few notes i took ...

## Notes

- Start and complete Windows 10 setup
- Create a Windows recovery USB stick
- Update BIOS to latest (Download from http://www.dell.com/support/home/uk/en/ukdhs1/product-support/product/xps-15-9560-laptop/drivers)

https://askubuntu.com/questions/729673/ubuntu-full-disk-encryption-with-encrypted-boot

```
cryptsetup -v --cipher aes-xts-plain64 --key-size 512 --hash sha256 --iter-time 5000 --verify-passphrase luksFormat /dev/nvme0n1p7

grub-install --uefi-secure-boot
```

```
/dev/nvme0n1p1 - EFI
/dev/nvme0n1p7 - root
/dev/nvme0n1p8 - temp boot / swap
```



