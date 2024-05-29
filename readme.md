# Retro Game Console

The Retro Game Console project is designed to offer an interactive and immersive experience using a joystick, featuring a list of retro games. This console allows users to select and play games via the Mednafen emulator and supports automatic USB detection for adding new ROMs to the system.

## Features

### Game List Interface
The console displays a list of available games, navigable via a joystick. The interface is user-friendly, with visual cues to aid game selection.

### Mednafen Emulator Integration
This project integrates the Mednafen emulator, capable of running various ROM file formats, ensuring broad game compatibility.

### USB Detection and ROM Management
When a USB device is detected, the system mounts it, copies new ROMs to the designated directory, and then unmounts the USB. This automated process ensures a seamless user experience.

### Startup Sequence
Upon initialization, the system plays a startup image and sound, enhancing the retro gaming ambiance.

## Getting Started

### Prerequisites
Ensure you have Python 3.x installed on your system.

### Installation

Clone the repository:

```bash
git clone https://github.com/Possible-99/EmbeddedSystemsFinalProject.git
cd EmbeddedSystemsFinalProject
```

Grant permissions and run the setup script to install dependencies and configure settings:

```bash
chmod +x setup.sh
sudo ./setup.sh
```

### Running the Project

Start the application with:

```bash
sudo python app.py
```

## Usage

- Navigate the game list using the joystick.
- Press the A button to select a game.
- Insert a USB device with new ROMs to automatically copy them to the system.

## Code Overview

### State Management
The project uses a state pattern to manage different application states:

- **GameMenuState:** Displays the game list and handles game selection.
- **PlayingGameState:** Manages the state when a game is being played.

### USB Handling
The system uses `pyudev` to monitor USB events, managing the mounting, copying, and unmounting of USB devices.

### Mednafen Integration
A separate thread runs the Mednafen emulator, ensuring the main application remains responsive.
