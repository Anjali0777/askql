# AskQL

Ask your database a question in plain English and get a ready-to-run SQL query back, with a short explanation of what it does.

Built for people who don't write SQL: paste your table definitions, pick a dialect, type a question like *"Top 5 customers by total spending this year"*, and copy the query into your database tool.

## Features

- Accepts `CREATE TABLE` statements or a loose list like `orders(id, customer_id, total, created_at)`
- Dialects: PostgreSQL, MySQL, SQLite, SQL Server, BigQuery, Snowflake
- Uses only the columns in your schema, with no invented ones
- Plain-language explanation, list of tables used, and any assumptions made
- Warns when a query would modify data
- Syntax-highlighted output with one-click copy
- Remembers your schema and your last 8 questions (stored in your browser only)

## Running it

It's a single static file (`index.html`) with no build step.

- **Locally:** open `index.html` in a browser.
- **Hosted:** deploy to GitHub Pages, Vercel, or Netlify as a static site.

Outside Claude, the app asks for an Anthropic API key. The key is saved in your browser's local storage and sent only to `api.anthropic.com`. When opened as a Claude artifact, it uses the viewer's Claude account instead and needs no key.

> Don't host this publicly with your own key baked in. Each visitor should use their own key.

## Stack

Vanilla HTML, CSS and JavaScript · Anthropic Messages API (`claude-sonnet-5-5`)
