TWINDRIFT: How to Run

Two cats. One set of controls. Left is right.

A browser puzzle game for Pixathon, Problem Statement 4: Open Innovation Puzzles. The whole game is one HTML file, so there is nothing to install or build.

Goal: put the blue cat on the blue diamond and the orange cat on the orange ring. The orange cat mirrors your left and right.

Quick start (30 seconds)
Download or clone this repository.
Open index.html in any modern browser (Chrome, Edge, Firefox, Safari).
Click PLAY.

That is all. No Node.js, no npm, no server, no build step.

bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
# then double-click index.html, or:
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
Other ways to run it
Option A: local web server (optional)

Use this if your browser blocks something when opening the file directly. Run one of these inside the project folder, then open http://localhost:8000.

bash
# Python 3
python -m http.server 8000

# or Node.js
npx serve .
Option B: play it online with GitHub Pages
Make sure the game file is named index.html in the repository root.
Go to Settings > Pages.
Under Build and deployment, set the source to Deploy from a branch.
Choose the main branch and the / (root) folder, then click Save.
After a minute, your game is live at https://<your-username>.github.io/<repo-name>/.
Option C: play on your phone
Open your GitHub Pages link in the phone browser.
Swipe on the board to move, or use the on-screen pad.
On iPhone, use Share > Add to Home Screen for a full-screen feel.
Requirements
Any modern browser from the last few years
JavaScript enabled
Internet is optional. It is only used to load the pixel font (Silkscreen from Google Fonts). Offline, the game falls back to a monospace font and plays the same.
Controls
Input	Action
Arrow keys or WASD	Move both cats
Swipe on the board	Move (touch screens)
On-screen pad	Move (touch screens)
Z	Undo
R	Restart level
H	Hint
Esc	Back to level select
Enter	Continue on the level-clear screen
How to play
Press PLAY, then choose Easy, Medium, Hard or Expert.
Pick a level. Each tier has 10, and clearing one unlocks the next.
Move both cats at once. Blue does what you press. Orange copies up and down, but swaps left and right.
Walls stop each cat on its own. The cats can never share a square, and a blocked move costs nothing.
Finish in par moves or fewer for 3 stars. Within 3 moves of par gives 2 stars. Using a hint caps you at 2 stars.
Troubleshooting
Problem	Fix
Page is blank	Make sure you opened the .html file in a browser, not in a text editor. Check that JavaScript is enabled.
No sound	Browsers only allow audio after a click. Click PLAY, and check the SOUND toggle on the main menu.
Keys do nothing	Click on the page once to give it focus.
Progress disappeared	Progress is saved in your browser's local storage. Clearing site data or using a private window resets it.
GitHub Pages shows 404	Check that the file is named index.html in the root of the branch you selected, then wait a minute and refresh.
Pixel font missing	You are offline or blocking Google Fonts. The game still works with a fallback font.
Project structure
.
├── index.html   # the whole game: logic, graphics and UI
└── README.md
Tech

Plain HTML, CSS and JavaScript. Canvas 2D for graphics and the Web Audio API for sound. No frameworks and no dependencies.

Every one of the 40 levels is generated from a fixed seed and checked with a breadth-first search, which proves the level is solvable and sets its par to the true best score.

Credits

Created by Rohit for Pixathon. Built with AI assistance (Claude by Anthropic).
