# Kernel Configuration Changes Log

This log tracks modifications made to the `kernconfig` file to optimize kernel build and boot times.

## Batch 1: Removed Legacy Hardware

- **Line 2416:** `# CONFIG_PCCARD is not set`
  - **Reason:** Removed legacy PCMCIA/CardBus support.
- **Line 2418:** `# CONFIG_PCMCIA_LOAD_CIS is not set`
  - **Reason:** Removed legacy PCMCIA/CardBus support.
- **Line 2419:** `# CONFIG_CARDBUS is not set`
  - **Reason:** Removed legacy PCMCIA/CardBus support.
- **Line 2728:** `# CONFIG_PARPORT is not set`
  - **Reason:** Removed legacy Parallel Port support.
- **Line 2746:** `# CONFIG_BLK_DEV_FD is not set`
  - **Reason:** Removed legacy Floppy Disk support.

## Batch 2: Unused Network Protocols and Drivers

- **Line 1865:** `# CONFIG_ATM is not set`
  - **Reason:** Removed legacy ATM network protocol support.
- **Line 2117:** `# CONFIG_CAN is not set`
  - **Reason:** Removed CAN bus support (for automotive/industrial use).
- **Line 2117:** `# CONFIG_BT is not set`
  - **Reason:** Removed BT support.
- **Line 2095:** `# CONFIG_HAMRADIO is not set`
  - **Reason:** Removed Amateur Radio (HAMRADIO) support.
- **Line 4391:** `# CONFIG_ISDN is not set`
  - **Reason:** Removed legacy ISDN support.
- **Line 9219:** `# CONFIG_INFINIBAND is not set`
  - **Reason:** Removed InfiniBand support (for high-performance computing).

## Batch 3: Filesystem Optimization

- **Line 11112:** `# CONFIG_JFS_FS is not set`
  - **Reason:** Removed JFS filesystem support (not in use).
- **Line 11117:** `# CONFIG_XFS_FS is not set`
  - **Reason:** Removed XFS filesystem support (not in use).
- **Line 11140:** `# CONFIG_BTRFS_FS is not set`
  - **Reason:** Removed BTRFS filesystem support (not in use).
- **Line 11147:** `# CONFIG_F2FS_FS is not set`
  - **Reason:** Removed F2FS filesystem support (not in use).
- **Line 11235:** `# CONFIG_NTFS3_FS is not set`
  - **Reason:** Removed NTFS3 filesystem support.
- **Line 11239:** `# CONFIG_NTFS_FS is not set`
  - **Reason:** Removed legacy NTFS filesystem support.
- **Line 11278:** `# CONFIG_HFS_FS is not set`
  - **Reason:** Removed HFS filesystem support.
- **Line 11279:** `# CONFIG_HFSPLUS_FS is not set`
  - **Reason:** Removed HFS+ filesystem support.

## Batch 4: Disabling Debugging and Tracing

- **Line 12127:** `# CONFIG_DEBUG_BUGVERBOSE is not set`
  - **Reason:** Disabled verbose bug reports to reduce code size.
- **Line 12130:** `# CONFIG_DEBUG_KERNEL is not set`
  - **Reason:** Disabled general kernel debugging to reduce overhead.
- **Line 12130:** `# CONFIG_DYNAMIC_DEBUG is not set`
  - **Reason:** Disabled general kernel debugging to reduce overhead.
- **Line 12167:** `# CONFIG_MAGIC_SYSRQ is not set`
  - **Reason:** Disabled the Magic SysRq key for a slightly smaller kernel.
- **Line 12171:** `# CONFIG_DEBUG_FS is not set`
  - **Reason:** Disabled the debug filesystem, which is not needed for a production kernel.
- **Line 12198:** `# CONFIG_SLUB_DEBUG is not set`
  - **Reason:** Disabled SLUB memory allocator debugging.
- **Line 12248:** `# CONFIG_LOCKUP_DETECTOR is not set`
  - **Reason:** Disabled the lockup detector, which adds overhead.
- **Line 12273:** `# CONFIG_SCHED_INFO is not set`
  - **Reason:** Disabled scheduler debugging info.
- **Line 12363:** `# CONFIG_FTRACE is not set`
  - **Reason:** Disabled the Ftrace kernel tracing infrastructure.

## Batch 5: Specialized Optimizations (CPU and Virtualization)

- **Line 435:** `CONFIG_X86_NATIVE_CPU=y` (n/a on Aarch64)
  - **Reason:** Enabled native CPU optimization to tailor the kernel for the specific CPU architecture, improving performance.
- **Virtualization Support (Guest):** (untouched on aarch64)
  - **Line 407:** `# CONFIG_HYPERVISOR_GUEST is not set`
  - **Line 408:** `# CONFIG_PARAVIRT is not set`
  - **Line 413:** `# CONFIG_XEN is not set`
  - **Line 425:** `# CONFIG_KVM_GUEST is not set`
    - **Reason:** Disabled guest-specific virtualization optimizations as this is a native install.
- **Virtualization Support (Host - Re-enabled as Modules):**
  - **Line 826:** `CONFIG_VIRTUALIZATION=m`
  - **Line 828:** `CONFIG_KVM=m`
  - **Line 829:** `CONFIG_KVM_INTEL=m`
  - **Line 832:** `CONFIG_KVM_AMD=m`
    - **Reason:** Re-enabled virtualization hosting support (KVM and general virtualization) as loadable modules.

## Batch 8: Building Essential Modules into Kernel (for faster boot)

**Note on Initramfs Generation:** When a new kernel is built, tools like `mkinitcpio` (Arch Linux) or `update-initramfs` (Debian/Ubuntu) automatically inspect the kernel to identify which modules are now built directly in (`=y`). These tools then generate a new, smaller initramfs that excludes these built-in modules, further optimizing boot time.

- **Line 2794:** `CONFIG_NVME=y`
  - **Reason:** Built NVMe support into kernel.
- **Line 2795:** `CONFIG_BLK_DEV_NVME=y`
  - **Reason:** Built block layer NVMe support into kernel.
- **Line 9021:** `CONFIG_MMC=y`
  - **Reason:** Built MMC core support into kernel.
- **Line 9022:** `CONFIG_MMC_BLOCK=y`
  - **Reason:** Built MMC block support into kernel.
- **Line 7186:** `CONFIG_DRM_AMDGPU=y`
  - **Reason:** Built AMDGPU driver into kernel.
- **Line 7209:** `CONFIG_DRM_NOUVEAU=y`
  - **Reason:** Built Nouveau driver into kernel.
- **Line 7161:** `CONFIG_DRM_EXEC=y`
  - **Reason:** Built DRM exec support into kernel.
- **Line 7162:** `CONFIG_DRM_GPUVM=y`
  - **Reason:** Built DRM GPUVM support into kernel.
- **Line 7163:** `CONFIG_DRM_GPUSVM=y`
  - **Reason:** Built DRM GPUSVM support into kernel.
- **Line 7164:** `CONFIG_DRM_BUDDY=y`
  - **Reason:** Built DRM buddy allocator into kernel.
- **Line 7166:** `CONFIG_DRM_TTM_HELPER=y`
  - **Reason:** Built DRM TTM helper into kernel.
- **Line 7169:** `CONFIG_DRM_SUBALLOC_HELPER=y`
  - **Reason:** Built DRM suballoc helper into kernel.
- **Line 6282:** `CONFIG_VIDEO_DEV=y`
  - **Reason:** Built generic video device support into kernel.

## Batch 9: Final Reconciliation after `make localmodconfig`

- **Action:** Ran `make localmodconfig` to further strip the kernel.
  - **Result:** `localmodconfig` successfully disabled many of the unused modules and filesystems we targeted, and confirmed our virtualization hosting settings.
  - **Correction:** `CONFIG_DEBUG_FS` was re-enabled by `localmodconfig`. This was corrected to `# CONFIG_DEBUG_FS is not set` (Line 7364 in the post-localmodconfig file).

## Remote Machine Specifications

```
                   -`                     efe@archx86
                 .o+`                    -----------
                `ooo/                    OS: Arch Linux x86_64
               `+oooo:                   Host: Victus by HP Gaming Laptop 16-s0xxx
              `+oooooo:                  Kernel: Linux 6.18.1-arch1-2
              -+oooooo+:                 Uptime: 1 hour, 47 mins
            `/:-:++oooo+:                Packages: 184 (pacman)
           `/++++/+++++++:               Shell: sshd-session: efe@notty
          `/++++++++++++++:              Display (CMN162E): 1920x1080 in 16", 144 Hz [Built-in]
         `/+++ooooooooooooo/`            Terminal: sshd
        ./ooosssso++osssssso+`           CPU: AMD Ryzen 7 7840HS (16) @ 5.14 GHz
       .oossssso-````/ossssss+`          GPU 1: NVIDIA GeForce RTX 4060 Max-Q / Mobile [Discrete]
      -osssssso.      :ssssssso.         GPU 2: AMD Phoenix1 [Integrated]
     :osssssss/        osssso+++.        Memory: 2.93 GiB / 14.90 GiB (20%)
    /ossssssss/        +ssssooo/-        Swap: 4.00 KiB / 4.00 GiB (0%)
  `/ossssso+/:-        -:/+osssso+-      Disk (/): 3.34 GiB / 14.66 GiB (23%) - ext4
 `+sso+:-`                 `.-/+oso:     Disk (/home/efe/kernelbuild): 18.75 GiB / 26.84 GiB (70%) - ext4
`++:.                           `-/+/    Local IP (wlan0): 192.168.1.40/24
.`                                 `/    Battery (PABAS0241231): 100% [AC Connected]
                                         Locale: C
```
