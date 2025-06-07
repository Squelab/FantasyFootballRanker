# Fantasy Football Rankings Tool

A drag-and-drop fantasy football rankings app that helps you create, customize, and manage your player rankings for draft day.

## Features

- **Drag & Drop Ranking** - Easily reorder players by dragging them up or down
- **Player Search & Filtering** - Find players by name, team, or position
- **Risk Assessment** - Mark players as Low/Medium/High risk with color coding
- **Notes System** - Add personal notes for each player (up to 100 characters)
- **Draft Mode** - Track drafted players during your live draft
- **Save & Load Rankings** - Export your rankings as JSON files

## Live Demo

**[Try it now!](https://elamschwey.github.io/fantasy-rankings)**

## Screenshots

*Add some screenshots here of the app in action*

## How to Use

### Basic Ranking
1. **Reorder Players** - Drag and drop players to change their rankings
2. **Search** - Use the search bar to find specific players
3. **Filter by Position** - Select QB, RB, WR, TE, K, or DST
4. **Add Notes** - Click in the notes field to add personal reminders
5. **Set Risk Levels** - Click the colored risk button (L/M/H) to cycle through risk levels

### Draft Day Mode
1. Click **"Draft Day"** to enter draft mode
2. Click the **"D"** button next to players as they get drafted
3. Recently drafted players appear in the red section at the top
4. Use **"UNDO"** to reverse accidental drafts

### Save Your Work
- Click **"Save Rankings"** to download your custom rankings
- Filename format: `YourName2025PPRRankings.json`
- Click **"Load Rankings"** to import saved rankings

### Player Data Format
```json
{
  "rankerName": "PFF",
  "year": "2025", 
  "scoringFormat": "Half PPR",
  "players": [
    {
      "name": "Saquon Barkley",
      "position": "RB",
      "team": "PHI",
      "id": "player-0",
      "risk": "Medium",
      "notes": "",
      "overallRank": 1,
      "positionRank": 1
    }
  ]
}
```

## 🎨 Features in Detail

### Smart Risk Color Coding
- 🟢 **Green** - Low risk, reliable players
- 🟡 **Yellow** - Medium risk, standard picks  
- 🔴 **Red** - High risk, boom-or-bust players

### Position-Based Colors
- 🟣 **Purple** - Quarterbacks (QB)
- 🔵 **Blue** - Running Backs (RB)  
- 🟢 **Green** - Wide Receivers (WR)
- 🟠 **Orange** - Tight Ends (TE)
- 🩷 **Pink** - Kickers (K)
- ⚫ **Gray** - Defense/Special Teams (DST)

### Draft Tracking
- Remove players from rankings as they're drafted
- See last 3 drafted players in "Recently Drafted" section
- Undo drafts if you make mistakes
- Maintain original rankings even after players are drafted

## File Management

### Importing Data
- **Load Rankings** - Import previously saved rankings (includes your custom notes, risk levels, and order)
- **Load Player Data** - Import basic player lists in JSON format

### Exporting Data
- **Save Rankings** - Downloads complete rankings with all your customizations
- **Filename Convention** - `[YourName][Year][ScoringFormat]Rankings.json`
- **Example** - `John2025PPRRankings.json`

## Technical Details

- **Built with** - HTML5, Tailwind CSS, Vanilla JavaScript
- **No Dependencies** - Runs entirely in the browser
- **Mobile Friendly** - Responsive design works on all devices
- **Local Storage** - No data leaves your browser
- **GitHub Pages Ready** - Easy to deploy and share

## Contributing

Feel free to fork this repo and submit pull requests! Some ideas for improvements:
- Player injury status tracking
- ADP (Average Draft Position) integration  
- Tier-based ranking system
- CSV export functionality
- Dark mode toggle

## License

MIT License - feel free to use this for your league!

## Made for Champions

Built by the back-to-back champ, for fantasy football wanna be-s.