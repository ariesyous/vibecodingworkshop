# Vibe Coding Prompt Guide & Cheat Sheet

> **Workshop:** Defying Gravity — AI Agentic Vibe Coding
> **Tools:** Gemini CLI + Google Antigravity
> **Keep this open while you build!**

---

## The Golden Rules

1. **Be specific.** The more detail you give, the better the output.
2. **Set context first.** Tell the AI what you're building, what tech you're using, and what API you're calling.
3. **Work in small steps.** Don't ask for everything at once — build incrementally.
4. **Feed errors back.** Copy-paste the exact error message. Don't paraphrase.
5. **Iterate, don't restart.** Refine what you have. Say "change the background to dark blue" not "start over."

---

## Starter Prompts by Track

### Track 1A — "Zero-G" Fact Generator

**Step 1: Scaffold the page**
```
Create a single HTML file with embedded CSS and JavaScript.
It should have a centered card layout with a space-themed
dark background (dark navy, stars). Include a title that says
"Zero-G Facts" and a button that says "Float a New Fact."
```

**Step 2: Add the API calls**
```
Add JavaScript that does two things when the button is clicked:
1. Fetches a random fun fact from https://uselessfacts.jsph.pl/api/v2/facts/random
2. Fetches a random duck image from https://random-d.uk/api/random
Display the fact text and duck image inside the card.
```

**Step 3: Add the floating animation**
```
Make the duck image slowly float around the screen using CSS
animations. It should drift up and down gently, like it's
in zero gravity. Use CSS keyframes, not a physics library.
```

---

### Track 1B — Nostalgia Physics Engine

**Step 1: Build the search page**
```
Create an HTML page with a search bar at the top. When the user
types a name and presses Enter, fetch Amiibo data from:
https://www.amiiboapi.com/api/amiibo/?name={searchTerm}
Display each result as a card showing the character name and image.
```

**Step 2: Add Matter.js physics**
```
Add the Matter.js library from CDN (https://cdnjs.cloudflare.com/ajax/libs/matter-js/0.19.0/matter.min.js).
When Amiibo images load, create physics bodies for each image and
let them drop onto the page with low gravity (0.1 instead of 1).
They should bounce off the walls and each other.
```

---

### Track 1C — "Corporate Gravity" Defier

**Step 1: Build the CLI tool**
```
Write a Python script that fetches a corporate buzzword phrase
from https://corporatebs-generator.sameerkumar.website/ and
prints it to the terminal.
```

**Step 2: Add the translator**
```
Now modify the script so it takes the corporate phrase and
rewrites it in two ways:
1. "Space Captain" style (dramatic, sci-fi captain dialogue)
2. "Plain English" style (simple, clear language)
Use string templates to do the rewriting — you don't need an
external AI API, just creative mapping of corporate jargon
to fun alternatives.
```

---

### Track 2A — Mission Briefing Terminal

**Step 1: Fetch launch data**
```
Write a Python script using the requests library that fetches
upcoming space launches from:
https://ll.thespacedevs.com/2.2.0/launch/upcoming/?limit=5
Parse the JSON response and print the name, date, and location
of each launch.
```

**Step 2: Build the Rich terminal UI**
```
Install the Rich library (pip install rich). Refactor the script
to display the launch data in a beautiful terminal table using
Rich. Add a countdown timer showing days/hours until each launch.
Use Rich panels and colored text to make it look like a mission
briefing terminal.
```

---

### Track 2B — Quantum "Bargain Hunter"

**Step 1: Create the wishlist**
```
Create a file called wishlist.json with this structure:
[
  {"title": "Portal 2", "maxPrice": 5.00},
  {"title": "Hades", "maxPrice": 10.00},
  {"title": "Celeste", "maxPrice": 8.00}
]
Then write a Python script that reads this file and for each
game, queries the CheapShark API:
https://www.cheapshark.com/api/1.0/deals?title={game_title}&limit=3
```

**Step 2: Generate the HTML report**
```
Take the deal results and generate a styled HTML report file
called "deals_report.html". Sort deals by savings percentage
(best deals first). Use a clean, dark-themed design with cards
for each game showing: game title, current price, normal price,
savings percentage, and a link to the deal.
```

---

### Track 2C — Academic Abstractor

**Step 1: Query arXiv**
```
Write a Python script that queries the arXiv API for recent
papers about gravity or propulsion:
http://export.arxiv.org/api/query?search_query=all:gravity+OR+all:propulsion&max_results=10
Parse the XML response using the xml.etree.ElementTree library.
Extract title, authors, abstract, and published date for each paper.
```

**Step 2: Save to SQLite**
```
Create a SQLite database called papers.db with a table called
'papers' with columns: id, title, authors, abstract, published_date.
Insert the parsed arXiv data into this table. Also generate a
Markdown summary file called papers_summary.md with a formatted
list of all papers.
```

---

### Track 2D — Art Remix Pipeline

**Step 1: Pull artwork metadata**
```
Write a Python script that fetches artwork data from the Art
Institute of Chicago API:
https://api.artic.edu/api/v1/artworks?limit=10&fields=id,title,artist_display,date_display,medium_display,image_id,description
For each artwork, build the image URL using:
https://www.artic.edu/iiif/2/{image_id}/full/843,/0/default.jpg
```

**Step 2: Generate sci-fi remixed descriptions**
```
For each artwork, take the historical description and create
a new sci-fi/cyberpunk version. Use string templates that
transform art terminology into futuristic equivalents.
Example: "oil on canvas" → "quantum-pigment on nanoweave substrate"
Save the remixed gallery as a styled HTML page with the original
image, original info, and the new sci-fi description side by side.
```

---

## Universal Prompt Patterns

### When something breaks
```
I ran the script and got this error:
[PASTE THE FULL ERROR HERE]
Fix it.
```

### When you want to add a feature
```
The [current thing] is working. Now add [new feature].
Don't change the existing functionality.
```

### When the output doesn't look right
```
The [element] is [problem]. Change it so that [desired behavior].
Keep everything else the same.
```

### When you're stuck
```
I'm trying to [goal]. I have [what you have so far].
What's the simplest next step to get closer to [goal]?
```

### When you want to understand the code
```
Explain what this code does in simple terms.
Focus on the main flow, not every detail.
[PASTE CODE]
```

---

## Quick Reference: Useful APIs

| API | URL | Returns |
|-----|-----|---------|
| Fun Facts | `uselessfacts.jsph.pl/api/v2/facts/random` | Random fact as JSON |
| Random Duck | `random-d.uk/api/random` | Duck image URL |
| Amiibo | `amiiboapi.com/api/amiibo/` | Nintendo character data |
| Corporate BS | `corporatebs-generator.sameerkumar.website/` | Buzzword phrase |
| Space Launches | `ll.thespacedevs.com/2.2.0/launch/upcoming/` | Launch schedule |
| CheapShark | `cheapshark.com/api/1.0/deals` | Game deal prices |
| arXiv | `export.arxiv.org/api/query` | Academic papers (XML) |
| Art Institute | `api.artic.edu/api/v1/artworks` | Artwork metadata |

---

## Gemini CLI Tips

| Command | What it does |
|---------|-------------|
| `gemini` | Start an interactive session |
| `/help` | Show available commands |
| `/chat new` | Start a fresh conversation |
| `/chat list` | See conversation history |
| Paste a file path | Gemini reads the file for context |
| `Ctrl+C` | Cancel current generation |

## Antigravity Tips

| Feature | How to use it |
|---------|--------------|
| Plan Mode | Best for complex tasks — AI creates a plan before coding |
| Fast Mode | Best for quick fixes — AI executes immediately |
| Artifacts | Check the artifacts panel to see the AI's work trail |
| Browser Preview | AI can test your web app in a built-in browser |

---

*Have fun, and remember: the best prompt is the one that gets you closer to your goal. There's no wrong way to vibe code!*
