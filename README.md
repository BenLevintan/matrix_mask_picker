# Matrix Mask Picker

**Link to a website with a live demo:** https://benlevintan.github.io/site_Ben/mask_picker.html

**Matrix Mask Picker** is a Python desktop application designed to toggle matrix masks on and off.

It provides a graphical user interface (GUI) built using **PyQt5**, allowing users to:
- Open and view JSON and CSV files
- Load matrix data into tables
- Visually edit binary matrices (0s and 1s)
- Synchronize matrix data
- Save modified data back to CSV files

---

## 🔧 Features

- **Visual matrix display**: Easily view and interact with binary data (1s and 0s).
- **Cell toggling**: Click on a cell to toggle its state between 0 and 1.
- **Color-coded**: 
  - `1` is shown as **green**
  - `0` is shown as **blue**
- **Highlight changes**: Modified cells become more saturated to show they’ve been changed.
- **Support for JSON and CSV**: Load input from JSON files, compare or sync with external CSV files.
- **Matrix synchronization**: Keep two matrices in sync with one click.
- **Save functionality**: Save updated matrices as CSV files.

---

## 🧠 How It Works

1. **Load a JSON file** using the **"Open JSON File"** button.
2. Choose to load either:
   - `actuatorsMask`
   - `relevantLensletsVector`
3. The selected matrix will be displayed on the left side.
4. **Load a CSV file** using the **"Open CSV File"** button to compare with the JSON matrix.
5. Use buttons between the two tables to control the matrices.

---

## 🧩 Matrix Display

- The application supports matrices of two types:
  - `12x12` (for `actuatorsMask`)
  - `15x16` (for `relevantLensletsVector`)
- Left-side matrix is the **master**, right-side is the **slave**.
- Each cell contains a binary value:
  - `0 → Blue`
  - `1 → Green`
- Clicking a cell toggles its value:
  - `0 → 1`
  - `1 → 0`
- Toggled cells are highlighted for easy identification.

---

## 🕹️ Control Buttons

Located between the two matrix displays:

- **Sync** – Copies all values from the left (master) matrix to the right (slave).
- **All Off** – Sets all values in the visible matrix to `0`.
- **All On** – Sets all values in the visible matrix to `1`.
- **Save** – Exports the current matrix to a `.csv` file.

---

## 📂 File Formats

### JSON

Data is expected as a **flat list** and reshaped internally into a **2D matrix**.

### CSV

- Should contain a matrix of `0`s and `1`s.
- Dimensions must be either:
  - `12x12` (for actuator masks), or
  - `15x16` (for relevant lenslet vectors).

---

## 📦 Requirements

- Python 3.x  
- PyQt5  
- numpy  

## Install dependencies using pip:

pip install -r requirements.txt

---

## ▶️ Running the Program

Run the program from the terminal:

python matrix_mask_pecker.py

---

## 📌 Summary

Matrix Mask Picker simplifies binary matrix editing for structured JSON and CSV data. With its intuitive PyQt interface, you can:

- Load  
- Visualize  
- Modify  
- Sync  
- Save  

binary data matrices — all without writing a single line of code.

---

## 📃 License

This project is for educational and internal use. Modify and use freely.