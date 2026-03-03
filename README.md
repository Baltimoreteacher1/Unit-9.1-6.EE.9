# ⚔️ Equation Quest RPG — 6.EE.C.9 Game Engine

A premium, narrative-driven RPG for teaching **CCSS 6.EE.C.9: Dependent & Independent Variables**

## What It Does

Students enter their name and embark on a 4-quest campaign to master equations by solving real-world problems. Each correct answer damages the enemy; wrong answers damage the player.

### Features
- ✅ **Character progression** — Levels, equipment upgrades, HP/Mana systems
- ✅ **4-quest narrative arc** — Locked quests unlock as students progress
- ✅ **3 problem types** — Identify variables, write equations, analyze relationships
- ✅ **Real-world contexts** — Pizza pricing, concert tickets, gardens, rentals
- ✅ **Visual polish** — Particle effects, animations, sound feedback (Tone.js)
- ✅ **Responsive design** — Desktop, tablet, mobile

## Deploy to Cloudflare Pages

### Option 1: Direct Upload (Easiest)
1. Go to https://dash.cloudflare.com → Pages
2. Click **Create a project** → **Upload assets**
3. Upload the **entire `equation-quest-rpg` folder**
4. Cloudflare auto-detects `index.html` as entry point
5. Done! Share the URL with students

### Option 2: GitHub + Auto-Deploy (Recommended)
1. Create a GitHub repo
2. Push this folder to `main` branch
3. In Cloudflare Pages, connect your GitHub account
4. Select the repo → Auto-deploys on every push
5. Live URL appears instantly

## File Structure
```
equation-quest-rpg/
├── index.html          # Single-file game (all CSS + JS embedded)
├── README.md           # This file
└── _redirects          # (Optional) For SPA routing
```

## Customization

### Change Problem Difficulty
Edit the `quests` array in `index.html`:
```javascript
{
    id: 1,
    enemy: { name: '🤖 Equation Guardian', hp: 50 },  // Increase hp for harder
    reward: { xp: 250 },
}
```

### Add New Problem Scenarios
```javascript
scenarios: [
    { 
        context: 'Movie Tickets: $12 each',
        independent: 'Tickets', 
        dependent: 'Cost', 
        expression: 'y = 12x' 
    },
]
```

### Change Colors
Edit CSS variables at top of `<style>`:
```css
:root {
    --primary: #00d4ff;      /* Cyan */
    --secondary: #ff006e;    /* Pink */
    --accent: #ffbe0b;       /* Yellow */
}
```

## Standards Alignment

**CCSS 6.EE.C.9**: "Use variables to represent two quantities in a real-world problem that change in relationship to one another; write an equation to express one quantity, thought of as the dependent variable, in terms of the other quantity, thought of as the independent variable."

This game teaches:
- ✅ Identifying independent vs dependent variables
- ✅ Writing equations from word problems
- ✅ Analyzing relationships via substitution
- ✅ Real-world mathematical modeling

## Teacher Notes

- **No login required** — Students just enter their name
- **Progress persists** — Uses browser localStorage (resets on clear)
- **Accessible** — High contrast, large text, keyboard support
- **Flexible pacing** — Students can repeat quests anytime
- **Progression** — Quest 2+ unlock after beating Quest 1

## Browser Support

- ✅ Chrome, Edge, Firefox, Safari (latest)
- ✅ iPad/tablet (responsive)
- ✅ Mobile (stacks vertically)
- ✅ Audio works on most browsers (may require user interaction first)

## Technical Stack

- **HTML5** — Single-file, no build needed
- **CSS3** — Animations, gradients, flexbox
- **Vanilla JavaScript** — No dependencies (except Tone.js from CDN)
- **Tone.js** — Sound effects (optional, fails gracefully)

## License

Free to use in classrooms. Built for 6th grade math educators.

---

**Made with ❤️ for equation mastery**
