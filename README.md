# 🏠 Student Renting Map 
<p>An interactive web map that helps students find affordable apartments in major Polish cities: Kraków, Warsaw, and Wrocław. The project is fully responsive and powered by open map technologies and Google Sheets as a backend.</p>

<h1>✨ Features</h1>
<p>🎯 View listings directly on the map using colorful markers based on apartment type.<br>
📋 Click on a marker to view apartment details: price, photo, description, and link to offer.<br>
🔄 Live data updates directly from a Google Sheet (no database needed).<br>
🎨 Custom design for desktop and mobile — different backgrounds and layout.<br>
🗺️ Toggleable legend on mobile, collapsible info panel.<br>
✅ SEO meta description + favicon.<br>
📩 Contact section & feedback form.<br>
🧭 Custom marker colors and dynamic layer styling.</p>

<h1>🚀 Technologies Used</h1>
<ul>
<li>HTML + CSS + vanilla JavaScript</li>
<li>MapLibre GL JS for open-source interactive maps</li>
<li>OpenFreeMap for map tile styling</li>
<li>Google Sheets as a CMS-like backend</li>
<li>opensheet.elk.sh API to pull spreadsheet data as JSON</li>
</ul>

<h1>🏗️ How I built this project</h1>
<p>This project was created from scratch based on a real need: to help students easily browse and compare apartments visually on a map. Here's a breakdown of how it came together:</p>
<h2>Idea & Planning</h2>
<p>The goal was to build a city selector → map viewer → apartment details experience in the most minimal, no-framework way.</p>
<h2>Mapping with OpenFreeMap + MapLibre</h2>
<ul>
  <li>Used MapLibre GL JS to render the vector map.</li>
  <li>Integrated OpenFreeMap for free, visually appealing tile styles.</li>
  <li>Configured OpenFreeMap’s bright theme</li>
</ul>

<h2>Custom Markers & Dynamic Styling</h2>
<l1>Points are rendered using `map.addLayer()` with a `"circle"` layer.</l1>
<li>Color-coded each marker dynamically using `["match", ["get", "typ"]]`.</li>
<li>Marker colors:
🔴 `kawalerka`: red

🟢 `2-pokojowe`: green

🔵 `3-pokojowe`: blue

🟣 `4-pokojowe`: purple
</li>

<h2>Google Sheets as a CMS</h2>
<ul>
  <li>Apartment data is added manually in a Google Sheet.</li>
  <li>Accessed via `https://opensheet.elk.sh/{sheetID}/{tabName}`</li>
  <li>Auto-refreshed every 15 seconds using `setInterval(fetchData, 15000)`</li>
</ul>

<h2>UI/UX & Responsiveness</h2>
<ul>
  <li>Two separate layouts:</li>
  <ul>
    <li>Desktop: full map, sidebar, legend</li>
    <li>Mobile: custom skyscraper background, floating billboard interface</li>
  </ul>
  <li>Interactive elements:</li>
  <ul>
    <li>📌 Legend toggle</li>
    <li>ℹ️ Instruction popup with dismiss button</li>
    <li>📨 Contact panel in the bottom corner</li>
    <li>🛠️ “Report Listing” button per apartment</li>
  </ul>
</ul>

<h2>Deployment-Ready</h2>
<ul>
  <li>SEO-optimized `(<meta name="description">)`</li>
  <li>Includes favicon and mobile-friendly backgrounds</li>
  <li>Ready to host statically (e.g. GitHub Pages, Netlify)</li>
</ul>

<h1>📫 Contact</h1>
<p>Made with 💻 by AroGoat</p>
<p>📧 Email: zenekorgin@gmail.com</p>
