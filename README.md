# Gantt Chart Extractor

This tool extracts task information from Gantt charts in PDF, MPP (Microsoft Project), and XLSX (Excel) files.  It provides a user-friendly interface for loading files, filtering tasks, and viewing extracted data.

## Features

- **Supports multiple file formats:**  PDF, MPP, and XLSX.
- **Automatic task extraction:** Extracts task names, start and end dates, and hierarchical level (for MPP and XLSX).
- **Advanced filtering:**  Search by keywords, include specific terms, and exclude unwanted terms.
- **Savable filters:** Save and load custom filter configurations for reuse.
- **Hierarchical task view:** Displays hierarchical relationships between tasks for MPP and XLSX files.
- **Intuitive GUI:** Easy-to-use graphical interface built with PySide6.


## Requirements

- Python 3.7+
- Java JDK 8+ (required for processing MPP files - ensure JAVA_HOME is set)
- Python libraries (install via `pip install -r requirements.txt`):
    - PySide6
    - pdfplumber
    - jpype1
    - mpxj
    - openpyxl
    - pandas

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/gantt-chart-extractor.git
   ```
2. **Install dependencies:**

  **Option 1 - Direct Installation:**
  ```bash
  pip install PySide6 pdfplumber jpype1 mpxj pandas openpyxl
  ```
  **Option 2 - Using requirements.txt:**
  ```bash
  pip install -r requirements.txt
  ```
3. **Set JAVA_HOME (for MPP files):** Configure the JAVA_HOME environment variable to point to your JDK installation directory.

## Usage

1. **Run the application:**
   ```bash
   python src/file_gui.py
   ```
2. **Load a file:** Use the "Load PDF", "Load MPP", or "Load XLSX" buttons to select your Gantt chart file.
3. **Filter tasks (Optional):**
    - **Search:** Enter comma-separated keywords. All keywords must be present in the task name.
    - **Include words:** Enter comma-separated terms. At least one term must be present in the task name.
    - **Exclude words:** Enter comma-separated terms.  Tasks containing these terms will be hidden.
4. **Save/Load Filters:** Use the "Save Filter" and "Load Filter" buttons to save and reuse filter configurations.  Filters are saved as `.ft` files.

## Project Structure

- `src/file_gui.py`: Main GUI application.
- `src/pdf_extractor.py`: PDF parsing and extraction.
- `src/mpp_extractor.py`: MPP parsing and extraction.
- `src/xlsx_extractor.py`: XLSX parsing and extraction.
- `src/filter_util.py`: Filtering utility functions.
- `src/loading_animation_widget.py`: Loading animation widget.
- `requirements.txt`: Project dependencies.


## License

MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue to discuss proposed changes before submitting a pull request.


## Example Filter File (.ft)

```
Incluir:construcción, diseño
Excluir:prueba, revisión
```


## Example Schedule (Conceptual - How data might appear in the application)

| Task ID | Level | Task Name         | Start Date | End Date   | File Source |
|---------|-------|-------------------|------------|------------|-------------|
| 1       | 0     | Project Start     | 01/01/2024 | 01/01/2024 | example.mpp |
| 2       | 1     | Phase 1          | 02/01/2024 | 15/01/2024 | example.mpp |
| 3       | 2     | Design Phase     | 02/01/2024 | 09/01/2024 | example.mpp |
| 4       | 2     | Build Phase      | 10/01/2024 | 15/01/2024 | example.mpp |
| 5       | 1     | Phase 2          | 16/01/2024 | 31/01/2024 | example.mpp |
| ...     | ...   | ...              | ...        | ...        | ...         |

```
