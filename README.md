# Invoice Generator Project

This Python project automates the generation of professional invoices from Excel files, saving them as PDFs. It includes dynamic data processing, branding, and styling to create polished invoices efficiently.

---

## Features

- **PDF Generation**: Converts Excel data into formatted PDF invoices.
- **Batch Processing**: Handles multiple Excel files in the `invoices/` directory.
- **Table Formatting**: Creates structured tables with headers and rows.
- **Automatic Totals**: Calculates and displays the total price.
- **Branding**: Adds a company name (`Patil & Company`) and **logo** (`mk-letter-logo.jpg`) at the end of the invoice.
- **Flexible Styling**: Customizable fonts, colors, and layout.

---

## How It Works

1. **Input**: Excel files (e.g., `10002-2023.1.18.xlsx`) stored in `/invoices/` with columns:
   - `product_id`, `product_name`, `amount_purchased`, `price_per_unit`, `total_price`
2. **Processing**:
   - Extracts invoice number and date from the filename.
   - Generates a PDF with headers, product tables, and totals.
   - Adds the company name and logo (`mk-letter-logo.jpg`) **at the end** for branding.
3. **Output**: Saves PDFs in `/PDFs/` with the same name as the input file.

---

## Code Highlights

### Logo Integration
The company logo (`mk-letter-logo.jpg`) is placed **at the end of the PDF** alongside the company name using:
```python
pdf.set_font(family="Times", size=14, style="B")
pdf.cell(w=20, h=8, txt="Patil & Company")
pdf.image("mk-letter-logo.jpg", w=20, h=8)  # Logo added here
```
Invoice Nr.10002
Date: 2023.1.18

| Product Id | Product Name | Amount | Unit Price | Total Price |
|------------|--------------|--------|------------|-------------|
| 8870011    | Paint Brush  | 2      | 34         | 68          |

The total price is 68.
