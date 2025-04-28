# OSA-and-Osteoporosis_TTMHH-R1130049
## Population selection.ipynb

This project filters and compares data from a master dataset based on multiple reference files. The overall process is as follows:

---

### 1. Data Loading

- Use `Pathlib` to specify the folder path `Data Set/csv`.
- Automatically load all `.csv` files from the folder into a dictionary named `dataframes` for easy access.

---

### 2. Parameter Setup

- Specify the **base file** (master dataset): `2017-2022-Meger.csv`.
- Specify the **key feature** column in the base file: `id_number`.
- Define the feature mappings for other reference files (all using `去個資編號` as the feature column).

---

### 3. Data Filtering Process

- Filter rows from the base file where `id_number` matches values found in the reference files.
- Avoid selecting the same ID multiple times during filtering.
- Record and display:
  - The number of samples selected from OSA (Obstructive Sleep Apnea) reports
  - The number of samples selected from BMD (Bone Mineral Density) reports

- Save the filtered data to: `Data Set/filter/2017-2022-filter.csv`.

---

### 4. Advanced Comparison

- Further categorize the selected data:
  - Samples found **only** in OSA reports
  - Samples found **only** in BMD reports
  - Samples found **in both** OSA and BMD reports
- Display the sample counts for each category.

---

### 5. Duplicate Check

- Read the newly created file `2017-2022-filter.csv`.
- Check if any `id_number` appears more than once.
- If duplicates are found, display the duplicated `id_number` values and their counts; if no duplicates, display a message confirming no duplicates.

---

### 📂 Output Results

- Filtered dataset saved as: `Data Set/filter/2017-2022-filter.csv`
- Summary statistics and duplicate checks printed to the console during execution.
