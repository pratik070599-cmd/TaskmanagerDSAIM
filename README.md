# TaskFlow — Simple Task Manager

A responsive, dependency-free task manager you can deploy directly to Vercel or GitHub Pages.

## Features

- Create, edit, delete, and complete tasks
- Due dates, priorities, overdue and due-today indicators
- Search, filter, and sort tasks
- Interactive monthly calendar with task details
- Dashboard with total, completed, pending, overdue, and completion percentage
- Export and import tasks as JSON backups
- Responsive desktop and mobile layout

## Run locally

Open `index.html` in a browser. For a local web server, run:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Publish to GitHub

1. Create a new repository on GitHub.
2. Upload `index.html`, `styles.css`, `app.js`, `README.md`, and `vercel.json` to the repository root.
3. Commit the files.

## Deploy to Vercel

1. Sign in to https://vercel.com and select **Add New > Project**.
2. Import your GitHub repository.
3. Choose **Other** as framework preset if prompted.
4. Leave the build command empty. The output directory is the repository root (`.`).
5. Click **Deploy**.

Alternatively, deploy the unzipped folder through the Vercel CLI.

## Important: how data is stored

Tasks are stored in the browser's `localStorage`, under `taskflow.tasks.v1`. They are **not** stored on GitHub or Vercel and **do not sync between browsers or devices**. Clearing site data or using private browsing can remove them. Use **Export tasks** regularly and **Import tasks** to restore them. This app does not include accounts, shared team tasks, email notifications, or background reminders. Due-date indicators appear when the app is opened.

For cross-device sync, add authentication and a hosted database (e.g. Supabase) in a future version.

## Files

- `index.html` — page structure and form
- `styles.css` — responsive styling
- `app.js` — task logic, calendar, and browser storage
- `vercel.json` — static deployment configuration

No dependencies, API keys, or environment variables are needed.
