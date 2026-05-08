# 64-cards-validation-tool
# ICCID & Barcode Validation Tool

This project is a desktop application built for telecom smart card validation and production environments. It reads ICCID data directly from smart cards using PC/SC readers, validates scanned barcodes, and automatically stores records in Excel sheets and a SQLite database.

The tool is designed to reduce manual work during validation processes and provide fast, reliable tracking for operators and production teams.

---

## Features

- Automatic ICCID reading from smart cards
- Barcode scanning and validation
- Half Card, Quarter Card, and USB Scanner modes
- Real-time MATCH / MISMATCH detection
- Excel report generation using a master template
- SQLite database logging
- Operator and machine tracking
- Shift-based record management
- Auto card detection with fast polling
- Smart APDU fallback handling for different card types
- Live validation table with color highlighting

---

## Technologies Used

- Python
- Tkinter
- pyscard
- Pillow
- OpenPyXL
- SQLite3

---

## Requirements

Install the required Python packages:

```bash
pip install pyscard pillow openpyxl
```

---

## How It Works

### Half Card Mode
1. Insert smart card
2. ICCID is read automatically
3. Scan barcode
4. Tool compares ICCID and barcode
5. Result is saved with MATCH or MISMATCH status

### Quarter Card Mode
- Reads and stores ICCID only

### USB Scanner Mode
- Allows barcode scanning independently

---

## Excel & Database Logging

The application automatically:
- Creates Excel logs from a master sheet
- Stores timestamps and operator details
- Highlights matched and mismatched values
- Saves all validation records into SQLite database

---

## Project Structure

```bash
ICCID_Logs/         # Generated Excel reports
ICCID_Database/     # SQLite database
logo.png            # Application logo
main.py             # Main application
```

---

## Running the Application

```bash
python main.py
```

---

## Notes

- Make sure a PC/SC smart card reader is connected
- Update Excel template paths if required
- Barcode scanner should work in keyboard input mode

---

## Author

Ajitkumar
