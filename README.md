# Income Taxes — One Master Example

An interactive, browser-based learning tool that explains **current tax, deferred tax, temporary differences, permanent differences, and the effective tax rate** through one fictional company: **Bright Co.**

The user can change:

- Year 1–5
- Revenue
- Cash operating costs
- Tax rate
- Machine cost
- Salvage value
- Warranty provision

The page recalculates the example instantly and walks through:

1. Book income vs. taxable income
2. Taxes payable
3. Deferred tax liabilities (DTL) from depreciation timing differences
4. Deferred tax assets (DTA) from the warranty provision
5. Current tax payable vs. total income tax expense
6. Temporary vs. permanent differences
7. Effective tax rate

## Live Demo

After enabling GitHub Pages, the project can be viewed directly in the browser at:

`https://<your-github-username>.github.io/<repository-name>/`

No server, build step, framework, API, or database is required.

## Why this is a useful portfolio project

This is deliberately a **small, self-contained front-end project**. It demonstrates:

- HTML/CSS layout
- JavaScript DOM manipulation
- Interactive range inputs
- Client-side financial calculations
- Dynamic explanatory text
- Responsive design
- Formula tracing and visual feedback
- GitHub Pages deployment

The emphasis is not on building a large application; it is on turning an accounting concept into an interactive learning experience.

## Accounting logic

### Book depreciation

The machine uses straight-line depreciation over five years:

`(Machine cost − Salvage value) / 5`

### Tax depreciation

Tax depreciation uses a simplified double-declining-balance approach:

`Opening tax basis × 2/5`

The deduction is capped so the tax basis does not fall below the salvage value.

### Warranty

Bright Co. recognizes the warranty provision in **Year 1** for book purposes but receives the tax deduction when the warranty is paid in **Year 3**.

That timing difference creates a **deferred tax asset (DTA)** before reversal.

### Machine timing difference

Because tax depreciation is accelerated relative to book depreciation, taxable income can be lower than book income in earlier years. The resulting taxable temporary difference creates a **deferred tax liability (DTL)**.

### Income tax expense

The simplified reconciliation used by the page is:

`Income tax expense = taxes payable + change in DTL − change in DTA`

### Permanent difference

Bright Co. also has `$5,000` of tax-exempt interest. It increases book income but is never taxable, so it does **not** create deferred tax. Instead, it affects the effective tax rate.

## Project structure

```text
income-taxes-master-example/
├── index.html
├── README.md
└── LICENSE
```

## Run locally

No installation is necessary.

Just open `index.html` in a browser.

For a local server, you can also use any static server, for example:

```bash
python3 -m http.server
```

Then open the local address shown by Python.

## Deploy with GitHub Pages

1. Create a new GitHub repository.
2. Add `index.html`, `README.md`, and `LICENSE`.
3. Push the files to the `main` branch.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select the `main` branch and `/ (root)`.
7. Save.
8. GitHub will publish the site.

Because this is a static HTML/CSS/JavaScript project, **GitHub Pages is sufficient**.

## Suggested portfolio description

> **Income Taxes — Interactive Master Example:** Built a browser-based accounting education tool using HTML, CSS and vanilla JavaScript. Users can change operating and tax assumptions and see real-time calculations for taxable income, taxes payable, deferred tax assets/liabilities, income tax expense, temporary/permanent differences, and effective tax rate.

## Tech stack

- HTML5
- CSS3
- Vanilla JavaScript
- GitHub Pages

## Note

This is an **illustrative educational model**, not tax advice or a production tax calculator. The depreciation and tax rules are intentionally simplified so the accounting concepts remain visible.
