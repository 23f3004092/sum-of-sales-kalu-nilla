# Sales Summary Demo

This is a simple single-page web application that fetches sales data from a CSV file, calculates the total sales, and displays it on the page.

## Features

- Fetches data from `data.csv`.
- Calculates the sum of the 'sales' column.
- Displays the total sales on the page.
- Uses Bootstrap 5 for styling.
- Displays a table of product sales.

## How to Run

1. Save the `index.html` file and `data.csv` file in the same directory.
2. Open `index.html` in your web browser.

## Checks

The following checks are implemented to ensure functionality:

- `document.title === 'Sales Summary demo123'`
- `!!document.querySelector('link[href*="bootstrap"]')`
- `Math.abs(parseFloat(document.querySelector('#total-sales').textContent) - 650) < 0.01`
- `document.querySelectorAll('#product-sales tbody tr').length >= 1`
- `(() => { const rows = [...document.querySelectorAll('#product-sales tbody tr td:last-child')]; const sum = rows.reduce((acc, cell) => acc + parseFloat(cell.textContent), 0); return Math.abs(sum - 650) < 0.01; })()`
