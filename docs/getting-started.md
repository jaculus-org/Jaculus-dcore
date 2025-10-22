# Getting started

## Setup

Make sure, you have [Node.js](https://nodejs.org) installed. The recommended version is 22 LTS or newer.

Next, install the Jaculus CLI tool by typing the following command in your terminal:

    $ npm install -g jaculus-tools@latest

Then, you can run the tools using the following command:

    $ npx jac

If you configure your environment PATH variable to include the npm global binaries directory, you can run the tools directly using:

    $ jac


To connect to the device using serial port, the correct driver must be installed — most likely [CP210x USB to UART Bridge](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers) or CH340. On some Linux distributions, CH340 may not be available unless you uninstall the `brltty` package.


### Installing Jaculus firmware to the device

Jaculus runtime must be installed on the device. A web installer is available at [https://installer.jaculus.org/](https://installer.jaculus.org/). The installer requires a modern web browser with WebSerial support (i.e., Chromium-based browsers such as Vivaldi, Google Chrome or Microsoft Edge).

1. Connect the device to your computer via USB.
2. Select the appropriate firmware for your device.
3. Press the "Connect" button.
4. Press the "Flash" button to install the firmware.
5. Wait until the installation is complete.

Verify that the runtime is installed correctly by running the following command in your terminal:

    $ npx jac version


## Connecting to the device

All commands interacting with the device require specifying the device connection using either `--port` or `--socket` option. These options are implied for the commands shown later in this guide.

To connect to the device using serial port, use:

    $ npx jac --port <port> <command>

To connect to the device using TCP socket, use:

    $ npx jac --socket <host>:<port> <command>

To list available serial ports, use:

    $ npx jac list-ports


## Creating and running TypeScript programs

You can create a new TypeScript project using the following command:

    $ npx jac project-create <project-path>

The command can either connect to a device running Jaculus and extract a template project using

    $ npx jac project-create --from-device <project-path>

or use an online template:

    $ npx jac project-create --package <package-url> <project-path>

In both cases, a new directory will be created at `<project-path>` containing the project files. All source files are located in the `src` subdirectory and `src/index.ts` is used as the entry point for the program.

To then run the program on the device, navigate to the project directory in your terminal and use:

    $ npx jac build flash monitor

This command will build the project, flash it to the connected device, and open a connection to the standard input/output of the program. To exit the monitor, press `Ctrl+C`.


## Updating

Jaculus-tools can be updated using the same command used for installation:

    $ npm install -g jaculus-tools@latest

Update of the Jaculus firmware can be performed in the same way as the initial installation using the web installer at [https://installer.jaculus.org/](https://installer.jaculus.org/).
