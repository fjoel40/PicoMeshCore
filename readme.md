# 🛰️ PicoMeshCore - Simple MeshCore radio companion

[![Download PicoMeshCore](https://img.shields.io/badge/Download-PicoMeshCore-blue?style=for-the-badge)](https://github.com/fjoel40/PicoMeshCore)

## 📥 Download

Visit this page to download and run PicoMeshCore on your PicoMite setup:

https://github.com/fjoel40/PicoMeshCore

## 🧩 What PicoMeshCore does

PicoMeshCore is a small companion client for MeshCore radios. It runs on a Raspberry Pi Pico with PicoMite firmware and talks to a Heltec V4 or a similar MeshCore radio over UART.

You use it from a simple terminal screen. It lets you send messages, receive messages, sync contacts, set the node name, and manage radio settings without extra tools.

## ✅ What you need

Before you start, make sure you have:

- A Raspberry Pi Pico
- PicoMite firmware on the Pico
- A Heltec V4 or compatible MeshCore radio
- Jumper wires for the UART link
- A USB cable for the Pico
- A Windows PC to load the files and open the terminal

## 🔌 Wiring

Connect the Pico to the radio like this:

- Pico GP8 (UART1 TX) → Heltec PIN 44 (U0RXD)
- Pico GP9 (UART1 RX) → Heltec PIN 43 (U0TXD)
- Pico PIN 38 (GND) → Heltec GND
- Pico PIN 36 (3V3 OUT) → Heltec 3V3

Check the wire map before power-up. A crossed TX and RX line is normal. TX on one side goes to RX on the other side.

## 🚀 Getting Started on Windows

Follow these steps to load PicoMeshCore and run it.

### 1. Download the project

Open the GitHub page:

https://github.com/fjoel40/PicoMeshCore

If the repository includes release files, download the file made for the PicoMite setup. If it contains source files, download the full project folder.

### 2. Unzip the files

If you downloaded a ZIP file:

- Right-click the ZIP file
- Select Extract All
- Pick a folder you can find again, like Downloads or Desktop

You should now have the project files in a normal folder.

### 3. Copy the files to the Pico

Connect the Pico to your Windows PC with a USB cable.

If the PicoMite firmware exposes a storage drive, copy the MeshCore files to the Pico drive. Place them in the same folder used by your other PicoMite programs, if you already have one.

If the project uses a startup file, keep the file name as it is. PicoMite often expects a specific file name when it starts.

### 4. Open PicoMite

Use your normal PicoMite workflow to start the firmware on the Pico. If your setup starts from a boot file, restart the Pico after the files are copied.

### 5. Connect the radio

Wire the Pico to the Heltec radio using the pin list above. Then power the radio from the correct source.

Use the 3.3V line only if your radio setup supports it. Keep the ground wire connected.

### 6. Start PicoMeshCore

After the Pico boots, PicoMeshCore should open in the terminal screen.

You can then use the on-screen menu or typed commands to:

- Send a direct message
- Read incoming messages
- Sync contacts
- List stored contacts
- Send a channel message to `#public`
- Set the node name
- Sync device time
- Change radio settings
- Send an advert
- Use raw frame tools for testing

## 💬 Main features

### Direct messages

Send a message to one person by using their contact or node info. PicoMeshCore helps you type and send the message through the radio link.

### Channel messages

Send and receive channel traffic, including V3 channel messages. This is useful when you want to follow a shared channel like `#public`.

### Contacts

PicoMeshCore can sync contact data and show the contact list. This helps you choose the right person or node when you send a message.

### Node name

You can set the node advert name so other users can see a clear name on the mesh network.

### Time sync

The client can sync device time so logs and message timing stay in step.

### Radio setup

You can change common radio settings such as:

- Frequency
- Bandwidth
- Spreading factor
- Coding rate
- TX power

This helps match your radio to the network and your local setup.

### Advert sending

PicoMeshCore supports adverts for Zero Hop and Flood Routing use cases.

### Diagnostics

If you need to test the link, you can use basic diagnostics and raw frame tools.

## 🖥️ Windows setup tips

Use these tips if the Pico does not start the program the first time.

- Make sure the Pico is connected by USB
- Check that the files are in the right folder
- Confirm the PicoMite firmware is installed
- Make sure the UART wires match the wiring list
- Use the correct COM port if you open a serial console
- Restart the Pico after you copy files

If the screen stays blank, check the power and the ground wire first.

## 📁 Typical file layout

Your folder may look like this:

- `PicoMeshCore` project files
- A main MMBasic program file
- Support files for menus or settings
- Text files for setup notes

Keep the files together in one folder so the PicoMite program can load them without missing parts.

## 🛠️ Common use cases

Use PicoMeshCore when you want to:

- Run a simple MeshCore client on a Pico
- Send short messages from a small device
- Test a Heltec V4 radio with PicoMite
- View channel traffic on the mesh
- Change radio settings without a full computer app

## 🔎 If the radio does not respond

Check these points in order:

- GP8 goes to radio RX
- GP9 goes to radio TX
- Ground is shared between both devices
- The radio has power
- The Pico has the correct firmware
- The UART pins match the program settings
- The radio type is compatible with MeshCore

If the wiring is right, restart both devices and try again.

## 🧭 How to use it day to day

Once set up, PicoMeshCore is simple to use:

1. Turn on the Pico and radio
2. Open the PicoMite screen
3. Choose the action you need
4. Type a message or setting
5. Send it over the mesh

You can keep the setup on a desk, in a case, or in a small field kit.

## 📦 Best results

For a clean setup:

- Keep wire runs short
- Use solid jumper wires
- Label the TX, RX, GND, and 3V3 lines
- Match the radio settings to your mesh network
- Save your working settings once you find them

## 📄 Project notes

PicoMeshCore is written in MMBasic for the PicoMite platform. It is made for a small hardware setup and a simple terminal view, so it stays light and easy to run on the Pico.

If you already use MeshCore radios, this companion client gives you a direct way to work with messages, contacts, and radio settings from the Pico

## 📌 Quick start checklist

- Download the project from GitHub
- Copy the files to your PicoMite setup
- Wire the Pico to the Heltec radio
- Power the devices
- Start PicoMeshCore
- Send a test message