# Invoice Generator Project 📄→📊→📑

This Python project automates the generation of professional invoices from Excel files, saving them as PDFs. Perfect for streamlining billing workflows! 💼✨  

---

## Features 🚀

- **PDF Generation**: Convert Excel data into polished PDF invoices.  
- **Batch Processing**: Handle multiple files at once (`/invoices/` directory).  
- **Table Formatting**: Create clean, structured tables with headers.  
- **Auto-Totals**: Calculate sums dynamically. ➕  
- **Branding**: Add company name (`Patil & Company`) and logo (`mk-letter-logo.jpg`). 🏢  
- **Custom Styling**: Adjust fonts, colors, and layout. 🎨  

---

## How It Works ⚙️

1. **Input**:  
   - Excel files (e.g., `10002-2023.1.18.xlsx`) in `/invoices/`.  
   - Required columns: `product_id`, `product_name`, `amount_purchased`, `price_per_unit`, `total_price`.  

2. **Processing**:  
   - 📂 Extract invoice number/date from filenames.  
   - 📊 Build PDFs with headers, tables, and totals.  
   - 🏷️ Add branding (logo + company name) at the end.  

3. **Output**:  
   - 💾 Save PDFs to `/PDFs/` with matching names.  

---

## Code Highlights 💡

### Logo Integration  
```python
   pdf.set_font(family="Times", size=14, style="B")
   pdf.cell(w=20, h=8, txt="Patil & Company")
   pdf.image("mk-letter-logo.jpg", w=20, h=8)  # 🖼️ Logo placement
```
## Invoice Nr.10002  
Date: 2023.1.18  

| Product Id | Product Name | Amount | Unit Price | Total Price |  
|------------|--------------|--------|------------|-------------|  
| 8870011    | Paint Brush  | 2      | 34         | 68          |  

The total price is 68. 💰  

## Skills Learned 🛠️

| Skill Category         | Description                                                                 | Tools/Libraries Used  |
|------------------------|-----------------------------------------------------------------------------|-----------------------|
| **Python Automation**  | Automated repetitive invoice generation tasks with Python scripts.          | `Python 3.x`          |
| **PDF Generation**     | Created dynamic, formatted PDF documents programmatically.                  | `FPDF`                |
| **Data Handling**      | Processed and manipulated structured data from Excel files.                 | `pandas`              |
| **File Management**    | Organized file inputs/outputs and handled path operations.                  | `glob`, `pathlib`     |
| **Branding**           | Integrated company identity (logo + styling) into generated documents.      | `FPDF`, Image Handling|

## Setup & Usage 🏁

### Requirements
- Python 3.6+
- Dependencies:
  ```bash
  pip install pandas fpdf
  ```
## How to Run 🚀

### Step-by-Step Guide

1. **Prepare Your Files**  
   - Create an `invoices` folder in your project directory   
   - Place Excel files inside with this naming format:  
     `[INVOICE_NUMBER]-[DATE].xlsx` (e.g., `10002-2023.01.18.xlsx`)  
   - Ensure Excel files contain these columns:  
     `product_id`, `product_name`, `amount_purchased`, `price_per_unit`, `total_price`

2. **Run the Script**
   - *main.py*
