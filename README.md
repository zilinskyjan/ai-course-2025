# AI Course: Understanding LLM Output

A Quarto-based course — "Understanding LLM Output: A Practical Guide for Social Scientists" — published via GitHub Pages.

## Setup

1. Install [Quarto](https://quarto.org/docs/get-started/)
2. Install R and the packages used in `ai-course.qmd` (notably `ellmer`)

## Local preview

```bash
quarto preview ai-course.qmd
```

Opens a live-reloading preview in your browser.

## Render

```bash
quarto render ai-course.qmd
```

Output: `index.html` (self-contained, all assets embedded).

## Publishing to GitHub Pages

### First-time setup

1. Create a GitHub repo (e.g. `zilinskyjan/ai-course-2025`)
2. Initialize and push:

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin git@github.com:zilinskyjan/ai-course-2025.git
git push -u origin main
```

3. Publish with Quarto's built-in GitHub Pages support:

```bash
quarto publish gh-pages
```

This renders the document, pushes output to a `gh-pages` branch, and configures GitHub Pages automatically. Your course will be live at:

**https://zilinskyjan.github.io/ai-course-2025/**

### Subsequent updates

After editing `ai-course.qmd`:

```bash
quarto publish gh-pages
```

That's it — one command to re-render and deploy.

## Linking from your main website

In your main website's `src/_data/site.json`, link to the published page:

```json
{ "title": "AI Course", "url": "https://zilinskyjan.github.io/ai-course-2025/", "icon": "Laptop", "external": true, "course": true }
```

## Files

| File | Purpose |
|------|---------|
| `ai-course.qmd` | Course source (Quarto + R code) |
| `styles.scss` | Custom styles |
