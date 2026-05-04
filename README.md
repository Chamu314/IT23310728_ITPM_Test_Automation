# IT23310728 — Assignment 1: Singlish-to-Sinhala Transliteration Accuracy Testing

**Student IT Number:** IT23310728  
**Module:** IT3040 — ITPM (Assignment 1)

---

## Project Overview

This project evaluates the transliteration accuracy of the Singlish-to-Sinhala conversion tool available at [Pixelssuite Chat Translator](https://www.pixelssuite.com/chat-translator). The testing focuses on identifying failure points (negative scenarios) where the tool fails to correctly convert informal chat-style Singlish input into Sinhala script.

The automation is built using Python and Playwright, covering **50 negative test cases** across **24 different Singlish input types**.

---

## Prerequisites

Before running the tests, ensure you have the following installed:

- **Python 3.11 / 3.12** — Download from [python.org](https://www.python.org/downloads/)
- **Google Chrome** browser (Recommended)

---

## Installation

Follow these steps to set up the environment and install the necessary dependencies:

**1. Navigate to the project directory:**

```bash
cd /d D:\IT23310728\Playwright_Project_Files
```

**2. Upgrade pip:**

```bash
python.exe -m pip install -U pip
```

**3. Install required libraries:**

```bash
pip install playwright openpyxl
```

**4. Install Playwright browsers:**

```bash
playwright install
```

---

## Running the Tests

To execute the automation script and record results into the Excel file, run the following command in your terminal:

```bash
python test_automation.py --excel "IT23310728_Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 10000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

> **Note:** The `--wait-ms 10000` flag is used to handle potential "Failed to fetch" errors or slow API responses from the target website. If the website is particularly slow, this value can be increased to `--wait-ms 20000`.

---

## Checking Results

Once the script has finished running:

1. Go to the `Playwright_Project_Files` folder
2. Reopen `IT23310728_Assignment 1 - Test cases.xlsx`
3. Verify that the **Actual output** and **Status** columns have been automatically filled in
4. Since all 50 test cases are negative scenarios (failure cases), most rows in the Status column should show **Fail**

---

## Project Structure

```
Playwright_Project_Files/
├── test_automation.py                          # Main Playwright automation script
├── IT23310728_Assignment 1 - Test cases.xlsx  # 50 negative test cases data file
└── README.md                                   # Project documentation (this file)
```

---

## Test Case Summary

| Description | Count |
|---|---|
| Total Test Cases | 50 |
| Test Case Type | Negative (Fail scenarios) |
| Singlish Input Types Covered | 24 |
| TC ID Format | Neg_0001 — Neg_0050 |

---

## Singlish Input Types Covered

1. Question Forms
2. Command Forms
3. Greetings
4. Requests
5. Responses
6. Repeated Words
7. Inputs with Punctuation Marks
8. Romanization / Spelling Variants
9. Isolated English Word Insertions in Singlish
10. Multi-Word English Phrases in Singlish
11. English Digital Terms in Singlish
12. Platform/App Names in Singlish
13. English Abbreviations/Acronyms in Singlish
14. English Clipped Forms in Singlish
15. Place Names Embedded in Singlish
16. Person Names Embedded in Singlish
17. Inputs with Numbers and Numeric Suffixes
18. Inputs with Currency
19. Inputs with Time Formats
20. Inputs with Dates
21. Inputs with Unit of Measurements
22. Inputs with Slang and Casual Phrasing
23. Online Identifiers in Singlish
24. Inputs Containing Emojis

---

## Author

| | |
|---|---|
| **Name** | M.H.C.T. Samarasinghe |
| **IT Number** | IT23310728 |
| **University** | Sri Lanka Institute of Information Technology (SLIIT) |
| **Module** | IT3040 — IT Project Management (ITPM) |
| **Assignment** | Assignment 1 — Option 1 |
