# CS350 Project Measurements x86

## Arch - PCIe (NVMe) Boot Time Measurements

### Stock Kernel (6.18.2-1-x86_64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 15503 ms | 1173 ms| 782 ms | 3365 ms| 2250 ms   | 23077 ms|
| 2    | 15397 ms | 1169 ms| 787 ms | 3343 ms| 1700 ms   | 22397 ms|
| **Avg** | **15450 ms** | **1171 ms** | **785 ms** | **3354 ms** | **1975 ms** | **22737 ms** |

### Custom Kernel (6.18.1-1-x86_64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 18928 ms | 370 ms | 784 ms | 1586 ms| 1736 ms   | 23405 ms|
| 2    | 15524 ms | 377 ms | 763 ms | 1578 ms| 2224 ms   | 20469 ms|
| 3    | 16378 ms | 377 ms | 784 ms | 1621 ms| 2333 ms   | 21496 ms|
| 4    | 12347 ms | 376 ms | 763 ms | 1586 ms| 2236 ms   | 17309 ms|
| 5    | 13239 ms | 376 ms | 764 ms | 1572 ms| 2287 ms   | 18240 ms|
| **Avg** | **15283 ms** | **375 ms** | **772 ms** | **1589 ms** | **2163 ms** | **20179 ms** |

### PCIe Summary

| Metric | Stock Kernel | Custom Kernel | Improvement |
|--------|--------------|---------------|-------------|
| **Average Total Boot Time** | 22737 ms (22.74 s) | 20179 ms (20.18 s) | **11% faster** |
| **Average Kernel Time** | 785 ms | 772 ms | 2% faster |
| **Average Loader Time** | 1171 ms | 375 ms | **68% faster** |
| **Average Firmware Time** | 15450 ms | 15283 ms | 1% faster |
| **Average Userspace Time** | 1975 ms | 2163 ms | 10% slower |
| **Initrd Time** | 3354 ms | 1589 ms | **53% faster** |

## Arch - USB Boot Time Measurements

### Stock Kernel (6.18.2-1-x86_64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 7160 ms  | 2491 ms| 776 ms | 4005 ms| 5055 ms   | 19490 ms|
| 2    | 7131 ms  | 2439 ms| 781 ms | 3553 ms| 10757 ms  | 24665 ms|
| 3    | 7160 ms  | 2600 ms| 787 ms | 3595 ms| 6259 ms   | 20402 ms|
| 4    | 7152 ms  | 2798 ms| 782 ms | 4174 ms| 6597 ms   | 21506 ms|
| 5    | 7169 ms  | 2675 ms| 774 ms | 3688 ms| 4844 ms   | 19153 ms|
| **Avg** | **7154 ms** | **2601 ms** | **780 ms** | **3803 ms** | **6702 ms** | **21043 ms** |

### Custom Kernel (6.18.1-1-x86_64-ARCH)

| Boot | Firmware | Loader | Kernel | Initrd | Userspace | Total |
|------|----------|--------|--------|--------|-----------|-------|
| 1    | 7157 ms  | 1440 ms| 752 ms | 2702 ms| 7115 ms   | 19168 ms|
| 2    | 7168 ms  | 700 ms | 752 ms | 2527 ms| 7152 ms   | 18299 ms|
| 3    | 7767 ms  | 792 ms | 762 ms | 2575 ms| 3329 ms   | 15227 ms|
| 4    | 7129 ms  | 1697 ms| 755 ms | 2774 ms| 4654 ms   | 17011 ms|
| 5    | 7169 ms  | 1621 ms| 754 ms | 2866 ms| 4758 ms   | 17169 ms|
| **Avg** | **7278 ms** | **1250 ms** | **755 ms** | **2689 ms** | **5402 ms** | **17375 ms** |

### USB Summary

| Metric | Stock Kernel | Custom Kernel | Improvement |
|--------|--------------|---------------|-------------|
| **Average Total Boot Time** | 21043 ms (21.04 s) | 17375 ms (17.38 s) | **17% faster** |
| **Average Kernel Time** | 780 ms | 755 ms | 3% faster |
| **Average Loader Time** | 2601 ms | 1250 ms | **52% faster** |
| **Average Firmware Time** | 7154 ms | 7278 ms | 2% slower |
| **Average Userspace Time** | 6702 ms | 5402 ms | **19% faster** |
| **Initrd Time** | 3803 ms | 2689 ms | **29% faster** |
