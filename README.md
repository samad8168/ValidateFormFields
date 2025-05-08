RPA Challenge Automation with UiPath

## Overview
This project automates the RPA Challenge (https://rpachallenge.com/) using UiPath. It reads 10 test cases from an Excel file, fills the challenge form, submits it, validates the results, and logs the pass/fail status with reasons back to the Excel file.

## Prerequisites
- UiPath Studio (version 2023.10 or later)
- Microsoft Excel
- Input Excel file ( C:\Users\computer\Downloads\challenge.xlsx) with 10 test cases
- Stable internet connection for accessing the RPA Challenge website

## Setup
1. Clone this repository: git clone <repo-url>
2. Open the project in UiPath Studio.
3. Ensure C:\Users\computer\Downloads\challenge.xlsx is in the project directory with the following columns:
   - TestCases,	First Name,	Last Name ,	Company Name,	Role in Company,	Address,	Email	,Phone Number,	Pass_Fail,	Reason
!

4. Install required UiPath activities:
   - UiPath.Excel.Activities
   - UiPath.UIAutomation.Activities
   - UiPath.WebAPI.Activities

## How It Works
1. Reads test cases from Challange.xlsx.
2. Opens the RPA Challenge website and starts the challenge.
3. For each test case:
   - Fills the form fields (First Name, Last Name, etc.).
   - Submits the form.
   - Validates the submission (checks for success or errors).
   - Logs the result (Pass/Fail) and reason (e.g., "Invalid Email Format") in the Excel file.
4. Saves the updated Excel file with results.

## Running the Project
1. Open Main.xaml in UiPath Studio.
2. Ensure Challange.xlsx in downlods folder is in the project folder.
3. Run the workflow (F5 or click "Run").
4. Check the updated Challange.xlsx for results.

## Output
- Challange.xlsx is updated with two new columns:
  - *Result*: Pass/Fail
  - *Reason*: Explanation for failure (if applicable)

## Notes
- Ensure the RPA Challenge website is accessible.
- Handle exceptions for network issues or incorrect data formats.
- Test the workflow with sample data before running all test cases.

