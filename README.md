# Daraz Website: Manual Testing Project

An independent practice project where I manually tested the public Daraz website (desktop web) to practise test design, execution and bug reporting.

> **Disclaimer:** This is a self-initiated learning project. I am not affiliated with Daraz, and Daraz did not request or approve it. I tested as a normal user. I did not place real orders, enter payment details, attempt to break security or generate load.

## What I tested

| Feature | Test cases |
|---|---|
| Search and price filter | 27 |
| Product page | 15 |
| Login and Forgot Password | 11 |
| Cart and wishlist | 16 |
| Checkout (up to payment selection) | 12 |
| **Total** | **81** |

**Not tested:** registration and OTP, orders and returns, filters other than price, mobile screens and the app, slow-network behaviour, real payments, security and load testing.

## Results

| Pass | Fail | Observation | Not concluded |
|---|---|---|---|
| 52 | 4 | 24 | 1 |

**3 defects found** (full details with steps and screenshots are in the report):

| ID | Defect | Severity |
|---|---|---|
| BUG_001 | Login and Forgot Password show technical wording ("The Phone may be null or illegal", "illegal param") instead of a plain message | Minor |
| BUG_002 | Handling Fee tooltip at checkout uses Indonesian "Rp" currency and a 6% rule that does not match the fee charged | Minor |
| BUG_003 | "Add a new card" panel at checkout opens with a very small content area (seen in Chrome, Chrome Incognito and Edge) | Minor to Moderate |

Other findings include a hard-to-find wishlist, fees that first appear at checkout, and delivery and handling fee rules that are not explained to the shopper. I also checked six order totals, and all of them matched their lines.

## How I tested

- **Test types:** functional, negative, boundary, field validation, state and navigation, data integrity, usability, localization
- **Techniques:** equivalence partitioning, boundary value analysis, decision table, error guessing, exploratory testing
- **Environment:** Chrome, Chrome Incognito and Edge on Windows, English language, guest and logged-in (own account)
- **Tools:** Chrome DevTools, Microsoft Word, [Excel / Google Sheets], [Jira / Trello if used]

Each test case records the test type, technique, test data, actual result and status. Failures and key observations have screenshots.

## Files

- [Test report (PDF)](Daraz_Manual_Testing_Report)
- [Screenshots](screenshots/): evidence for the three defects is named `BUG_001_...`, `BUG_002_...` and `BUG_003_...`; other files are named after the test case they support (for example `TC_CHK_008_cerave_qty5.png`)

## What I would do next

- Resolve the review-sorting question on the product page
- Work out the delivery fee and handling fee rules by testing more products and quantities
- Add phone-size screens and slow-network tests with Chrome DevTools
- Test registration, orders and returns

## Note on AI assistance

All testing and result verification were done manually by me. I used an AI assistant (Claude) to help structure and format the report from my notes, and I reviewed the content for accuracy.
