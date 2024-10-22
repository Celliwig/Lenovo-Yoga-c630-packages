# Lenovo Yoga c630 packages

A collection of packages to facilitate running linux on the Lenovo Yoga c630.

If you wish to run one of the kernel packages please follow these instructions.

* Install kernel.deb & qmi-svc.deb (if you haven't built qmi userspace utils) packages.
* Edit /etc/default/grub, add 'pd_ignore_unused clk_ignore_unused' to GRUB_CMDLINE_LINUX_DEFAULT option (should resemble GRUB_CMDLINE_LINUX_DEFAULT="efi=novamap pd_ignore_unused clk_ignore_unused"). Run 'sudo update-grub'.
* Reboot into Windows, run an update to ensure device drivers are up to date. Reboot to linux with the new kernel.
* Run [yoga_fw_extract.sh](https://github.com/Celliwig/Lenovo-Yoga-c630/tree/master/yoga_fw_extract) to create the relavent firmware directories.
* Install initramfs-tools-firmware.deb.
* Reboot.
