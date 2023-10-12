# <img src="resources/hodhod.png" alt="Screenshot of HODHOD" width="30" height="30"> HODHOD

## Table of Contents
- [ HODHOD](#-hodhod)
      - [Video Demo: Watch Video](#video-demo-watch-video)
  - [Features](#features)
  - [Installation](#installation)
  - [Installation](#installation-1)
    - [For Windows Users](#for-windows-users)
    - [For macOS Users](#for-macos-users)
    - [For Linux Users](#for-linux-users)
      - [Note](#note)
  - [Getting Started](#getting-started)
  - [Built With](#built-with)
  - [Future Enhancements](#future-enhancements)
  - [Contributing](#contributing)
  - [License](#license)
  - [Contact](#contact)
- [HODHOD Project](#hodhod-project)  
  - [Main Files and Their Purpose](#main-files-and-their-purpose)
    - [project.py](#projectpy)  
    - [activateCode.py ](#activatecodepy)
    - [hod.py ](#hodpy)
    - [hodhod\_animation.py ](#hodhod_animationpy)
    - [hodhod\_classes.py ](#hodhod_classespy)
    - [hodhod\_functions.py ](#hodhod_functionspy)
    - [hodhod\_SentData.py ](#hodhod_sentdatapy)
    - [hodhod\_style.py ](#hodhod_stylepy)
    - [sentAndReciveClass.py ](#sentandreciveclasspy)
    - [serial.py ](#serialpy)
    - [serialFile.py ](#serialfilepy)
    - [temporaryMemory.py ](#temporarymemorypy)
    - [test\_project.py ](#test_projectpy)
 
---



#### Video Demo: [Watch Video](https://youtu.be/z-J3yhMoPUg)

Welcome to Hodhod, an innovative file transfer and chat application designed to seamlessly connect devices over a Wi-Fi network. Developed with Python, Hodhod autonomously identifies devices on the network, updating IP addresses as they change, and presenting an intuitive user interface for effortless communication and file sharing.

## Features

- **Auto Device Discovery**: Automatically identifies and updates devices connected on the same Wi-Fi network.
- **User Friendly**: Engage with an interactive window where the UI size and background color can be altered.
- **Server Exploration**: Moving bars indicate Hodhod’s exploration of connected servers, which takes a user-determined duration between 10 and 34 seconds.
- **Device List**: View and connect with up to 255 devices, each showing its name and icon.
- **Interactive Chat and File Sharing**: Use a designated space for message writing and file sharing, with drag-and-drop functionality.
- **Received Files**: Easy access and opening of received files with a simple click.
- **Settings Control**: Manage the program background, user information, search speed, language, and registered servers.
- **Cross-Platform**: Initially designed for computers and Windows OS.

## Installation
## Installation

### For Windows Users

1. **Download the Installer**: Navigate to the [releases page](https://github.com/tarekammari//HODHOD) of Hodhod and download the latest version of the installer, [`HODHOD_setup_V1.1.4`](https://github.com/tarekammari//HODHOD).


2. **Run the Installer**: Locate the downloaded `HODHOD_setup_V1.1.4` file in your Downloads folder (or wherever you saved it) and double-click it to run the installer.

3. **Follow the Installation Wizard**: Follow the instructions in the installation wizard. Select the destination folder and click "Next" through the wizard, then click "Install" to install Hodhod.

4. **Launch Hodhod**: Once the installation is complete, launch Hodhod either from the Start menu or the Desktop shortcut, if you chose to create one.

### For macOS Users

_// (If applicable) Add instructions for macOS users._

### For Linux Users

_// (If applicable) Add instructions for Linux users._

#### Note

- Ensure that your device is connected to the Wi-Fi network during installation and usage of Hodhod.
- Upon first use, you'll be prompted to enter a name and password, which will be visible to all devices it connects to. You can update these details later within the program.



## Getting Started

1. **Initial Setup**: Upon first use, enter your name and a password. These details will be visible to all devices you connect to and can be updated through the program.
2. **Connect to a Server**: Select the desired server from the displayed list.
3. **Send Files and Messages**: Drag and drop files into the designated space and type your messages for chat.
4. **Receive Files**: Click on received files to open them. By clicking on the server icon, access the folder containing all files sent by it.





## Built With

- [Python](https://www.python.org/)
- [Socket](https://docs.python.org/3/library/socket.html) - For connection management
- [PySide](https://www.pyside.org/) - For user experience

## Future Enhancements

- Extend compatibility to additional operating systems and devices.
- Implement enhanced security features for secure file transfers and communications.
- Add multi-language support.
  
## Contributing



## License

[license](license.txt)





## Contact

<img src="resources/gmail.png" alt="Screenshot of HODHOD" width="30" height="25">   [Tarek AMMARI](mailto:tarekammari1@gmal.com)

---

# HODHOD Project

HODHOD is a project that [provide a brief description of your project here].



# Main Files and Their Purpose 


# project.py 
This is the main executable file for the HODHOD project. It utilizes the `MainWindow(QMainWindow)` class to initialize and display the main application window, manage GUI widgets, buttons, and text edit functionalities. It also handles various UI events and interacts with other modules to perform specific tasks, such as authentication and data management. It plays a pivotal role in initiating the application and managing user interactions with the GUI.


# activateCode.py 

### Overview 

The `activateCode.py` script is pivotal in managing serial numbers, crucial for the software activation process in the HODHOD project. It encompasses functionalities that facilitate the encryption and decryption of data, generation, validation, and updating of serial numbers, and also contains logic to check whether the serial number adheres to specified criteria. 

### Detailed Workflow 

1. **Decrypting and Loading Data**: 
   - The script reads encrypted data from a file, decrypts it, and loads it into a Python dictionary for further processing.
   
2. **Serial Number Update and Management**: 
   - If a change is flagged (`data["CHANGE"] == 1`), a new serial number is generated and updated in the data. 
   - The `data["CHANGE"]` flag is then set to 0 and the updated data (including the new serial number) is encrypted and written back to the file.
   - If no change is flagged, the existing serial number is used.

3. **Serial Number Validation**: 
   - The script ensures that the serial number adheres to specific requirements regarding the count of digits, uppercase letters, lowercase letters, and special characters.

4. **Diamond Logic Implementation**: 
   - The `diamond()` and `diamonds()` functions manipulate the serial number to create specific 'diamond' patterns, used for undisclosed purposes (likely related to further validation or use in other parts of the software).
   - This involves intricate logic with serial number character positioning and repositioning, possibly to generate specific codes or keys.

5. **Additional Utilities**: 
   - The script also contains functionality to transform and manipulate the serial number into various formats as required for different aspects of the software.

### Key Functions

- `validate_serial(serial)`: Validates the serial number based on specific criteria.
- `diamond()`: Generates a list of 'diamond' patterns based on the serial number characters.
- `diamonds()`: Further manipulates the serial number characters to generate additional patterns or codes.
- `serialForTextEdit()`: A utility function to retrieve the serial number, possibly for display or use within a text edit field in a GUI.

### Important Notes 

Understanding the detailed logic within the `diamond` generation and usage, and the specific use cases of the manipulated serial number in other parts of the software, might require further exploration and documentation.


[Description of activateCode.py]

## hod.py <a name="hodpy"></a>
hod.py serves as a pivotal module in the HODHOD project, primarily responsible for constructing, managing, and handling user interactions within the Graphical User Interface (GUI) of the application. Importantly, it utilizes various widgets and UI elements from the PySide2 (Qt for Python) library to render a user-friendly interface that facilitates seamless user engagement with the application's features. Below are some of the key aspects and functionalities managed by hod.py:

- **User Interface Creation and Management**: The file encompasses the creation of various UI elements like labels, frames, buttons, and text edits, aligning them in structured layouts to offer a clean and intuitive user experience.
- **Threading for Asynchronous Operations**: It incorporates threading to manage potentially blocking operations, such as socket communications, ensuring that the UI remains responsive and fluid during runtime.
- **Inter-Module Interactions**: hod.py interacts with several other modules like hodhod_animation and hodhod_style to achieve visually appealing animations and styles within the UI, enhancing the aesthetic and interactive aspects of the application.
- **Socket Communications**: Though not explicitly evident in the initial code snippet, there might be functionalities related to socket programming, facilitating the core communication capabilities of HODHOD, enabling it to connect and communicate across devices on a network.
- **User Input and Event Handling**: Manages user inputs, events, and interactions, ensuring appropriate responses and actions are taken within the application, including updates to the UI and initiation of communication protocols.
- **Settings and Configurations Management**: Likely to manage user configurations and settings, potentially allowing users to customize aspects of the application according to their preferences.

This file is crucial in enabling users to interact with the underlying functionalities of the HODHOD application, providing a bridge between the user and the technical operations occurring in the background.
# hodhod_animation.py 

### hodhod_animation.py <a name="hodhod_animationpy"></a>

The `hodhod_animation.py` module is dedicated to handling and managing animations within the HODHOD application. While ensuring smooth and visually appealing user experience, this file incorporates functionalities that provide dynamic visual feedback and interactive animations in the GUI. Here are some key aspects:

- **Dynamic Visual Elements**: It introduces dynamic elements into the UI, such as moving bars, to showcase the process of exploring connected servers and other interactive animations, enhancing user engagement.
  
- **User Feedback**: Through animations, it provides visual feedback in response to user actions and system processes, such as file transfers, message sending, and server discovery, providing intuitive and clear indications of ongoing activities within the application.

- **Visual Aesthetics**: It plays a crucial role in enhancing the visual aesthetics of the application, contributing to a polished and professional appearance, and aiding in user navigation and interaction.

- **Enhanced User Interaction**: Animations can also serve to guide the user's attention and interactions, subtly indicating available actions and prompting user engagement in a visually guided manner.

This module, while potentially lightweight, significantly enhances user interaction and experience by providing a dynamic, responsive, and visually enriched interface, contributing to the overall usability and appeal of the HODHOD application.

# hodhod_classes.py 


## Overview

`hodhod_classes.py` is a Python script developed to create a GUI application using the PySide2 library, which is the official set of Python bindings for Qt libraries. The script seems to implement functionalities related to graphical user interface creation, networking, and potentially secure data communication.

## Description

### Imports and Dependencies
- **GUI-related Libraries:** Various modules from PySide2 are employed to facilitate GUI creation, including `QApplication`, `QLabel`, `QVBoxLayout`, `QHBoxLayout`, `QLineEdit`, `QPushButton`, `QWidget`, `QFileDialog`, and others.
- **Other Libraries:** The script utilizes several standard Python libraries and modules, such as `sys`, `io`, `os`, `json`, `socket`, `threading`, `math`, and `cryptography.fernet`.
- **Custom Module:** A custom module named `hodhod_style` is imported, presumably to apply specific styles to the GUI components.

### GUI Styling
- Various GUI components are likely styled using elements imported from `hodhod_style`, potentially affecting elements like buttons and labels.

### Networking and Threading
- The application implies the use of networking functionalities, considering the import of `socket` and `threading`. It might operate on client-server communication principles, as suggested by defined `CLIENT_HOST` and `SERVER_PORT` variables.

### Encryption
- The script seems to implement cryptographic operations by importing `Fernet` from the `cryptography` package, potentially securing data transmission across the network.

## Requirements
- **Python:** Ensure that Python is installed on your system.
- **PySide2:** Utilized for GUI creation.
- **Cryptography:** Employed for potential encryption and decryption functionalities.
- **Additional Libraries:** Ensure additional standard and custom Python libraries/modules are available.




# hodhod_functions.py 

## Overview

This Python script utilizes the `PySide2` library and various other modules to perform GUI operations and possibly some network and system-level tasks. 

## Imports

- **GUI Components and Functionalities**: Utilizes `PySide2` to work with various widgets and functionalities like `QMessageBox`, `QFileDialog`, etc.
- **Threading**: Employs `threading` for possibly managing concurrent operations.
- **System and Process Management**: Uses `psutil` and `subprocess` for managing system processes.
- **Network Communication**: Utilizes `socket` for network-related tasks.
- **Data Handling**: Uses `json` for handling JSON data.
- **Cryptography**: Employs `cryptography` for some encryption functionalities.
- **Custom Styles and Classes**: Imports styles from `hodhod_style` and classes from `hodhod_classes`.


# hodhod_SentData.py 

## Overview

The script `hodhod_SentData.py` is involved with networking and cryptography functionalities, possibly related to sending data over a network in an encrypted format.

## Imports

- **Networking**: Utilizes `socket` for network communications.
- **Data Handling**: Employs `json` for managing JSON data.
- **Operating System Interactions**: Uses `os` for various OS-level operations.
- **Cryptography**: Employs `cryptography` for encryption and decryption tasks.
- **Custom Classes**: Imports `BtnWidget` from `hodhod_classes`.

## Constants and Variables

- Networking-related: `CLIENT_HOST`, `SERVER_PORT`, `FORMAT`, `HEADER`, `D`, `who_connect`, `SEPARATOR`, `ADDR`.
- Cryptography-related: `KEY`, `cipher`.

## Data Decryption

The script attempts to read, decrypt, and parse JSON data from a file named `user.py`.

## Functions

### send_DATA(self, send_files_edit, label_IpOfServerSlected, progressBarrForSendData_signal, progress_SendingBar, edit_FilterServersByCharacters, vlayout_ContainsButtonsAndServerNamesAndIc...)

This function takes multiple parameters and seems to be related to sending data, likely over a network, although further details would require a deeper analysis.




# hodhod_style.py

## Overview

This Python script, `hodhod_style.py`, manages the styling of a GUI application, likely developed using PyQt or PySide.

## Class Definitions

### `StyleSheet`

#### Description

Manages styles in a concatenated string format.

#### Methods

- `__init__(self)`: Initializes a new instance, setting up a string to hold styles.
- `add_style(self, style)`: Adds a new style to the instance's string of styles.
- `get_style(self)`: Retrieves the instance's concatenated string of styles.

## Styling Variables and Objects

### Background Colors

- `background_centralWidgetRight`: Defined color likely used for styling.
- `background_centralWidgetMiddle`: Another defined color.
- `background_centralWidgetLeft`: Yet another defined color.

### Styling Sheets

Instances of `StyleSheet` are defined and configured with various gradient and color styling information:

- `central_widget_style`: Configured with a linear gradient background.
- `darkMode_style`: Configured with a different linear gradient background.



# sentAndReciveClass.py 

## Overview

The Python script `sentAndReciveClass.py` is associated with GUI development, possibly related to sending and receiving messages or data, using the PySide2 library and handling notifications via `winotify`.

## Imports

### GUI Components and Functionalities

- Utilizes various GUI components and functionalities from `PySide2`.
  
### Notifications

- Utilizes `Notification` and `audio` from `winotify` for handling notifications.

### Image Handling

- Employs `QPixmap` for potential image handling in the GUI.

### Data Handling and Time

- Uses `json` for managing JSON data and `datetime` for time-related functionalities.

### Styling and Custom Classes

- Imports various styling elements from `hodhod_style` and custom classes from `hodhod_classes`.

## Class Definitions

### `SentReciveClass`

#### Description

A class potentially related to sending and receiving data or messages within a GUI context. 

#### Methods

- `__init__(self)`: Initializes an instance of `SentReciveClass`. The full functionality needs further exploration.




# serial.py 



## Overview

The Python script `serial.py` defines a class for generating a serial number using random components.

## Imports

### Randomization

- Utilizes `random` and `string` for generating random strings.

## Class Definitions

### `SerialNumberGenerator`

#### Description

A class designed to generate a serial number using random strings of different character types.

#### Methods

##### `generate_serial()`

- **Description**: Generates a random serial number.
- **Return**: Returns a string that represents the generated serial number.
- **Details**: 
    - Generates 5 random digits, 5 random uppercase letters, 5 random lowercase letters, and 5 random special characters.
    - Combines and shuffles these strings to produce a serial number.

# serialFile.py 

## Overview

The file `serialFile.py` contains a single string of data which appears to be encrypted or serialized and encrypted:


# temporaryMemory.py 
[Description of temporaryMemory.py]

# test_project.py 

## Overview

The Python script `test_project.py` appears to be used for testing purposes, specifically testing certain functions from a module named `hodhod`.

## Imports

### Functions from `hodhod`

- `dataJson`
- `checkSerialFile`
- `resourcesFolder`

## Test Functions

### `test_dataJson()`

- **Description**: Tests the `dataJson` function from `hodhod`.
- **Returns**: `True` if `dataJson` returns a truthy value.

### `test_checkSerialFile()`

- **Description**: Tests the `checkSerialFile` function from `hodhod`.
- **Returns**: `True` if `checkSerialFile` returns a truthy value.

### `test_resourcesFolder()`

- **Description**: Tests the `resourcesFolder` function from `hodhod`.
- **Returns**: `True` if `resourcesFolder` returns a truthy value.
