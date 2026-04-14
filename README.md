# 🎨 Theme Switcher

A simple and elegant light/dark theme switcher built with HTML, CSS, and JavaScript. This project demonstrates DOM manipulation, CSS custom properties, and event handling.

## 🌐 Demo

[View Live Demo](https://hokkaidodev.github.io/Theme-Switcher/)

## ✨ Features

- 🌓 Toggle between light and dark theme
- ⚡ Smooth CSS transitions (0.3s)
- 🎯 Dynamic UI updates
- 💾 Clean and modular code
- 📱 Responsive design

## 🛠️ Technologies

- **HTML5** - semantic markup
- **CSS3** - CSS custom properties, grid layout, transitions
- **JavaScript (ES6)** - DOM manipulation, event handling

## 📁 Project Structure

```
Theme-Switcher/
├── index.html          # Main HTML page
├── style.css           # Styles and themes
├── app.js              # JavaScript logic
└── README.md           # This file
```

## 🚀 How to Use

1. **Clone or download the project**
   ```bash
   git clone <repo-url>
   cd Theme-Switcher
   ```

2. **Open the file in a browser**
   - Easiest: double-click on `index.html`
   - Or use Live Server in VS Code

3. **Click the switcher**
   - Click the circular button in the header to toggle the theme

## 📋 How It Works

### CSS Custom Properties

The project uses CSS variables to manage colors:

```css
.page {
  --color-page: #485268;        /* Text color */
  --bg-page: #f5f6fa;           /* Page background */
  --color-header: #333a4a;      /* Header text color */
  --bg-header: #fff;            /* Header background */
}

.page--theme--dark {
  /* Dark theme overrides the variables */
  --color-page: #f5f6fa;
  --bg-page: #485268;
  --color-header: #fff;
  --bg-header: #333a4a;
}
```

### JavaScript Functionality

When clicking the switcher:
- The `page--theme--dark` class is added/removed from the page
- Theme text is dynamically updated
- CSS custom properties automatically apply new colors

```javascript
switcher.addEventListener('click', () => {
  if (page.classList.contains('page--theme--dark')) {
    // Switch to light theme
    page.classList.remove('page--theme--dark');
    // ... update UI
  } else {
    // Switch to dark theme
    page.classList.add('page--theme--dark');
    // ... update UI
  }
});
```

## 💡 Possible Improvements

- Persist theme in `localStorage` (to remember user's choice after reload)
- Support system theme preferences
- Add smooth animations for the switcher
- Add more theme options (not just light/dark)

## 📚 Learning Value

This project is perfect for:
- Learning DOM manipulation
- Understanding CSS custom properties
- Practicing event handlers
- Demonstrating reactive design principles (basic level)

## 📄 License

MIT License - feel free to use this code!

---

**Author:** HokkaidoDev 
**Purpose:** Educational project for HTML/CSS/JavaScript course