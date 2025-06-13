# Fantasy Football Rankings Tool

A drag-and-drop fantasy football rankings app with **live ADP data** that helps you create, customize, and manage your player rankings for draft day.

## 🔥 New Features

- **Live ADP Integration** - Pull real-time Average Draft Position data for PPR, Half PPR, and Standard formats
- **AI Insights Button** - Advanced analytics coming soon
- **Top 200 Players** - Focused on skill positions (QB, RB, WR, TE) for cleaner rankings
- **ADP Display** - See consensus ADP values next to each player for better draft strategy

## Features

- **Drag & Drop Ranking** - Easily reorder players by dragging them up or down (desktop & mobile)
- **Live ADP Data** - Fetch current Average Draft Position data from multiple scoring formats
- **Player Search & Filtering** - Find players by name, team, or position
- **Risk Assessment** - Mark players as Low/Medium/High risk with color coding
- **Notes System** - Add personal notes for each player (up to 100 characters)
- **Draft Mode** - Track drafted players during your live draft
- **Save & Load Rankings** - Export your rankings as JSON files
- **Printable Rankings** - Download printer-friendly HTML versions

## Live Demo

**[Try it now!](https://elamschwey.github.io/fantasy-rankings)**

## How to Use

### Getting Started with Live Data
1. **Load Live ADP** - Click "Load Live ADP" to fetch current consensus rankings
2. **Choose Scoring Format** - Select PPR, Half PPR, or Standard from the dropdown
3. **Refresh Data** - Use "Refresh ADP" to get the latest data (auto-cached for 30 minutes)

### Basic Ranking
1. **Reorder Players** - Drag and drop players to change their rankings (works on mobile!)
2. **Search** - Use the search bar to find specific players
3. **Add Notes** - Click in the notes field to add personal reminders
4. **Set Risk Levels** - Click the colored risk button (L/M/H) to cycle through risk levels
5. **Compare to ADP** - See how your rankings differ from consensus with the blue ADP values

### Draft Day Mode
1. Click **"Draft Day"** to enter draft mode
2. Click the **"D"** button next to players as they get drafted
3. Recently drafted players appear in the red section at the top
4. Use **"UNDO"** to reverse accidental drafts
5. Notes become read-only to prevent accidental changes

### Save Your Work
- Click **"Save Rankings"** to download your custom rankings
- Filename format: `YourName2025PPRRankings.json`
- Click **"Load Rankings"** to import saved rankings
- **"Download Printable"** creates a print-friendly cheat sheet

## 🎨 Visual Design

### Smart Risk Color Coding
- 🟢 **Green** - Low risk, reliable players
- 🟡 **Yellow** - Medium risk, standard picks  
- 🔴 **Red** - High risk, boom-or-bust players

### Position-Based Colors
- 🟣 **Purple** - Quarterbacks (QB)
- 🔵 **Blue** - Running Backs (RB)  
- 🟢 **Green** - Wide Receivers (WR)
- 🟠 **Orange** - Tight Ends (TE)

### ADP Integration
- **Blue ADP Values** - Shows consensus Average Draft Position next to team names
- **Real-Time Data** - Updates based on your selected scoring format
- **Smart Filtering** - Automatically loads top 200 skill position players only

## 📊 Data Sources

### Live ADP API
- **Endpoint** - `https://fantasyranker-adp-api.onrender.com/api/players`
- **Formats Supported** - PPR, Half PPR, Standard
- **Player Count** - Top 200 skill position players
- **Cache Duration** - 30 minutes for optimal performance
- **Positions Included** - QB, RB, WR, TE (excludes K and DST)

### Player Data Format
```json
{
  "rankerName": "Your Name",
  "year": 2025,
  "scoringFormat": "Half PPR",
  "players": [
    {
      "name": "Ja'Marr Chase",
      "position": "WR",
      "team": "CIN",
      "adp": 1.0,
      "id": "player-0",
      "risk": "Low",
      "notes": "Elite WR1 target",
      "overallRank": 1,
      "positionRank": 1
    }
  ],
  "draftedPlayers": []
}
```

## 🚀 Technical Features

### Mobile-First Design
- **Touch Drag & Drop** - Long-press to drag players on mobile
- **Responsive Layout** - Notes section adapts to screen size
- **Edge Detection** - Prevents accidental drags near screen edges

### Performance Optimizations
- **Debounced Search** - Smooth filtering without lag
- **Smart Caching** - ADP data cached for 30 minutes
- **Efficient Rendering** - Fast re-renders even with 200+ players

### Browser Compatibility
- **Modern Browsers** - Chrome, Firefox, Safari, Edge
- **Mobile Support** - iOS Safari, Chrome Mobile
- **No Dependencies** - Pure JavaScript, no frameworks needed

## File Management

### Live Data Operations
- **Load Live ADP** - Fetches current consensus rankings
- **Refresh ADP** - Forces fresh data fetch
- **Format Switching** - Automatically prompts to reload data when changing scoring

### Import/Export
- **Load Rankings** - Import previously saved rankings (includes customizations)
- **Save Rankings** - Downloads complete rankings with all your data
- **Download Printable** - Creates printer-friendly cheat sheet
- **Filename Convention** - `[YourName][Year][ScoringFormat]Rankings.json`

## 🔧 Setup & Deployment

### Local Development
1. Clone the repository
2. Open `index.html` in a web browser
3. No build process required!

### GitHub Pages Deployment
1. Push to a GitHub repository
2. Enable GitHub Pages in repository settings
3. Point to main branch
4. Access at `https://username.github.io/repository-name`

## API Integration

### ADP Data Source
The app connects to a live ADP API that provides:
- Current average draft positions
- Multiple scoring format support
- Filtered to relevant fantasy positions
- Cached for performance

**Note**: First API request may take 30 seconds as the backend service wakes up.

## Contributing

Ideas for future improvements:
- ✅ Live ADP integration (completed)
- ✅ Mobile drag & drop (completed)
- 🔄 AI-powered insights (in progress)
- 📈 Historical ADP trends
- 🏆 Tier-based ranking system
- 📊 Player projections integration
- 🔄 Auto-sync with popular platforms

---

*Last updated: 2025 - Now with live ADP data integration*