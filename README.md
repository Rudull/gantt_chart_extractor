# Gantt Chart Extractor

This is a Gantt chart extractor that allows you to load and analyze PDF, MPP (Microsoft Project), and XLSX (Excel) files to extract information about tasks and their schedules.

## Features

- Loads PDF, MPP, and XLSX files.
- Automatically extracts tasks with their dates.
- Advanced filtering system.
- Keyword search.
- Saving and loading custom filters.
- Hierarchical view of tasks (for MPP and XLSX).
- Intuitive graphical interface.

## Requirements

- Python 3.7+
- Java JDK 8+ (for processing MPP files)
- The following Python libraries:
  - PySide6
  - pdfplumber
  - jpype1
  - mpxj
  - openpyxl
  - pandas

## Installation

1. Clone this repository:
```bash
git clone https://github.com/your-username/gantt-chart-extractor.git
```

2. Install the dependencies:

**Option 1 - Direct Installation:**
```bash
pip install PySide6 pdfplumber jpype1 mpxj pandas openpyxl
```
**Option 2 - Using requirements.txt:**
```bash
pip install -r requirements.txt
```

3. Make sure you have JAVA_HOME configured in your system's environment variables if you are going to use MPP files.

## Usage

1. Run the program:
```bash
python file_gui.py
```

2. Use the "Load PDF", "Load MPP", or "Load XLSX" buttons to open files.

3. Use the search and filter bars to find specific tasks:
   - Search: General search for terms (all words must be present).
   - Include words: Terms that must be present (at least one word must be present).
   - Exclude words: Terms that should not appear.

4. You can save and load custom filters using the corresponding buttons. Filters are saved in `.ft` files.

## Project Structure

- `file_gui.py`: Main graphical interface.
- `pdf_extractor.py`: PDF file handling.
- `mpp_extractor.py`: MPP file handling.
- `xlsx_extractor.py`: XLSX file handling.
- `filter_util.py`: Filtering utilities.
- `loading_animation_widget.py`: Loading animation widget.


## License

[MIT License](LICENSE)

## Contributions

Contributions are welcome. Please open an issue first to discuss the changes you would like to make.

---
For more information or to report issues, please create an issue in the repository.
