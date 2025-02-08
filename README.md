# MLG-OS

This repository contains the source code and documentation for the MLG-OS project. The project is organized into several directories to keep the files well-structured and easy to navigate.

## Repository Structure

The repository is organized as follows:

- `src/`: Contains the source code files for the MLG-OS project.
  - `CP.ASM`: Assembly code for the CP/M operating system.
  - `boot_sect.asm`: Assembly code for the boot sector.
  - `UNKNOWN_0.asm`: Assembly code for an unknown component.

- `docs/`: Contains the documentation files for the MLG-OS project.

- `build/`: Contains the build scripts for the MLG-OS project.

- `LICENSE`: The license file for the MLG-OS project.

## Getting Started

To get started with the MLG-OS project, follow the instructions below:

1. Clone the repository:
   ```
   git clone https://github.com/Mario9501/MLG-OS.git
   ```

2. Navigate to the project directory:
   ```
   cd MLG-OS
   ```

3. Build the project:
   ```
   nasm -f bin src/boot_sect.asm -o build/boot_sect.bin
   nasm -f bin src/CP.ASM -o build/CP.bin
   nasm -f bin src/UNKNOWN_0.asm -o build/UNKNOWN_0.bin
   cat build/boot_sect.bin build/CP.bin build/UNKNOWN_0.bin > build/MLG-OS.img
   ```

4. Run the project:
   ```
   qemu-system-x86_64 -drive format=raw,file=build/MLG-OS.img
   ```

## Contributing

Contributions are welcome! If you would like to contribute to the MLG-OS project, please follow the guidelines below:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push the branch to your forked repository.
4. Create a pull request with a description of your changes.

## License

This project is licensed under the [Unlicense](LICENSE).
