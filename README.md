Meditation app
A minimalist meditation and relaxation web app that pairs ambient video loops with synchronized audio and a built-in countdown timer. 

Features

Fullscreen looping background video for each scene
Ambient audio playback synced to the video
1-minute countdown timer per session
Three relaxation modules: Waves, Nature, Rain
Simple, distraction-free UI

📁 Project Structure
meditation-app/
│
├── index.html          # Landing page with module selection
├── style.css           # Global styles
├── mainScreen.mp4      # Background video for landing page
│
├── waves/
│   ├── waves.html
│   ├── waves.js
│   ├── waves.mp4
│   └── waves.mp3
│
├── nature/
│   ├── nature.html
│   ├── nature.js
│   ├── nature.mp4
│   └── nature.mp3
│
└── rain/
    ├── rain.html
    ├── rain.js
    ├── rain.mp4
    └── rain.mp3

    
Getting Started
No dependencies or build steps required — this is pure HTML, CSS, and JavaScript.

Clone the repository:

bash   git clone https://github.com/your-username/serenity-app.git

Add your .mp4 video and audio files to the appropriate module folders.
Open index.html in your browser.


Note: Browsers block autoplay with audio on mobile. The play button(mobile only: max-width: 800px) inside each module is required to start both the audio and video together — this is intentional behavior.

How It Works
Each module (waves, nature, rain) follows the same pattern:

A looping background video plays silently on load
Clicking the play button starts both the ambient audio and the video with sound
A countdown timer runs for 1 minute, then stops automatically

The timer logic lives in each module's .js file:
jsconst timer = 1; // minutes
let amountTime = timer * 60;

let timerid = setInterval(calculateTime, 1000);

Customization

Change session length: Edit the timer value in any module's .js file (e.g. const timer = 5 for 5 minutes).
Swap videos/audio: Replace the .mp4 source files in each module folder.
Add a new module: Duplicate an existing module folder, update the HTML source paths, and add a button on index.html.

Browser Support
Works in all modern browsers. Chrome and Edge offer the best autoplay support for muted video.
