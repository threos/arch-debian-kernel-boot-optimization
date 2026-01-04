# CS350 Project Measurements ARM

## Debian - NVMe Boot Time Measurements

### Stock Kernel (6.1.0-37-arm64)

| Boot | Kernel | Userspace | Total |
|------|--------|-----------|-------|
| 1    | 2962 ms| 4156 ms   | 7119 ms|
| 2    | 2906 ms| 4373 ms   | 7279 ms|
| 3    | 2964 ms| 4655 ms   | 7620 ms|
| 4    | 2944 ms| 4240 ms   | 7184 ms|
| 5    | 2934 ms| 4521 ms   | 7455 ms|
| **Avg** | **2942 ms** | **4389 ms** | **7331 ms** |

### Custom Kernel (6.1.158-prl-fast)

| Boot | Kernel | Userspace | Total |
|------|--------|-----------|-------|
| 1    | 664 ms | 4627 ms   | 5292 ms|
| 2    | 1134 ms| 3897 ms   | 5031 ms|
| 3    | 875 ms | 4679 ms   | 5554 ms|
| 4    | 1214 ms| 4409 ms   | 5624 ms|
| 5    | 1151 ms| 4500 ms   | 5652 ms|
| **Avg** | **1008 ms** | **4422 ms** | **5431 ms** |

### NVMe Summary

| Metric | Stock Kernel | Custom Kernel | Improvement |
|--------|--------------|---------------|-------------|
| **Average Total Boot Time** | 7331 ms (7.33 s) | 5431 ms (5.43 s) | **26% faster** |
| **Average Kernel Time** | 2942 ms | 1008 ms | **66% faster** |
| **Average Userspace Time** | 4389 ms | 4422 ms | 1% slower |

## Debian - Flash Drive Boot Time Measurements

### Stock Kernel (6.1.0-37-arm64)

| Boot | Kernel | Userspace | Total |
|------|--------|-----------|-------|
| 1    | 2510 ms| 7048 ms   | 9559 ms|
| 2    | 2521 ms| 8115 ms   | 10636 ms|
| 3    | 2533 ms| 7174 ms   | 9708 ms|
| 4    | 2542 ms| 7673 ms   | 10216 ms|
| 5    | 2591 ms| 6911 ms   | 9503 ms|
| **Avg** | **2539 ms** | **7384 ms** | **9924 ms** |

### Custom Kernel (6.1.158-prl-fast)

| Boot | Kernel | Userspace | Total |
|------|--------|-----------|-------|
| 1    | 794 ms | 7237 ms   | 8032 ms|
| 2    | 814 ms | 7721 ms   | 8535 ms|
| 3    | 1277 ms| 7099 ms   | 8376 ms|
| 4    | 1303 ms| 7236 ms   | 8540 ms|
| 5    | 828 ms | 7702 ms   | 8531 ms|
| **Avg** | **1003 ms** | **7399 ms** | **8403 ms** |

### Flash Drive Summary

| Metric | Stock Kernel | Custom Kernel | Improvement |
|--------|--------------|---------------|-------------|
| **Average Total Boot Time** | 9924 ms (9.92 s) | 8403 ms (8.40 s) | **15% faster** |
| **Average Kernel Time** | 2539 ms | 1003 ms | **61% faster** |
| **Average Userspace Time** | 7384 ms | 7399 ms | 0% (negligible change) |

## Arch - NVMe Boot Time Measurements

### Stock Kernel (6.18.2-1-aarch64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 1407 ms  | 212 ms | 2079 ms| 1271 ms| 1474 ms   | 6445 ms|
| 2    | 1024 ms  | 200 ms | 2077 ms| 1312 ms| 1439 ms   | 6054 ms|
| 3    | 1037 ms  | 208 ms | 2069 ms| 1434 ms| 1457 ms   | 6207 ms|
| 4    | 1087 ms  | 222 ms | 2076 ms| 1320 ms| 1458 ms   | 6164 ms|
| 5    | 1035 ms  | 209 ms | 2090 ms| 1320 ms| 1442 ms   | 6098 ms|
| **Avg** | **1118 ms** | **210 ms** | **2078 ms** | **1331 ms** | **1454 ms** | **6194 ms** |

### Custom Kernel (6.18.2-1-aarch64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 651 ms   | 194 ms | 707 ms | 0 ms   | 2025 ms   | 3578 ms|
| 2    | 652 ms   | 194 ms | 718 ms | 0 ms   | 2110 ms   | 3675 ms|
| 3    | 650 ms   | 193 ms | 686 ms | 0 ms   | 2065 ms   | 3595 ms|
| 4    | 659 ms   | 194 ms | 739 ms | 0 ms   | 2093 ms   | 3687 ms|
| 5    | 690 ms   | 197 ms | 745 ms | 0 ms   | 2094 ms   | 3729 ms|
| **Avg** | **660 ms** | **194 ms** | **719 ms** | **0 ms** | **2077 ms** | **3653 ms** |

### NVMe Summary

| Metric | Stock Kernel | Custom Kernel | Improvement |
|--------|--------------|---------------|-------------|
| **Average Total Boot Time** | 6194 ms (6.19 s) | 3653 ms (3.65 s) | **41% faster** |
| **Average Kernel Time** | 2078 ms | 719 ms | **65% faster** |
| **Average Loader Time** | 210 ms | 194 ms | 8% faster |
| **Average Firmware Time** | 1118 ms | 660 ms | **41% faster** |
| **Average Userspace Time** | 1454 ms | 2077 ms | 43% slower |
| **Initrd Time** | 1331 ms | 0 ms | Eliminated |

## Arch - Flash Drive Boot Time Measurements

### Stock Kernel (6.18.2-1-aarch64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 684 ms   | 1829 ms| 2069 ms| 1359 ms| 1767 ms   | 7710 ms|
| 2    | 799 ms   | 1137 ms| 2060 ms| 1417 ms| 1775 ms   | 7189 ms|
| 3    | 710 ms   | 2004 ms| 2050 ms| 1523 ms| 1821 ms   | 8111 ms|
| 4    | 653 ms   | 1831 ms| 2057 ms| 1381 ms| 1701 ms   | 7625 ms|
| 5    | 739 ms   | 1027 ms| 2064 ms| 1289 ms| 1448 ms   | 6568 ms|
| **Avg** | **717 ms** | **1566 ms** | **2060 ms** | **1394 ms** | **1702 ms** | **7441 ms** |

### Custom Kernel (6.18.2-1-aarch64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 687 ms   | 588 ms | 828 ms | 0 ms   | 2539 ms   | 4644 ms|
| 2    | 703 ms   | 571 ms | 853 ms | 0 ms   | 2352 ms   | 4480 ms|
| 3    | 693 ms   | 569 ms | 796 ms | 0 ms   | 2327 ms   | 4386 ms|
| 4    | 657 ms   | 553 ms | 810 ms | 0 ms   | 2482 ms   | 4503 ms|
| 5    | 678 ms   | 587 ms | 825 ms | 0 ms   | 2305 ms   | 4397 ms|
| **Avg** | **684 ms** | **574 ms** | **822 ms** | **0 ms** | **2401 ms** | **4482 ms** |

### Flash Drive Summary

| Metric | Stock Kernel | Custom Kernel | Improvement |
|--------|--------------|---------------|-------------|
| **Average Total Boot Time** | 7441 ms (7.44 s) | 4482 ms (4.48 s) | **40% faster** |
| **Average Kernel Time** | 2060 ms | 822 ms | **60% faster** |
| **Average Loader Time** | 1566 ms | 574 ms | **63% faster** |
| **Average Firmware Time** | 717 ms | 684 ms | 5% faster |
| **Average Userspace Time** | 1702 ms | 2401 ms | 41% slower |
| **Initrd Time** | 1394 ms | 0 ms | Eliminated |