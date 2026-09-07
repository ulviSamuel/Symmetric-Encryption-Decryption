# Symmetric Encryption and Decryption   

A Java 17 command-line application for encrypting and decrypting text with DES in ECB or CBC mode.

![Java 17](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Command-line application](https://img.shields.io/badge/Type-Command--line%20application-4C566A?style=flat-square)
![Academic Project](https://img.shields.io/badge/Category-Academic%20Project-5E81AC?style=flat-square)
![Year | 2024](https://img.shields.io/badge/Year%20%7C%202024-8FBCBB?style=flat-square)

> [!NOTE]
> This repository contains an academic project originally developed during earlier programming studies. It is preserved as a record of the technical knowledge, design decisions and development experience acquired at the time.

## Overview

The application presents an interactive console menu for choosing encryption or decryption, selecting the DES/ECB/PKCS5Padding or DES/CBC/PKCS5Padding transformation, and entering a text message. Ciphertext is displayed as Base64.

The implementation is an educational example rather than a production security tool. DES is an obsolete encryption standard, and the generated key and CBC initialization vector remain in memory for the current process instead of being persisted or exchanged.

## Features

- Encrypts text with DES in ECB mode.
- Encrypts text with DES in CBC mode using a randomly generated initialization vector.
- Decrypts ECB and CBC ciphertext during the same application run.
- Encodes encrypted bytes as Base64 for console display and accepts Base64 ciphertext as input.
- Validates menu selections and supports cancelling text input by pressing Enter.

## Technology stack

- **Language:** Java
- **Runtime/API:** Java Cryptography Architecture (`javax.crypto`, `java.security`)
- **Interface:** Interactive standard-console input and output
- **Build configuration:** Eclipse project metadata targeting Java 17
- **External dependencies:** None declared in the repository

## Project structure

```text
CifrDecifSimmetrica/
├── src/
│   └── it/volta/ts/ulivisamuel/cifrdecifrulivi/
│       ├── Main.java                 # Application entry point
│       ├── Console.java              # Interactive menu and input flow
│       ├── biz/                      # ECB and CBC cipher implementations
│       ├── events/                   # Console notification types
│       └── util/                     # Input-validation helpers
├── .classpath                        # Eclipse Java 17 classpath
└── .project                          # Eclipse Java project definition
```

## Getting started

### Prerequisites

- A Java Development Kit (JDK) 17.

The repository explicitly configures Eclipse compilation for Java 17. No package manager or third-party dependency installation is required.

### Compile

From the repository root:

```bash
mkdir -p /tmp/cifrdecif-simmetrica-bin
javac -d /tmp/cifrdecif-simmetrica-bin $(find CifrDecifSimmetrica/src -type f -name '*.java')
```

### Run

After compiling:

```bash
java -cp /tmp/cifrdecif-simmetrica-bin it.volta.ts.ulivisamuel.cifrdecifrulivi.Main
```

Use the displayed menus to choose encryption or decryption, then select ECB or CBC and enter a message. Decryption is available only after the corresponding cipher instance has generated its key, so ciphertext produced in a separate process cannot be decrypted by this application.

## Testing

No automated test suite is included in the repository. A successful `javac` compilation is the available build validation path.

## License

This project is shared for educational and portfolio purposes. All rights reserved unless otherwise stated.
