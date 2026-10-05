# Honeycomb Bravo Lite Support

This fork adds Windows support for the Honeycomb Bravo Lite landing gear indicator LEDs when using X-Plane 12.

## What was added

The Bravo Lite uses a different USB product ID and HID interface/report structure than the original Honeycomb Bravo Throttle Quadrant.

This modification adds support for the Bravo Lite USB device and communicates with its dedicated LED HID collection.

### Landing gear LED behavior

The three landing gear indicators operate as follows:

- **Green** - Gear down and locked
- **Red** - Gear in transit
- **Off** - Gear fully retracted

## Tested configuration

- Honeycomb Bravo Lite
- X-Plane 12
- Windows
- Tested with the default Beechcraft Baron 58 profile

## Installation

Build the plugin or obtain the compiled `hcbravo.xpl` from the Releases section.

Install the Windows plugin at:

`X-Plane 12/Resources/plugins/hcbravo/win_x64/hcbravo.xpl`

The `win_x64` directory is required for X-Plane to load the Windows plugin correctly.

## Technical notes

Bravo Lite support includes:

- USB VID/PID detection for Honeycomb Bravo Lite
- Selection of the Bravo Lite vendor-defined HID collection
- Bravo Lite HID report ID and report structure
- Feature-report communication for the landing gear LEDs
- Three-state landing gear indication: down, transit, and retracted

## Credits

This is a modification of the original `hcbravo` X-Plane plugin by Isaac Gelado.

Original project:
https://github.com/igelado/hcbravo

The original project and this fork are distributed under the GNU Lesser General Public License v2.1 (LGPL-2.1).
