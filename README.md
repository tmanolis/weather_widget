# 🌤️💜 Custom Weather Widget 

This is a **clean and responsive weather widget** for **Paris**, ideal for embedding into **Notion** using **GitHub Pages**.

## ✨ Features

- Displays:
  - 📍 City: Paris
  - 📅 Local date (French format, e.g. "Samedi 14 Juin")
  - 🌤️ Weather forecast for 3 periods: morning, afternoon, evening
- Uses the free [Open-Meteo](https://open-meteo.com/) API (no API key required)
- Emoji-based weather icons using `weathercode`
- Lightweight, fully responsive, and zero dependencies
- Custom pastel background

## 📂 Files

- `index.html` — main widget file
- `background-widget.jpg` — background image used in layout

## 🚀 Deployment

1. Create a GitHub repository and upload both files at the root level
2. Enable **GitHub Pages** in `Settings > Pages`
   - Source: `Deploy from branch`
   - Branch: `main` / folder: `/root`
3. GitHub will provide a public URL (e.g. `https://your-name.github.io/paris-weather-widget/`)
4. Embed that URL into Notion using `/embed`

## ⚙️ Customization
Make changes inside `index.html` to customize the widget
1. Change the **city**:
   - Change the displayed city name:
     Replace "PARIS" with your desired city name in:
     ```html
     <div class="city">PARIS ❀</div>
     ```
   - Change the coordinates and timezone for the API:
     ```js
     fetch("https://api.open-meteo.com/v1/forecastlatitude=48.8566&longitude=2.3522&hourly=temperature_2m,weathercode&current_weather=true&timezone=Europe%2FParis")
     ```
     Update the following values:
     - `latitude` and `longitude`: Replace `48.8566` and `2.3522` with your city's coordinates.
     - `timezone`: Replace `Europe%2FParis` with your city's IANA timezone, encoded for URLs (e.g., `America%2FNew_York`).
  
2. Change the style:
- To change the style, edit the `background-image`, font or colors directly in CSS

## 📜 License

Free to use for personal or professional projects. No attribution required.

---
Built with ☀️ by [@tmanolis](https://github.com/tmanolis)
