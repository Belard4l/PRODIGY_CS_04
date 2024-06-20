# Simple Keylogger

This project is a basic keylogger written in Python. It captures keystrokes and logs them to a specified file. The keylogger utilizes the `pynput` library to listen for keyboard events.

## Features

- Logs all keystrokes to a specified file.
- Captures special keys such as space, enter, and backspace.
- Customizable log file path through command-line arguments.

## Prerequisites

- Python 3.x
- `pynput` library

You can install `pynput` using pip if you don't have it already:

```bash
pip install pynput
```

## Usage

1. Clone the repository or download the script.

2. Run the script from the command line:

```bash
python keylogger.py --log-file <path_to_log_file>
```

If no log file path is specified, the keylogger will default to using `log.txt` in the current directory.

### Command-Line Arguments

- `--log-file`: Specify the path to the log file where keystrokes will be saved. If not specified, defaults to `log.txt`.

Example:

```bash
python keylogger.py --log-file keystrokes.log
```

## Code Explanation

### Imports

- `pynput.keyboard.Listener`: Listens for keyboard events.
- `argparse`: Parses command-line arguments.
- `os`: Provides a way of using operating system-dependent functionality.

### Functions

- `writeToFile(key, log_file)`: Writes the pressed key to the log file. It handles special keys such as space, enter, and backspace appropriately.
- `main()`: The main function that sets up the argument parser, ensures the log file exists, and starts the keylogger listener.

### Key Handling

- Special keys such as space, enter, and backspace are handled explicitly.
- Other special keys (e.g., shift, ctrl) are ignored.

### Listener

- The `Listener` from `pynput` is used to capture and log keystrokes. It runs in a blocking loop until interrupted.

## Stopping the Keylogger

To stop the keylogger, you can interrupt the process by pressing `Ctrl + C` in the terminal where the script is running. This will gracefully stop the listener and exit the program.

## Disclaimer

This keylogger is intended for educational purposes only. Unauthorized use of this script to log keystrokes without the consent of the user is illegal and unethical. Use it responsibly and only on systems you own or have explicit permission to monitor.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

---

By following the instructions and guidelines provided in this README, you should be able to set up and run the keylogger successfully. If you encounter any issues or have questions, feel free to reach out.
