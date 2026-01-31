# IT23856936 - Singlish to Sinhala Translator Automation Testing

Automated UI testing suite for the Swift Translator website using Playwright. This project validates Singlish to Sinhala translation functionality through comprehensive test cases mapped from Excel test documentation (Appendix 2 guidelines).

## 🌐 System Under Test

**Website:** [https://www.swifttranslator.com/](https://www.swifttranslator.com/)

## 📋 Overview

This repository contains Playwright-based end-to-end automation tests that validate:

- ✅ **Translation Accuracy** - Singlish to Sinhala conversion correctness
- ✅ **Mixed Language Support** - Handling of English + Singlish combinations
- ✅ **UI Responsiveness** - Real-time output updates
- ✅ **Input Handling** - Clear functionality and edge cases
- ✅ **Negative Testing** - Invalid input scenarios

All test cases are directly mapped from the Excel test case file (`Book1(AutoRecovered).xlsx`) created as per campus Appendix 2 guidelines.

## 🧪 Test Coverage

### Positive Functional Tests
- `Pos_Fun_0001` - Simple daily sentence translation
- `Pos_Fun_0002` - Greeting question translation
- `Pos_Fun_0008` - Mixed English + Singlish translation

### Negative Functional Tests
- `Neg_Fun_0001` - Joined words handling

### UI Tests
- `Pos_UI_0001` - Real-time output updates
- `Neg_UI_0002` - Clear input clears output

**Total Test Cases:** 6

## 📦 Prerequisites

Before running the tests, ensure you have:

- **Node.js** 18 or higher ([Download](https://nodejs.org/))
- **npm** (comes with Node.js)
- **Internet connection** (for accessing the test website)

Verify installation:
```bash
node -v
npm -v
```

## 🚀 Installation

1. **Clone or download this repository**
   ```bash
   cd IT23856936-playwright
   ```

2. **Install project dependencies**
   ```bash
   npm install
   ```

3. **Install Playwright browsers**
   ```bash
   npx playwright install
   ```

   This will download Chromium, Firefox, and WebKit browsers required for testing.

## ▶️ Usage

### Run All Tests

Execute the complete test suite:
```bash
npm test
```

### Run Tests in UI Mode

Interactive test runner with step-by-step execution:
```bash
npm run test:ui
```

### View Test Report

After running tests, view the HTML report:
```bash
npm run report
```

The report will open in your default browser showing:
- Test execution summary
- Pass/fail status
- Execution time
- Screenshots (on failure)
- Videos (on failure)
- Detailed error logs

## 📁 Project Structure

```
IT23856936-playwright/
│
├── tests/
│   └── singlishTranslator.spec.js    # Test automation scripts
│
├── playwright.config.js               # Playwright configuration
├── package.json                       # Project dependencies & scripts
├── README.md                          # Project documentation
│
├── playwright-report/                 # Generated HTML reports (after test run)
│   └── index.html                    # Main report file
│
└── test-results/                      # Test artifacts (screenshots, videos)
    └── [test-name]/
        ├── test-failed-1.png
        ├── video.webm
        └── error-context.md
```

## ⚙️ Configuration

### Playwright Configuration (`playwright.config.js`)

- **Test Directory:** `./tests`
- **Timeout:** 30 seconds per test
- **Base URL:** `https://www.swifttranslator.com/`
- **Headless Mode:** Enabled
- **Screenshots:** Captured on failure only
- **Videos:** Retained on failure only
- **Reporter:** HTML report (auto-generated)

### Test Selectors

Current selectors used in tests (may need adjustment based on website updates):
- **Input Field:** `textarea`
- **Output Field:** `#output, .output, textarea[readonly]`

## 📊 Test Reports

### HTML Report

After running tests, an interactive HTML report is generated in the `playwright-report/` directory. This report includes:

- ✅ Test execution summary
- 📸 Screenshots for failed tests
- 🎥 Video recordings for failed tests
- 📝 Detailed error messages and stack traces
- ⏱️ Execution time metrics
- 🔍 Step-by-step test execution details

**Access the report:**
```bash
npm run report
```

Or manually open: `playwright-report/index.html`

### Test Artifacts

- **Screenshots:** Saved in `test-results/[test-name]/test-failed-1.png`
- **Videos:** Saved in `test-results/[test-name]/video.webm`
- **Error Context:** Saved in `test-results/[test-name]/error-context.md`

## 🔧 Troubleshooting

### Tests Failing Due to Selector Issues

If tests fail with "element(s) not found" errors:

1. Inspect the website using browser DevTools
2. Update selectors in `tests/singlishTranslator.spec.js`
3. Adjust the `INPUT` and `OUTPUT` constants as needed

### Browser Installation Issues

If `npx playwright install` fails:

```bash
npx playwright install --with-deps
```

### Network/Timeout Issues

If tests timeout:

1. Check internet connection
2. Verify website is accessible: https://www.swifttranslator.com/
3. Increase timeout in `playwright.config.js` if needed

## 📝 Test Execution Workflow

1. **Setup** → Install dependencies and browsers
2. **Execute** → Run test suite (`npm test`)
3. **Analyze** → Review HTML report (`npm run report`)
4. **Debug** → Check screenshots/videos for failures
5. **Fix** → Update selectors or test logic if needed
6. **Re-run** → Execute tests again to verify fixes

## 📤 Submission Package

For campus submission, include:

1. ✅ **IT23856936-playwright/** folder (entire project)
2. ✅ **IT23856939-TestCase.xlsx** (Excel test case documentation)
3. ✅ **playwright-report/** folder (HTML test execution report)

## 🛠️ Technologies Used

- **Playwright** - End-to-end testing framework
- **Node.js** - JavaScript runtime
- **npm** - Package manager

## 👤 Author

**Registration Number:** IT23856936

## 📄 License

This project is created for academic purposes as part of the testing automation coursework.

## 🔗 Useful Links

- [Playwright Documentation](https://playwright.dev/docs/intro)
- [Playwright API Reference](https://playwright.dev/docs/api/class-test)
- [Node.js Documentation](https://nodejs.org/docs/)

---

**Note:** This automation suite is designed to work with the Swift Translator website. Selectors may need periodic updates if the website UI changes.
