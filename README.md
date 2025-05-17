# 🏠 Student Renting Map

An interactive web map that helps students find affordable apartments in major Polish cities: Kraków, Warsaw, and Wrocław.  
The project is fully responsive and powered by open map technologies and Google Sheets as a backend.

## ✨ Features

- 🎯 View listings directly on the map using colorful markers based on apartment type  
- 📋 Click on a marker to view apartment details: price, photo, description, and link to offer  
- 🔄 Live data updates directly from a Google Sheet (no database needed)  
- 🎨 Custom design for desktop and mobile — different backgrounds and layout  
- 🗺️ Toggleable legend on mobile, collapsible info panel  
- ✅ SEO meta description + favicon  
- 📩 Contact section & feedback form  
- 🧭 Custom marker colors and dynamic layer styling  

## 🚀 Technologies Used

- HTML + CSS + vanilla JavaScript  
- MapLibre GL JS for open-source interactive maps  
- OpenFreeMap for map tile styling  
- Google Sheets as a CMS-like backend  
- opensheet.elk.sh API to pull spreadsheet data as JSON  

## 🏗️ How I built this project

This project was created from scratch based on a real need: to help students easily browse and compare apartments visually on a map.

### Idea & Planning

The goal was to build a city selector → map viewer → apartment details experience in the most minimal, no-framework way.

### Mapping with OpenFreeMap + MapLibre

- Used `MapLibre GL JS` to render the vector map  
- Integrated OpenFreeMap for free, visually appealing tile styles  
- Configured OpenFreeMap’s bright theme  

### Custom Markers & Dynamic Styling

- Points are rendered using `map.addLayer()` with a `"circle"` layer  
- Color-coded each marker dynamically using `["match", ["get", "typ"], ...]`  
- Marker colors:  
  - 🔴 `kawalerka`: red  
  - 🟢 `2-pokojowe`: green  
  - 🔵 `3-pokojowe`: blue  
  - 🟣 `4-pokojowe`: purple  

### Google Sheets as a CMS

- Apartment data is added manually in a Google Sheet  
- Accessed via `https://opensheet.elk.sh/{sheetID}/{tabName}`  
- Auto-refreshed every 15 seconds using `setInterval(fetchData, 15000)`  

### UI/UX & Responsiveness

- Two separate layouts:
  - **Desktop**: full map, sidebar, legend  
  - **Mobile**: custom skyscraper background, floating billboard interface  

- Interactive elements:
  - 📌 Legend toggle  
  - ℹ️ Instruction popup with dismiss button  
  - 📨 Contact panel in the bottom corner  
  - 🛠️ “Report Listing” button per apartment  

### Deployment-Ready

- SEO-optimized (`<meta name="description">`)  
- Includes favicon and mobile-friendly backgrounds  
- Ready to host statically (e.g. GitHub Pages, Netlify)  

## 📫 Contact

Made with 💻 by **AroGoat**  
📧 Email: `zenekorgin@gmail.com`

