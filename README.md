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

<p>HTML + CSS + vanilla JavaScript<br>
MapLibre GL JS for open-source interactive maps<br>
OpenFreeMap for map tile styling<br>
Google Sheets as a CMS-like backend<br>
opensheet.elk.sh API to pull spreadsheet data as JSON<br>
</p>

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
<l1>Points are rendered using map.addLayer() with a "circle" layer.</l1>
<li>Color-coded each marker dynamically using ["match", ["get", "typ"]].</li>
<li>Marker colors:

🔴 kawalerka: red

🟢 2-pokojowe: green

🔵 3-pokojowe: blue

🟣 4-pokojowe: purple</li>
