# 🏆 Certificate Generator using Python & Google Sheets

This project automates the generation of personalized certificates using data from a Google Sheet. It fetches participant names, formats them, and generates high-quality certificate PDFs with names auto-positioned on a custom template.
It supports:
- Fetching names directly from Google Sheets  
- Custom certificate template support (PNG format)  
- Auto-center participant names using Pillow  
- Saving certificates as PDF files  
- Interactive coordinate selector for name placement using Tkinter  
- Name formatter for clean capitalization and spacing  

## Folder Structure
```
.
├── certificate_template.png      # Your certificate background
├── arial.ttf                     # Font file used
├── generate_certificates.py      # Main Python script
├── Generated_Certificates/       # Output folder with PDFs
└── README.md                     # This file
```

## Requirements
- Python 3.7+
- Packages:
  - pandas
  - gspread
  - pillow
  - requests
  - tkinter (usually included with Python)

Install requirements:-
```
pip install pandas gspread pillow requests
```

## Google Sheet Setup
1. Open your Google Sheet.
2. Share the sheet as “Anyone with the link can view”.
3. Get the CSV export link:
   ```
   https://docs.google.com/spreadsheets/d/<your-sheet-id>/export?format=csv
   ```
4. Replace the SHEET_URL in the script with your link.

## How to Set Name Position
1. Run the coordinate helper script (included in script):
```python
from PIL import Image, ImageTk
import tkinter as tk
...
```
2. Click anywhere on your certificate preview to get the X, Y coordinate.
3. Update NAME_POSITION in your main script with this coordinate.

## Running the Script
```
python generate_certificates.py
```

## Output
All certificate PDFs will be saved in the `Generated_Certificates` folder.

## Contribution
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---
