# US Stock Notifier

A  desktop assistant for monitoring US stock prices, supporting real-time price display, desktop notifications, and system tray operation. Supports both Chinese and English interfaces.

## Features
- Real-time monitoring of US stock prices (using Yahoo Finance)
- Customizable stock list and notification interval
- Apple-style modern UI (light gray/blue, rounded corners, modern fonts)
- Desktop notifications (native Windows 10/11 notification)
- System tray icon, can minimize to tray
- Operation log and status bar
- One-click language switch (Chinese/English)

## Dependencies
- Python 3.8+
- yfinance
- pystray
- pillow
- winotify
- tkinter (comes with Python)

## Installation
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. (Optional) For packaging as an exe:
   ```bash
   pip install pyinstaller
   ```

## Packaging to EXE
```bash
pyinstaller --onefile --windowed --name "US Stock Notifier" --add-data "README.md;." stock_notifier_gui.py
```
The exe will be generated in the `dist/` folder.

## Usage
1. Run the program:
   - Double-click the exe, or
   - Run `python stock_notifier_gui.py`
2. Enter stock symbols (comma separated, e.g. `AAPL, TSLA, MSFT`)
3. Set notification interval (minutes)
4. Click "Start" to begin monitoring
5. Minimize to tray for background operation
6. Click the "English/中文" button to switch language

## Language Switch
- The top-right button toggles between English and Chinese.
- All UI, table headers, buttons, messages, and logs will switch instantly.

## System Tray
- When minimized, the app will hide to the system tray.
- Right-click the tray icon for menu (Show Main Window, Exit).

## FAQ
- **No notification?**
  - Make sure Windows notifications are enabled.
  - Try running as administrator if needed.
- **Data not updating?**
  - Check your network connection.
  - Yahoo Finance API may have rate limits.
- **Font not displaying correctly?**
  - The app uses system fallback fonts if PingFang/Menlo are not available.

## License
MIT 
