# STM32F429I Discovery CMake Project with LVGL Integration

This project demonstrates how to set up a **CMake-based development environment** for the **STM32F429I Discovery** board and integrate it with the **LVGL (Light and Versatile Graphics Library)**. The project successfully runs an LVGL example on the STM32F429I board.

---

## Features

- **CMake-based Project Management**:
  - Portable and modular build system, easy to configure and maintain.
  - Supports cross-platform development workflows with **CMake Presets**.
- **LVGL Integration**:
  - Demonstrates the use of the LVGL library for graphical user interface (GUI) development.
- **Hardware Support**:
  - Fully supports the STM32F429I Discovery board.
- **VSCode Development Environment**:
  - Includes configurations for **VSCode** with **CMake Tools**.

---

## Project Structure
```
├── Core/ # Main application code 
│   ├── Src/ # Source files for the application 
│   └── Inc/ # Header files for the application 
├── Drivers/ # STM32 HAL and BSP drivers 
├── ext/ # External libraries managed by FetchContent 
│   └── lvgl/ # LVGL library (fetched dynamically via CMake)
├── cmake/ # CMake configuration files 
├── .vscode/ # VSCode configuration for build and flash 
├── mx_f429i_disco.ioc # STM32CubeMX configuration file 
├── CMakeLists.txt # Main CMake configuration file 
├── STM32F429ZITx_FLASH.ld # Linker script 
├── startup_stm32f429xx.s # Startup code 
└── README.md # Project documentation
```

---

## CMake Setup and Workflow

This project leverages **CMake** to manage the build process for STM32 projects. Additionally, the **STM32 for VS Code Extension** simplifies the workflow by integrating STM32CubeMX and debugging tools into the VSCode environment.

### Key Features

1. **CMake and STM32 for VS Code**:
   - Manages the build process with **CMake** for portability and modularity.
   - Uses the **STM32 for VS Code Extension** to streamline STM32CubeMX and debugging configurations.

2. **Toolchain Integration**:
   - Configured for the `arm-none-eabi-gcc` toolchain provided by the **STM32CubeIDE** or **GNU Arm Embedded Toolchain**.

3. **LVGL Integration**:
   - Use CMake to fetch and build the **LVGL** library as part of the project.

---

### Prerequisites

1. **Install Visual Studio Code**:

2. **Install STM32 for VSCode Extensions**:
   - Install the following extensions:
     - **CMake Tools**
     - **STM32 for VSCode**
3. **Toolchain Setup**:
   - Install the [GNU Arm Embedded Toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm).
   - Ensure `arm-none-eabi-gcc` is added to your system's `PATH`.
---

### Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/SubWorkGit/mx_f429i_disco_11123.git
   ```
2. **Open the Project in VSCode**
3. **Configure the Build System**
4. **Build the Project**
5. **Flash the Program**
    - Use tools like **STM32CubeProgrammer** or other flashing utilities to upload the binary to your STM32F429I Discovery board.
