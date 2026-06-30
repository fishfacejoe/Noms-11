# Party Ranking Sorter

This project is a simple single-page application template that allows users to rank songs from a list by comparing them in duels.

## Project Structure

```
party-ranking-sorter-template/
├── index.html
├── style.css
├── script.js
├── songList.json
├── config.js
└── README.md
```

## Features

- Autosave to the local storage after each duel.
- Can load saved result or show final result if sorter was previously completed.
- Options for choosing between mp3 and video files when sorting.
- Region selection for catbox links (EU, NA1, NA2).

## Setting Up a Custom Sorter

To set up a custom sorter for your specific party ranking, follow these steps:

1. **Update `songList.json`:**
   - Replace the content of `songList.json` with your own list of songs. Each song should have an `id`, `anime`, `name`, `video`, and optionally an `mp3` field.
   - Links should be either animemusicquiz catbox links or YouTube links.
   - Example:
     ```json
     [
         {
             "id": 1,
             "anime": "Your Anime Title",
             "name": "Your Song Name",
             "video": "https://your-video-url.com",
             "mp3": "https://your-mp3-url.com"
         },
         {
             "id": 2,
             "anime": "Another Anime Title",
             "name": "Another Song Name",
             "video": "https://another-video-url.com",
             "mp3": "https://another-mp3-url.com"
         },
         {
             "id": 3,
             "anime": "Example Anime",
             "name": "Example Song",
             "video": "https://eudist.animemusicquiz.com/example.webm",
             "mp3": "https://eudist.animemusicquiz.com/example.mp3"
         }
     ]
     ```

2. **Update the Title and Description in `config.js`:**
   - Open `config.js` and change the `title` and `description` variables to match your custom sorter.
   - Also you **will** have to change `localStoragePrefix` if you plan on hosting multiple github-pages from a single account (there is an issue of shared `localStorage` if base URL is the same, so need to differentiate `localStorage` for different party rankings)
   - Example:
     ```javascript
     const config = {
         localStoragePrefix: "your-party-rank-sorter",
         title: "Your Custom Party Rank Sorter",
         description: "Party rank sorter for your custom list of songs."
     };
     ```

## Credit

Most of the project was taken from this repo by FlatoLitou: [Winter2025ED](https://github.com/Flatolitou/Winter2025ED).
