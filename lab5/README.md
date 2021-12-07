# Lab5

Choose one of DPDK performance test and  SPDK performance test. Welcome to choose both, but no extra score.

DPDK performance test:

   (1)Create two virtual machines on KVM.

   (2)Compile and install DPDK library on each virtual machine.

   (3)Compile and run DPDK sample application l2fwd on VM2, then compile and run pktgen-dpdk on VM1.  pkgen-dpdk will record the size of the packages VM1 sends and the amount of packages received from VM2,  while l2fwd just send back the packages it received from VM1.

   (4)Evaluate DPDK’s performance of L2 forwarding.

SPDK performance test:

   (1)Create one virtual machine on KVM.

   (2)Compile and install SPDK library on the host machine.

   (3)Compile and run SPDK vhost-user sample application with a malloc device as the vhost-user back-end on the host, then start the VM with the attached vhost-user socket, exposing to the VM either a block device or scsi device. Please remember to prevent the VM from booting using this empty disk.

   (4)In the VM, make sure the virtio_blk or virtio_scsi kernel driver is correctly probed, and the virtual disk is shown (use $ lsblk to check).

   (5)In the VM, use the fio tool to benchmark this newly added virtual disk. Please get as high performance (in terms of throughput or IOPS) as you can, by changing fio and vhost-user settings, or proposing your optimizations.
