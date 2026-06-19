---
dg-publish: true
---
## Overview

If you're experiencing lag, rubberbanding, or random disconnects, it may be caused by issues between your computer and the server, not the server itself.

To help us diagnose this, we recommend running a tool called `mtr` (My Traceroute). It shows the path your internet traffic takes and reveals where problems like packet loss or latency spikes are happening.

## Guide for Linux/macOS

1. **Install `mtr`** (if not already installed):

```bash
sudo apt install mtr  # Debian/Ubuntu
sudo pacman -S mtr    # Arch
brew install mtr      # macOS with Homebrew
```

2. **Run the test**
```bash
mtr -rwzbc100 play.landfall.world > mtr_report.txt
```
- `-r`: Report mode
- `-w`: Wide format
- `-z`: Show AS numbers (optional but useful)
- `-b`: Show both IP and hostname
- `-c100`: Send 100 pings

⚠️ **macOS Note**: If `mtr` fails to run, try running it with `sudo`, or grant Terminal full disk and network access via **System Settings > Privacy & Security**.

3. **Send the `mtr_report.txt`**
   - Once the command finishes execution, send us the output. You can upload the `mtr_report.txt` file directly to your Discord ticket.

## Guide for Windows (WinMTR)

A more extensive guide for using WinMTR can be found [here](https://xneelo.co.za/help-centre/website/how-to-run-an-mtr/).

1. **Download and Launch WinMTR**
- [Download WinMTR](https://sourceforge.net/projects/winmtr/) here or from a trusted source and launch it.

2. **Run the MTR**
- Input `play.landfall.world` in the Host field and click start. Let this run for about 60 seconds, then press stop.

3. **Send the Results**
   - Export the results and send them to us.

