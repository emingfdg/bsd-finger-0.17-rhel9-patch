# bsd-finger-0.17-rhel9-patch

This repository provides a compatibility patch for building [`bsd-finger-0.17`](https://ibiblio.org/pub/Linux/system/network/finger/bsd-finger-0.17.tar.gz) on **RHEL 9**, **AlmaLinux 9**, and **Rocky Linux 9** systems.

## Overview

The original `bsd-finger-0.17` was released in the early 2000s and does not compile cleanly on modern Linux systems due to:

- Deprecated or incompatible header files (e.g. `<sys/time.h>`)
- Missing initialization of pointers leading to segmentation faults
- Stricter modern compilers and glibc behavior

This patch resolves those issues.

---

## How to Use

1. **Download the original source**  
   Source: [bsd-finger-0.17.tar.gz](https://ibiblio.org/pub/Linux/system/network/finger/bsd-finger-0.17.tar.gz)

2. **Extract the source**

```bash
tar xvf bsd-finger-0.17.tar.gz
```

3. **Apply the patch**

```bash
patch -p1 -d bsd-finger-0.17 < patch.diff
```

4. **Build**

```bash
cd bsd-finger-0.17
./configure
make
```

5. **Test**

```bash
./finger/finger $(whoami)
```

---

## Changes in This Patch

- Replaced `<sys/time.h>` with `<time.h>` in:
  - `finger/lprint.c`
  - `finger/sprint.c`
- Added initialization of `pn->realname = NULL;` in `finger/util.c` to prevent crash when GECOS field is empty

---

## Compatibility

Tested on:

- AlmaLinux 9.6
- glibc 2.34
- GCC 11.4+

---

## Maintainer

Akira Endo endoaki@jl1fbd.org
June 30, 2025

This repository contains only the patch file and documentation. Original source code is property of its respective authors.
