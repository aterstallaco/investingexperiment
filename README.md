# Read-Only Portfolio Tracker Setup

This is the **public** version of your investing experiment tracker. It loads portfolio data from a static JSON file instead of localStorage.

## Files Included

1. **tracker.html** — The read-only public tracker page
2. **family-investing-data-SAMPLE.json** — Example JSON structure

## How It Works

### Step 1: Enter Data Using Your Admin Tracker (index.html)
- Keep using your existing `index.html` as your **admin panel**
- Add all family members and their stock picks
- Make any updates/edits as needed

### Step 2: Export the JSON
- Click the **"Export"** button in your admin tracker
- This downloads a file called `family-investing-data.json`

### Step 3: Upload to GitHub
1. Go to your GitHub repository: `aterstallaco.github.io/investingexperiment/`
2. Click "Add file" → "Upload files"
3. Upload/replace the `family-investing-data.json` file
4. Commit the changes

### Step 4: The Public Tracker Auto-Updates
- The public tracker automatically reads from `family-investing-data.json`
- Live stock prices refresh every 5 minutes
- News feed updates every 15 minutes
- Everyone sees the same leaderboard and portfolios

## GitHub Pages Setup

Upload these files to your repository:
```
aterstallaco.github.io/investingexperiment/
├── Outline.html                    (your guidelines page - already there)
├── index.html                      (your admin tracker - keep private/local)
├── tracker.html                    (public tracker - upload this)
└── family-investing-data.json      (exported data - upload this)
```

**Public URL:** `https://aterstallaco.github.io/investingexperiment/tracker.html`

## Important Notes

### What's Different from index.html?
✅ **REMOVED:**
- "Add Member" button
- "Add Stock" forms
- Edit/Delete buttons
- Import button (data comes from JSON only)

✅ **KEPT:**
- Leaderboard with live rankings
- Portfolio cards with holdings
- Stock tables with live prices
- Market news feed
- Refresh buttons for prices and news

### Updating Data
Every time you want to update the tracker:
1. Open your local `index.html`
2. Make changes
3. Click "Export Data"
4. Upload the new JSON to GitHub
5. Public tracker shows new data within ~1 minute (GitHub Pages cache)

### JSON Format
When you export from your admin tracker, it creates this structure:
```json
{
  "people": [
    {
      "id": "p001",
      "name": "Sarah",
      "stocks": [
        {
          "id": "s001",
          "symbol": "AAPL",
          "shares": 1,
          "buyPrice": 150.25,
          "buyDate": "2026-02-10"
        }
      ]
    }
  ],
  "updated": 1738800000000
}
```

## Troubleshooting

**"Failed to load portfolio data"**
- Make sure `family-investing-data.json` exists in the same directory as `tracker.html`
- Check that the JSON file is valid (use the Export button from index.html)
- Wait a minute after uploading for GitHub Pages to update

**Stock prices not updating**
- Click the "Refresh Prices" link at the bottom
- Prices auto-refresh every 5 minutes
- Some stocks may not be available on Yahoo Finance

**News not loading**
- Click "Refresh" in the news section
- News auto-refreshes every 15 minutes
- Only shows news for stocks in the active portfolio

## Design Match
This tracker uses the **exact same design** as your Guidelines page and admin tracker:
- Libre Baskerville + Source Sans 3 fonts
- Navy/Cream/Gold color palette
- White cards on cream background
- Gold accents for leaders and key data
