
# Payslip Generation Script - README

This script generates individual payslips for employees in PDF format based on the data in an Excel file.

## Requirements

- Python 3.x
- Libraries:
  - FPDF: `pip install fpdf`
  - Pandas: `pip install pandas`

## Input File

The script reads employee data from an Excel file called `Employees.xlsx`. The file must contain the following columns:

- **Employee ID**: Unique identifier for each employee.
- **Name**: Employee's full name.
- **Basic Salary**: The basic salary of the employee.
- **Allowances**: Additional allowances added to the salary.
- **Deductions**: Deductions from the salary (e.g., taxes, insurance).

Ensure the file is located in the same directory as the script, or update the `file_path` variable with the correct file path.

## Script Workflow

1. The script reads the Excel file and processes each row (representing an employee).
2. For each employee, a PDF payslip is generated with the following sections:
    - **Employee Information**: Displays Employee ID, Name, and the current date.
    - **Salary Details**: Lists the Basic Salary, Allowances, Deductions, and Net Salary.
    - **Signature Section**: Includes a placeholder for the signature and company seal.
3. The generated payslips are saved in a folder named `payslips`. Each payslip is named in the format: `EmployeeID_EmployeeName.pdf`.

## How to Run the Script

1. Install the necessary dependencies:
    ```bash
    pip install fpdf pandas
    ```
2. Place the script and the `Employees.xlsx` file in the same directory.
3. Open a terminal/command prompt and navigate to the folder containing the script.
4. Run the script using the following command:
    ```bash
    python script_name.py
    ```

## Output

The script will create PDF payslips for each employee in the `payslips` folder, with filenames like:
```
payslips/12345_John_Doe.pdf
```

## Troubleshooting

If there's an error with the Excel file (e.g., wrong format, missing columns), the script will display an error message:
```
❌ Error: {e}
```

Make sure the Excel file is correctly formatted, and the columns match the required structure.

## Customization

You can modify the script as needed, including:
- Adjusting the layout of the PDF payslips.
- Changing the format of the file path or the folder name.

