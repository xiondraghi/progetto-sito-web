# Elden Ring Blog - UI/UX Redesign

## Project Overview
This project is a complete UI/UX redesign of a classic, legacy HTML/CSS template. The objective was to modernize the structure and aesthetics, transforming a basic layout into a sleek, dark-themed, and visually striking blog inspired by the lore and atmosphere of the videogame made by Fromsoftware: *Elden Ring*

The goal is to make a blog that will feauture characters like Messmer the Impaler, Midra, Malenia, and Ranni, with their unique characteristics and fan art. There will be a link to news regarding the character and a forum.

The main protagonist of this page is Messmer the Impaler, the poster-child of the game DLC

## Key Features & Technical Implementations
* **Modern CSS Layouts:** Transitioned from legacy fixed layouts to modern **CSS Flexbox**. This allowed for perfect alignment of the custom header, search bar, and interactive buttons.

* **Responsive Typography (rem):** Replaced static pixel (`px`) measurements with relative units (`rem`) for better scalability and accessibility across the UI.

* **Custom Nivo Slider Implementation:** * Heavily customized the legacy jQuery **Nivo Slider** plugin.
    * **Technical Workaround:** Overcame the plugin's native limitations with HTML captions by injecting custom HTML structure directly into the image `title` attributes. 
    * Forced CSS overrides using `!important` to bypass inline JavaScript styles, creating a modern, semi-transparent frosted-glass caption box (`backdrop-filter: blur`).

* **Interactive Dropdown Menu:** Implemented a custom hamburger menu that toggles a sleek dropdown via **Vanilla JavaScript**. It includes event propagation handling to ensure the menu closes automatically when clicking outside of it.

* **Replaced the outdated "Featured Content" blocks** with a dynamic "Trivia Section" (Messmer Collection), utilizing Flexbox to create a perfectly aligned grid of square image cards (using `aspect-ratio`) and action buttons.

* **UI Polish:** Removed default browser focus outlines for a cleaner aesthetic on interactive elements like buttons and links.

## Typography & Iconography
The project uses a carefully paired typography system to match the dark fantasy theme:
* **Headings:** [Syne](https://fonts.google.com/specimen/Syne) (via Google Fonts) - Used for bold, cinematic titles.

* **Body & UI Elements:** **Satoshi** (via Fontshare / Local Webfonts) - Used for clean, legible descriptions and kickers.

* **Icons:** [FontAwesome 6](https://fontawesome.com/) (via CDN) - Used for the search and hamburger menu icons.

---

## Setup & Installation

To run this project locally, simply clone the repository and open the `index.html` file in any modern web browser. No build tools or package managers are required.

### Installing the Local 'Satoshi' Font
If you are hosting the Satoshi font locally instead of using the API, follow these steps:

1. Place the `satoshi/` folder into a main `fonts/` directory in your project.
2. Place the `satoshi.css` file into your `css/` folder.
3. *(Optional)* Adapt the `url('path')` inside `satoshi.css` depending on your specific folder structure.
4. Import `satoshi.css` at the top of your main `style.css` file:
```css
   @import url('satoshi.css');