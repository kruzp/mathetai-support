# Mathetai
#### Video Demo:  https://youtu.be/YuJIe6Z4iqw
#### Description:
# Mathetai

Mathetai is a modern, multi-platform Bible study and thinking tool designed to empower deep, structured exploration of Scripture. Inspired by the Greek word "μαθηταί" (meaning *disciples* or *learners*), the app blends the timeless practice of reading, comparing, and meditating on the Bible with cutting-edge software design and intuitive usability.

This project is part of my CS50 coursework, but it is also the foundation for a production-ready application I intend to publish to the App Store. 

---

## Features

- **Bible Reading Pane** – Displays the selected book, chapter, and verse in a clean, focused layout.
- **Notes Panel** – Styled like a terminal for minimal distraction, enabling fast and organized note-taking.
- **Modern, Minimal UI** – White-on-black or black-on-white themes for visual comfort.
- **Data Syncing** – Notes and settings sync securely across devices via iCloud.

---

## File Descriptions

Below are the key files in this project and their purposes:

### `MathetaiApp.swift`
- The entry point for the application.
- Configures the main scenes for iOS, iPadOS, and macOS.
- Initializes the primary views and handles app-wide state.

### `ContentView.swift`
- The main container view of the application.
- Houses the **Bible Reading Pane**, **Notes Panel**, and layout logic for split views.
- Manages tab states and UI responsiveness.

### `SidebarView.swift`
- Displays a navigable list of books and chapters.
- Triggers content updates in the main reading pane.

### `BibleTextView.swift`
- Responsible for rendering verses in the chosen translation.
- Handles both local and API-sourced text data.

### `NotesView.swift`
- A markdown-compatible note-taking interface styled to resemble a terminal.
- Stores notes locally and syncs via iCloud.

### `ComparisonView.swift`
- Manages the layout for side-by-side translation display.
- Optimized to minimize re-rendering when switching translations.

### `BibleDataManager.swift`
- Handles local storage of Bible translations.
- Manages API calls for additional translations.
- Caches API responses for offline use.

### `ThemeManager.swift`
- Centralizes theme selection (light/dark modes).
- Updates views in real-time as the user switches preferences.

---

## Design Choices

During development, I debated several architectural and UI decisions:

1. **Why SwiftUI over UIKit?**  
   SwiftUI allows for declarative, cross-platform UI building with less boilerplate. Given my goal to support macOS, iOS, and iPadOS, it was the clear choice.

2. **Why local storage for common translations?**  
   I wanted Mathetai to work offline. Storing common translations locally ensures users can study without internet access, while keeping less-common translations available via API to save storage space.

3. **Why a terminal-style Notes Panel?**  
   The clean, monospaced aesthetic encourages focus. It subtly signals that the user is “working” rather than browsing.

4. **Why minimal color schemes?**  
   High-contrast black/white designs reduce visual fatigue and emphasize the text itself, not the interface.

5. **Why tabs and split views?**  
   Serious study often requires comparing multiple passages at once. This feature mirrors the workflow of professional editors like VS Code.

---

## How It Works

1. **Navigation** – The sidebar lets you choose books and chapters.
2. **Reading** – The Bible Reading Pane loads the text instantly from local storage (or via API if needed).
3. **Comparing** – Split view mode opens a second Bible pane for side-by-side translation comparison.
4. **Notetaking** – The Notes Panel can be opened in any tab, allowing you to annotate while reading.
5. **Syncing** – Changes to notes or settings are stored in iCloud and reflected across devices.

---

## Future Improvements

- **Highlighting & Tagging** – Highlight verses and tag them for later.
- **Search Functionality** – Search across translations and notes.
- **Export Options** – Export notes as Markdown or PDF.
- **Community Features** – Share studies with other users.

---

## Acknowledgements

This project was inspired by the need for a high-quality, distraction-free Bible study tool.  
Special thanks to the CS50 community for fostering the technical skills and discipline that made Mathetai possible.
