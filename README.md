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

---

## Contributing
1. Fork the repository.
2. Create a new branch for your feature:
   ```sh
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```sh
   git commit -m "Add new feature"
   ```
4. Push the branch:
   ```sh
   git push origin feature-name
   ```
5. Open a Pull Request.

---

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Contact
For any issues or feature requests, please open an issue on GitHub or contact `your-email@example.com`.

