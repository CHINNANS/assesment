# Serial Communication with Bluetooth Module

This C program demonstrates how to read data from a Bluetooth module connected to a serial port on a Windows system. The program uses the Windows API for serial communication.

## Prerequisites

- Windows operating system
- [Bluetooth module](#) connected to a serial port (COMx)
- [Visual Studio](#) or another C compiler

## Getting Started

1. Clone the repository or download the source code.

    ```bash
    git clone https://github.com/CHINNANS/assesment.git
    ```

2. Open the project in your preferred C development environment.

3. Build the project to generate the executable.

## Usage

1. Connect your Bluetooth module to a serial port on your computer.

2. Run the compiled executable.

    ```bash
    ./serial-communication.exe
    ```

3. Monitor the console output for received data from the Bluetooth module.

## Configuration

- Modify the `COM7` parameter in the code to match the actual COM port of your Bluetooth module.

    ```c
    // Replace "COM7" with the actual COM port of your Bluetooth module
    hSerial = CreateFile("COM7", GENERIC_READ, 0, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    ```

- Adjust the baud rate and other serial port parameters if necessary.

    ```c
    // Set serial port parameters (baud rate, data bits, stop bits, parity)
    dcbSerialParams.BaudRate = CBR_9600;
    dcbSerialParams.ByteSize = 8;
    dcbSerialParams.StopBits = ONESTOPBIT;
    dcbSerialParams.Parity = NOPARITY;
    ```

## Contributing

1. Fork the repository.
2. Create a new branch for your feature: `git checkout -b feature-new-feature`.
3. Commit your changes: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature-new-feature`.
5. Submit a pull request.
