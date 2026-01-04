# CS350 Project Measurements ARM

## Arch

### NVMe
#### Stock Kernel
##### Boot 1<!-- {"fold":true} -->

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 1.407s (firmware) + 212ms (loader) + 2.079s (kernel) + 1.271s (initrd) + 1.474s (userspace) = 6.445s 
graphical.target reached after 1.473s in userspace.
Startup finished in 1.407s (firmware) + 212ms (loader) + 2.079s (kernel) + 1.271s (initrd) + 1.474s (userspace) = 6.445s 
graphical.target reached after 1.473s in userspace.
[root@myhostname ~] # 
```

##### Boot 2<!-- {"fold":true} -->

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 1.024s (firmware) + 200ms (loader) + 2.077s (kernel) + 1.312s (initrd) + 1.439s (userspace) = 6.054s 
graphical.target reached after 1.438s in userspace.
Startup finished in 1.024s (firmware) + 200ms (loader) + 2.077s (kernel) + 1.312s (initrd) + 1.439s (userspace) = 6.054s 
graphical.target reached after 1.438s in userspace.
[root@myhostname ~] # 
```

##### Boot 3<!-- {"fold":true} -->

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 1.037s (firmware) + 208ms (loader) + 2.069s (kernel) + 1.434s (initrd) + 1.457s (userspace) = 6.207s 
graphical.target reached after 1.455s in userspace.
Startup finished in 1.037s (firmware) + 208ms (loader) + 2.069s (kernel) + 1.434s (initrd) + 1.457s (userspace) = 6.207s 
graphical.target reached after 1.455s in userspace.
[root@myhostname ~] # 
```

##### Boot 4<!-- {"fold":true} -->

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 1.087s (firmware) + 222ms (loader) + 2.076s (kernel) + 1.320s (initrd) + 1.458s (userspace) = 6.164s 
graphical.target reached after 1.454s in userspace.
Startup finished in 1.087s (firmware) + 222ms (loader) + 2.076s (kernel) + 1.320s (initrd) + 1.458s (userspace) = 6.164s 
graphical.target reached after 1.454s in userspace.
[root@myhostname ~] # 
```

##### Boot 5<!-- {"fold":true} -->

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 1.035s (firmware) + 209ms (loader) + 2.090s (kernel) + 1.320s (initrd) + 1.442s (userspace) = 6.098s 
graphical.target reached after 1.440s in userspace.
Startup finished in 1.035s (firmware) + 209ms (loader) + 2.090s (kernel) + 1.320s (initrd) + 1.442s (userspace) = 6.098s 
graphical.target reached after 1.440s in userspace.
[root@myhostname ~] #
```

#### Custom Kernel
##### Boot 1<!-- {"fold":true} -->
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 651ms (firmware) + 194ms (loader) + 707ms (kernel) + 2.025s (userspace) = 3.578s 
graphical.target reached after 2.024s in userspace.
Startup finished in 651ms (firmware) + 194ms (loader) + 707ms (kernel) + 2.025s (userspace) = 3.578s 
graphical.target reached after 2.024s in userspace.
[root@myhostname ~] # 
```

##### Boot 2<!-- {"fold":true} -->
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 652ms (firmware) + 194ms (loader) + 718ms (kernel) + 2.110s (userspace) = 3.675s 
graphical.target reached after 2.107s in userspace.
Startup finished in 652ms (firmware) + 194ms (loader) + 718ms (kernel) + 2.110s (userspace) = 3.675s 
graphical.target reached after 2.107s in userspace.
[root@myhostname ~] # 
```
##### Boot 3<!-- {"fold":true} -->
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 650ms (firmware) + 193ms (loader) + 686ms (kernel) + 2.065s (userspace) = 3.595s 
graphical.target reached after 2.064s in userspace.
Startup finished in 650ms (firmware) + 193ms (loader) + 686ms (kernel) + 2.065s (userspace) = 3.595s 
graphical.target reached after 2.064s in userspace.
[root@myhostname ~] # 
```
##### Boot 4<!-- {"fold":true} -->
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 659ms (firmware) + 194ms (loader) + 739ms (kernel) + 2.093s (userspace) = 3.687s 
graphical.target reached after 2.089s in userspace.
Startup finished in 659ms (firmware) + 194ms (loader) + 739ms (kernel) + 2.093s (userspace) = 3.687s 
graphical.target reached after 2.089s in userspace.
[root@myhostname ~] # 
```
##### Boot 5<!-- {"fold":true} -->
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 690ms (firmware) + 197ms (loader) + 745ms (kernel) + 2.094s (userspace) = 3.729s 
graphical.target reached after 2.094s in userspace.
Startup finished in 690ms (firmware) + 197ms (loader) + 745ms (kernel) + 2.094s (userspace) = 3.729s 
graphical.target reached after 2.094s in userspace.
[root@myhostname ~] # 
```

### Flash drive
#### Stock Kernel
##### Boot 1

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 684ms (firmware) + 1.829s (loader) + 2.069s (kernel) + 1.359s (initrd) + 1.767s (userspace) = 7.710s 
graphical.target reached after 1.766s in userspace.
Startup finished in 684ms (firmware) + 1.829s (loader) + 2.069s (kernel) + 1.359s (initrd) + 1.767s (userspace) = 7.710s 
graphical.target reached after 1.766s in userspace.
[root@myhostname ~] #
```

##### Boot 2

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 799ms (firmware) + 1.137s (loader) + 2.060s (kernel) + 1.417s (initrd) + 1.775s (userspace) = 7.189s 
graphical.target reached after 1.774s in userspace.
Startup finished in 799ms (firmware) + 1.137s (loader) + 2.060s (kernel) + 1.417s (initrd) + 1.775s (userspace) = 7.189s 
graphical.target reached after 1.774s in userspace.
[root@myhostname ~] # 
```

##### Boot 3

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 710ms (firmware) + 2.004s (loader) + 2.050s (kernel) + 1.523s (initrd) + 1.821s (userspace) = 8.111s 
graphical.target reached after 1.820s in userspace.
Startup finished in 710ms (firmware) + 2.004s (loader) + 2.050s (kernel) + 1.523s (initrd) + 1.821s (userspace) = 8.111s 
graphical.target reached after 1.820s in userspace.
[root@myhostname ~] # 
```

##### Boot 4

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 653ms (firmware) + 1.831s (loader) + 2.057s (kernel) + 1.381s (initrd) + 1.701s (userspace) = 7.625s 
graphical.target reached after 1.697s in userspace.
Startup finished in 653ms (firmware) + 1.831s (loader) + 2.057s (kernel) + 1.381s (initrd) + 1.701s (userspace) = 7.625s 
graphical.target reached after 1.697s in userspace.
[root@myhostname ~] # 
```

##### Boot 5

```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 739ms (firmware) + 1.027s (loader) + 2.064s (kernel) + 1.289s (initrd) + 1.448s (userspace) = 6.568s 
graphical.target reached after 1.447s in userspace.
Startup finished in 739ms (firmware) + 1.027s (loader) + 2.064s (kernel) + 1.289s (initrd) + 1.448s (userspace) = 6.568s 
graphical.target reached after 1.447s in userspace.
[root@myhostname ~] # 
```

#### Custom Kernel
##### Boot 1
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 687ms (firmware) + 588ms (loader) + 828ms (kernel) + 2.539s (userspace) = 4.644s 
graphical.target reached after 2.537s in userspace.
Startup finished in 687ms (firmware) + 588ms (loader) + 828ms (kernel) + 2.539s (userspace) = 4.644s 
graphical.target reached after 2.537s in userspace.
[root@myhostname ~] # 
```

##### Boot 2
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 703ms (firmware) + 571ms (loader) + 853ms (kernel) + 2.352s (userspace) = 4.480s 
graphical.target reached after 2.351s in userspace.
Startup finished in 703ms (firmware) + 571ms (loader) + 853ms (kernel) + 2.352s (userspace) = 4.480s 
graphical.target reached after 2.351s in userspace.
[root@myhostname ~] # 
```
##### Boot 3
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 693ms (firmware) + 569ms (loader) + 796ms (kernel) + 2.327s (userspace) = 4.386s 
graphical.target reached after 2.325s in userspace.
Startup finished in 693ms (firmware) + 569ms (loader) + 796ms (kernel) + 2.327s (userspace) = 4.386s 
graphical.target reached after 2.325s in userspace.
[root@myhostname ~] # 
```
##### Boot 4
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 657ms (firmware) + 553ms (loader) + 810ms (kernel) + 2.482s (userspace) = 4.503s 
graphical.target reached after 2.477s in userspace.
Startup finished in 657ms (firmware) + 553ms (loader) + 810ms (kernel) + 2.482s (userspace) = 4.503s 
graphical.target reached after 2.477s in userspace.
[root@myhostname ~] #
```
##### Boot 5
```
[root@myhostname ~] # uname -r
systemd-analyze
systemd-analyze time
6.18.2-1-aarch64-ARCH
Startup finished in 678ms (firmware) + 587ms (loader) + 825ms (kernel) + 2.305s (userspace) = 4.397s 
graphical.target reached after 2.304s in userspace.
Startup finished in 678ms (firmware) + 587ms (loader) + 825ms (kernel) + 2.305s (userspace) = 4.397s 
graphical.target reached after 2.304s in userspace.
[root@myhostname ~] #
```

## Debian

### NVMe
#### Stock Kernel
##### Boot 1<!-- {"fold":true} -->

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.0-37-arm64
Startup finished in 2.962s (kernel) + 4.156s (userspace) = 7.119s 
graphical.target reached after 4.136s in userspace.
Startup finished in 2.962s (kernel) + 4.156s (userspace) = 7.119s 
graphical.target reached after 4.136s in userspace.
parallels@debian-gnu-linux-12-11:~$ 
```

##### Boot 2<!-- {"fold":true} -->

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.0-37-arm64
Startup finished in 2.906s (kernel) + 4.373s (userspace) = 7.279s 
graphical.target reached after 4.350s in userspace.
Startup finished in 2.906s (kernel) + 4.373s (userspace) = 7.279s 
graphical.target reached after 4.350s in userspace.
parallels@debian-gnu-linux-12-11:~$ 
```

##### Boot 3<!-- {"fold":true} -->

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.0-37-arm64
Startup finished in 2.964s (kernel) + 4.655s (userspace) = 7.620s 
graphical.target reached after 4.631s in userspace.
Startup finished in 2.964s (kernel) + 4.655s (userspace) = 7.620s 
graphical.target reached after 4.631s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

##### Boot 4<!-- {"fold":true} -->

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.0-37-arm64
Startup finished in 2.944s (kernel) + 4.240s (userspace) = 7.184s 
graphical.target reached after 4.222s in userspace.
Startup finished in 2.944s (kernel) + 4.240s (userspace) = 7.184s 
graphical.target reached after 4.222s in userspace.
parallels@debian-gnu-linux-12-11:~$ 
```

##### Boot 5<!-- {"fold":true} -->

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.0-37-arm64
Startup finished in 2.934s (kernel) + 4.521s (userspace) = 7.455s 
graphical.target reached after 4.502s in userspace.
Startup finished in 2.934s (kernel) + 4.521s (userspace) = 7.455s 
graphical.target reached after 4.502s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

#### Custom Kernel
##### Boot 1<!-- {"fold":true} -->
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 664ms (kernel) + 4.627s (userspace) = 5.292s 
graphical.target reached after 4.593s in userspace.
Startup finished in 664ms (kernel) + 4.627s (userspace) = 5.292s 
graphical.target reached after 4.593s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

##### Boot 2<!-- {"fold":true} -->
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 1.134s (kernel) + 3.897s (userspace) = 5.031s 
graphical.target reached after 3.876s in userspace.
Startup finished in 1.134s (kernel) + 3.897s (userspace) = 5.031s 
graphical.target reached after 3.876s in userspace.
parallels@debian-gnu-linux-12-11:~$
```
##### Boot 3<!-- {"fold":true} -->
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 875ms (kernel) + 4.679s (userspace) = 5.554s 
graphical.target reached after 4.654s in userspace.
Startup finished in 875ms (kernel) + 4.679s (userspace) = 5.554s 
graphical.target reached after 4.654s in userspace.
parallels@debian-gnu-linux-12-11:~$
```
##### Boot 4<!-- {"fold":true} -->
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 1.214s (kernel) + 4.409s (userspace) = 5.624s 
graphical.target reached after 4.391s in userspace.
Startup finished in 1.214s (kernel) + 4.409s (userspace) = 5.624s 
graphical.target reached after 4.391s in userspace.
parallels@debian-gnu-linux-12-11:~$
```
##### Boot 5<!-- {"fold":true} -->
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 1.151s (kernel) + 4.500s (userspace) = 5.652s 
graphical.target reached after 4.480s in userspace.
Startup finished in 1.151s (kernel) + 4.500s (userspace) = 5.652s 
graphical.target reached after 4.480s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

### Flash drive
#### Stock Kernel
##### Boot 1

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 2.510s (kernel) + 7.048s (userspace) = 9.559s 
graphical.target reached after 7.031s in userspace.
Startup finished in 2.510s (kernel) + 7.048s (userspace) = 9.559s 
graphical.target reached after 7.031s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

##### Boot 2

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 2.521s (kernel) + 8.115s (userspace) = 10.636s 
graphical.target reached after 8.093s in userspace.
Startup finished in 2.521s (kernel) + 8.115s (userspace) = 10.636s 
graphical.target reached after 8.093s in userspace.
parallels@debian-gnu-linux-12-11:~$ 
```

##### Boot 3

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 2.533s (kernel) + 7.174s (userspace) = 9.708s 
graphical.target reached after 7.156s in userspace.
Startup finished in 2.533s (kernel) + 7.174s (userspace) = 9.708s 
graphical.target reached after 7.156s in userspace.
parallels@debian-gnu-linux-12-11:~$ 
```

##### Boot 4

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 2.542s (kernel) + 7.673s (userspace) = 10.216s 
graphical.target reached after 7.647s in userspace.
Startup finished in 2.542s (kernel) + 7.673s (userspace) = 10.216s 
graphical.target reached after 7.647s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

##### Boot 5

```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 2.591s (kernel) + 6.911s (userspace) = 9.503s 
graphical.target reached after 6.891s in userspace.
Startup finished in 2.591s (kernel) + 6.911s (userspace) = 9.503s 
graphical.target reached after 6.891s in userspace.
parallels@debian-gnu-linux-12-11:~$ 
```

#### Custom Kernel
##### Boot 1
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 794ms (kernel) + 7.237s (userspace) = 8.032s 
graphical.target reached after 7.208s in userspace.
Startup finished in 794ms (kernel) + 7.237s (userspace) = 8.032s 
graphical.target reached after 7.208s in userspace.
parallels@debian-gnu-linux-12-11:~$
```

##### Boot 2
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 814ms (kernel) + 7.721s (userspace) = 8.535s 
graphical.target reached after 7.704s in userspace.
Startup finished in 814ms (kernel) + 7.721s (userspace) = 8.535s 
graphical.target reached after 7.704s in userspace.
parallels@debian-gnu-linux-12-11:~$
```
##### Boot 3
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 1.277s (kernel) + 7.099s (userspace) = 8.376s 
graphical.target reached after 7.083s in userspace.
Startup finished in 1.277s (kernel) + 7.099s (userspace) = 8.376s 
graphical.target reached after 7.083s in userspace.
parallels@debian-gnu-linux-12-11:~$
```
##### Boot 4
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 1.303s (kernel) + 7.236s (userspace) = 8.540s 
graphical.target reached after 7.213s in userspace.
Startup finished in 1.303s (kernel) + 7.236s (userspace) = 8.540s 
graphical.target reached after 7.213s in userspace.
parallels@debian-gnu-linux-12-11:~$
```
##### Boot 5
```
parallels@debian-gnu-linux-12-11:~$ uname -r
systemd-analyze
systemd-analyze time
6.1.158-prl-fast
Startup finished in 828ms (kernel) + 7.702s (userspace) = 8.531s 
graphical.target reached after 7.684s in userspace.
Startup finished in 828ms (kernel) + 7.702s (userspace) = 8.531s 
graphical.target reached after 7.684s in userspace.
parallels@debian-gnu-linux-12-11:~$
```