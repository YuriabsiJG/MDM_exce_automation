# Excel Filtering and Grouping Tool

## Overview
`excel_gen_filter_gen_1.py` is a Python script designed to load, filter, and group Excel data efficiently using a user-defined template. It provides an interactive interface for selecting input files, setting filter criteria, and tracking progress while processing.

## Features
- **Load Excel Data:** Dynamically identifies the header row.
- **Filter Data:** Apply filters based on user-defined criteria.
- **Group Data:** Saves filtered results into a predefined template.
- **Progress Tracking:** Displays a progress bar while processing.

---

## Installation
1. Ensure you have Python installed (>=3.7).
2. Install required dependencies using pip:
   ```sh
   pip install pandas openpyxl tqdm
   ```
3. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/excel-filtering-tool.git
   cd excel-filtering-tool
   ```

---

## Usage

### Step 1: Select Input, Output, and Template Files
1. **Input File:** Click Browse and select the Excel file (`.xlsx`) containing raw data.
2. **Output File:** Click Browse to specify where to save the filtered results.
3. **Template File:** Click Browse and select the Excel template for structured output.

### Step 2: Set Filter Criteria
- Enter column names and corresponding filter values.
- Click **Add Filter** to apply multiple conditions.
- Avoid duplicate column entries.

### Step 3: Process Data
Click **Filter and Group** to start filtering and grouping.
- A loading window with a progress bar appears during execution.
- A success message confirms completion.

### Step 4: Run Merge Script (Optional)
Click **Run Merge Script** to execute `merge.py` if needed.

---

## Notes
- Ensure the column names match the dataset headers.
- The filtered file is saved with a filename based on applied filters.
- The program prevents duplicate filter criteria.

# Excel File Merger - GitHub Documentation

## Overview
This tool allows users to merge multiple Excel files into a single sheet while preserving formatting. The program uses a template file to maintain consistency in structure.

## Features
- **Select a template file** to define the structure of the merged output.
- **Add multiple Excel files** to merge.
- **Remove selected files** from the list before merging.
- **Choose an output filename** for the merged file.
- **Merge the selected files** into the template while maintaining formatting.

---

## Installation
1. Ensure Python is installed (>=3.7).
2. Install required dependencies:
   ```sh
   pip install pandas openpyxl tqdm
   ```
3. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/excel-file-merger.git
   cd excel-file-merger
   ```

---

## Usage

### Step 1: Launch the Application
Run the Python script to open the graphical user interface (GUI).

### Step 2: Select a Template File
Click **Browse** to choose an Excel template. This template will define the structure of the merged file.

### Step 3: Add Excel Files
Click **Add Files** to select an Excel file or use `Ctrl + Click` to select multiple Excel files that need to be merged.

### Step 4: Remove Unwanted Files
Select files from the list and click **Remove Selected** to exclude them from the merging process.

### Step 5: Choose an Output File
Click **Browse** under **Output Filename** to specify where the merged Excel file will be saved and create a filename of your preference.

### Step 6: Merge Files
Click **Merge Selected Files** to start merging.
- The process runs in a separate thread to prevent UI freezing.
- A progress pop-up will appear until completion.

---

## Notes
- Ensure that column names and data formats match the template.
- The merged file will maintain the formatting of the template.
- Large datasets may take longer to process.

# Modular Guide: Setting Up and Executing a Standalone Program via PyInstaller

## Overview
PyInstaller is a Python package that allows you to convert Python scripts into standalone executable files for Windows, macOS, and Linux. This guide provides step-by-step instructions on setting up and executing a standalone program using PyInstaller.

## Prerequisites
- Python (>=3.7) installed
- Required Python dependencies installed
- PyInstaller installed

---

## Installation
### Step 1: Install PyInstaller
To install PyInstaller, run the following command:
```sh
pip install pyinstaller
```

### Step 2: Verify Installation
Check if PyInstaller is installed by running:
```sh
pyinstaller --version
```

---

## Creating a Standalone Executable

### Step 1: Navigate to Your Script's Directory
Ensure your terminal or command prompt is in the directory containing your Python script:
```sh
cd /path/to/your/script
```

### Step 2: Run PyInstaller
To create an executable from a Python script (`your_script.py`), use:
```sh
pyinstaller --onefile your_script.py
```

### Additional Options
- `--onefile`: Generates a single executable file.
- `--noconsole`: Hides the terminal window (useful for GUI applications).
- `--icon=icon.ico`: Sets a custom icon for the executable.
- `--name=CustomName`: Sets a custom name for the output file.

Example:
```sh
pyinstaller --onefile --noconsole --icon=myicon.ico --name=MyApp your_script.py
```

---

## Executing the Standalone Program

### Locate the Executable
After running PyInstaller, the executable will be found in the `dist/` folder:
```sh
dist/your_script.exe  # Windows
./dist/your_script  # macOS/Linux
```

### Running the Executable
To run the standalone program:
```sh
./dist/your_script  # macOS/Linux
```
For Windows, simply double-click `your_script.exe`.

---

## Troubleshooting

### 1. Missing Dependencies
If the executable fails to run, ensure all required dependencies are installed. Try reinstalling them:
```sh
pip install -r requirements.txt
```

### 2. Large File Size
If the output executable is too large, try using UPX compression:
```sh
pyinstaller --onefile --upx-dir=/path/to/upx your_script.py
```

### 3. Permission Issues
If you encounter permission errors on macOS/Linux, grant execution permissions:
```sh
chmod +x dist/your_script
```

---

## Conclusion
Using PyInstaller, you can easily convert Python scripts into standalone executables. By following this modular guide, you can customize your build, troubleshoot issues, and efficiently distribute your program.


