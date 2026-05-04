# IT3040 Assignment 1 (Option 1)

**BSc (Hons) in Information Technology, Year 3**  
**IT3040 - ITPM Semester 1**

## Assignment Overview

This project automates transliteration checks for the Chat Sinhala feature at:

🔗 https://www.pixelssuite.com/chat-translator

### Assignment Objective

Evaluate how accurately chat-style Singlish input is converted to Sinhala output in the live web application.

### Scope

**In scope:**

- Chat Sinhala transliteration accuracy testing only

**Out of scope:**

- Standard Sinhala transliteration mode
- Backend API testing
- Performance, scalability, and security testing

---

## Prerequisites & Installation

### 1. Install Python

Install **Python 3.11 or 3.12** and verify installation:

```bash
python --version
pip --version
```

### 2. Install Browsers

**Option A (recommended):** Install Google Chrome manually.

**Option B:** Let Playwright install Chromium automatically.

### 3. Install Python Dependencies

From this project folder, run:

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## Running the Automation


### Option 1: From the clone repository (Recommended)
```bash
git clone https://github.com/isuru-bimsara/-IT23674912---IT3040---ITPM.git
```
```bash
cd -IT23674912---IT3040---ITPM
```
```bash
python test_automation.py --excel "-IT23674912---IT3040---ITPM\IT23674912 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 12000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Option 2: If you download zip file (`IT23674912`)

Unzip file and go IT23674912-ITPM-Assignment1 folder (IT23674912\IT23674912\IT23674912-ITPM-Assignment1).

```bash
python test_automation.py --excel "IT23674912-ITPM-Assignment1\IT23674912 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 12000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Command-line Options

| Option            | Description                                   |
| ----------------- | --------------------------------------------- |
| `--excel`         | Path to the Excel test case file              |
| `--url`           | Target web application URL                    |
| `--wait-ms`       | Wait time in milliseconds before interactions |
| `--type-delay-ms` | Delay between typing characters (ms)          |
| `--slow-mo-ms`    | Slow motion delay (ms)                        |
| `--save-every`    | Save results after every N test cases         |
| `--keep-open`     | Keep browser window open after execution      |
| `--headless`      | Run browser in headless mode (no UI)          |

### Notes

- Remove `--keep-open` if you don't want the browser to stay open
- Use **Ctrl+C** to stop when running with `--keep-open`
- Add `--headless` to run without visible browser UI

---

## Excel Workflow

### Before Running the Script

Open **Assignment 1 - Test cases.xlsx** and fill only these columns:

| Column            | Description                       |
| ----------------- | --------------------------------- |
| TC ID             | Test case identifier              |
| Input length type | Category of input length          |
| Input             | Chat-style Singlish input to test |
| Expected output   | Expected Sinhala translation      |

**Do NOT manually fill:**

- Actual output
- Status

### After Running the Script

1. **Reopen the Excel file** and verify values written to:
   - Actual output
   - Status

2. **Add two new columns** next to Status:
   - Singlish input types covered
   - Evidence or rationale for the input type covered

3. **Fill these columns manually** using Appendix 2 style reference

---

## Project Structure

```
IT23674912-ITPM-Assignment1/
├── README.md                          # This file
├── test_automation.py                 # Main automation script
└── IT23674912 - Test cases.xlsx     # Test case spreadsheet
```

---

## Support & Issues

For issues or questions, refer to the assignment requirements and verify:

- Python and Playwright are correctly installed
- Excel file is in the correct format
- Target URL is accessible
- Browser (Chrome/Chromium) is installed and functional
