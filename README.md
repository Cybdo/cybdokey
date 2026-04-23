# CybdoKey
A RP2354 based usb hardware authentication key, or anything else you can write firmware for ;)


<img width="1270" height="720" alt="render showing front and back of cybdokey" src="https://github.com/user-attachments/assets/c995826c-fcd9-4199-bcff-b1967f765c89" />

Cybdokey was made because yubikeys are too expensive and all the other options, including picofido on other devboards, were clunky. the user interaction button was tiny and hard to press, and depending on the board it was too big and/or needed an extra cable. Cybdokey was made to be a polished, compact FIDO key with capacative touch support.


**Note:** `bom.csv` is the LCSC parts list with working liks, whilst `overall-bom.csv` is an estimate of the overall project cost

## Zine Page / Poster

pdf in `assets/zine/Zine page.pdf`

<img width="401" height="614" alt="Zine page" src="https://github.com/user-attachments/assets/e01f9577-dfe1-4d3a-9f2e-a00efa33b71d" />


## Features
- RP2354-based development board
- Stacked 2MB flash storage
- onboard USB-A connector
- Capacative touch pad with shine-through red and blue LEDs
- exposed 3V3, GND, RESET and BOOTSEL
- 2 keyring/accessory mount holes
- Hand-solderable (in theory)
- tiny form factor!
<img width="1270" height="720" alt="render showing the backside of cybdokey" src="https://github.com/user-attachments/assets/33fe673f-e43e-420d-80b9-66b2a31928ed" />

## Usage

Simply plug Cybdokey into your computer's USB-A port, and it will function similar to a yubikey. Passkeys and OTPs can be stored on it, and it supports human presence detection using the capacative touch pad. LED signals are identical to that of any other pico-fido key.

## Schematics
<img width="1287" height="990" alt="image" src="https://github.com/user-attachments/assets/46e68c64-a258-42bd-bf8f-d22971f3334f" />

## PCB

|Front|Back|
|---|---|
|<img width="245" height="858" alt="image" src="https://github.com/user-attachments/assets/a06eb7f3-8f91-4e6a-a017-e931db1f4d0c" /> | <img width="242" height="850" alt="image" src="https://github.com/user-attachments/assets/b3294d04-dc3b-432f-8b6a-537a3a903951" />|

## Firmware

See [https://github.com/cybdo/cybdokey-fw](https://github.com/cybdo/cybdokey-fw) for FIDO key firmware.

Firmware can be flashed on first boot, or by shorting the BOOTSEL jumper on the left side of the crystal, diagonally underneath the MCU, before booting.

CybdoKey is also compatiable with anything written for a RP2350/RP2354.


## Credits and Acknowledgements

 - [KiCad](https://www.kicad.org)
 - [Hack Club Fallout](https://fallout.hackclub.com)
 - [pcb2blender](https://github.com/30350n/pcb2blender)
 - [Blender](https://blender.org)
 - [MicroKey](https://github.com/Badbird5907/microkey)
 - [Pico FIDO](https://github.com/polhenarejos/pico-fido), forked to make [CybdoKey firmware](https://github.com/cybdo/cybdokey-fw)
