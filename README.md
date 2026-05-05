# ChordPro Song Viewer

**ChordPro Song Viewer** is a lightweight web application that makes it easy to search, display, and interact with songs written in ChordPro-style format. Built with Node.js and vanilla JavaScript, the app provides a clean browser-based interface for viewing lyrics and chords, while also allowing users to transpose songs instantly.

Designed for simplicity, speed, and readability, this project demonstrates how a custom Node.js server can deliver a functional music-viewing experience without relying on external packages or frameworks.

This project was created for **Carleton University's COMPSCI Program**.

## Overview

ChordPro Song Viewer allows users to enter the name of a song, load the matching file from the local song library, and view the formatted result directly in the browser. Chords are extracted from ChordPro-style notation and displayed above the corresponding lyrics, making the song easier to read and play.

The application also includes transposition controls, allowing musicians to quickly shift chords up or down by semitone and return to the original key when needed.

## Key Features

- Search and load songs from a local song collection
- Display lyrics and chords in a clean, readable layout
- Parse basic ChordPro-style chord notation
- Transpose chords up or down by semitone
- Restore songs to their original key
- Visually distinguish original chords from transposed chords
- Serve files using a custom Node.js HTTP server
- Run without external npm dependencies

## Tech Stack

- **Node.js**
- **JavaScript**
- **HTML**
- **CSS**

The server uses only built-in Node.js modules:

- `http`
- `fs`
- `url`

No external packages are required.

## Project Structure

```text
.
├── html/
│   ├── buttonHandlers.js
│   ├── chords.js
│   ├── client.js
│   ├── eventListeners.js
│   ├── favicon.ico
│   └── index.html
├── songs/
│   ├── All Shook Up.txt
│   ├── Brown Eyed Girl.txt
│   ├── Never My Love.txt
│   ├── Peaceful Easy Feeling.txt
│   └── Sister Golden Hair.txt
├── server.js
└── README.md
```

## Getting Started

### Prerequisites

Make sure **Node.js** is installed on your machine.

You can check your installed version with:

```bash
node --version
```

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository-name.git
```

Move into the project folder:

```bash
cd your-repository-name
```

No additional installation is required because the project does not use external npm packages.

## Running the Application

Start the server with:

```bash
node server.js
```

Then open the application in your browser:

```text
http://localhost:3000/index.html
```

You can also access the app from:

```text
http://localhost:3000/
```

## Example Song Searches

The application currently includes the following songs:

```text
All Shook Up
Brown Eyed Girl
Never My Love
Peaceful Easy Feeling
Sister Golden Hair
```

Enter one of these titles in the search field to load the song.

The search title should match the song filename in the `songs/` folder without the `.txt` extension.

## How the Application Works

1. The user opens the web app in the browser.
2. The user enters a song title into the search field.
3. The client sends a request to the Node.js server.
4. The server searches the local `songs/` directory for the matching song file.
5. If the song exists, the server returns the song data to the browser.
6. The client parses the ChordPro-style text.
7. Lyrics and chords are displayed in a formatted, musician-friendly layout.
8. The user can transpose the song up, transpose it down, or return it to the original key.

## ChordPro Format Example

Songs are stored as plain text files using a simple ChordPro-style format:

```text
{title: Brown Eyed Girl -Van Morrison}

[G]Hey, where did [C]we go, da[G]ys when the ra[D]ins came
```

The application detects chords inside square brackets and places them above the matching lyric positions.

## Transposition

ChordPro Song Viewer includes built-in transposition controls:

- **Transpose Up** raises all chords by one semitone
- **Transpose Down** lowers all chords by one semitone
- **Original Key** restores the song to its starting key

This makes the app useful for quickly adapting songs to different vocal ranges or instrument preferences.

## Why This Project Is Useful

ChordPro Song Viewer offers a simple and practical way to manage chord sheets in the browser. Instead of reading raw ChordPro text files, users can view songs in a cleaner layout that separates chords from lyrics and supports instant key changes.

The project also highlights important web development concepts, including client-server communication, file handling, DOM manipulation, event handling, and modular JavaScript organization.

## Notes and Limitations

- Song searches currently depend on matching local filenames.
- The app supports basic ChordPro-style notation, but not every advanced ChordPro feature.
- Songs are loaded from local text files rather than a database.
- The server is intended for local development and academic demonstration.

## Future Improvements

Potential future improvements could include:

- Partial or fuzzy song search
- A larger song library
- Database-backed song storage
- Support for additional ChordPro directives
- Improved styling for mobile devices
- Playlist or favourites functionality
- User-uploaded song files

## Author

Ahmad Kanaan

## License

This project was created for academic purposes. Add a license before using, modifying, or distributing it publicly.
