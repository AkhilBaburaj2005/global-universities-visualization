# global-universities-visualization
A dynamic project that maps and visualizes universities worldwide using geocoding and interactive mapping technologies.
📋 Project Description
This system processes university names from an input file (where.data), retrieves geographic coordinates via the OpenStreetMap Nominatim API, and stores results in a SQLite database. The data is then exported to a JavaScript file (where.js) and visualized using OpenStreetMap with OpenLayers.
Key components:
geoload.py: Batch processes locations with API rate limiting (1 request/sec)
geodump.py: Exports geographic data to JavaScript format (where.js)
where.html: Interactive map visualization interface
where.js: Contains geocoded university data
opengeo.sqlite: SQLite database for storing geodata
🛠️ Prerequisites
Python 3.6+
Required modules: sqlite3, urllib, json, ssl
DB Browser for SQLite (recommended)
Modern web browser with JavaScript enabled
🚀 Installation
bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
💻 Usage
Process Locations (Generates opengeo.sqlite):
bash
python3 geoload.py
Note: Input file where.data required
Export Data (Creates where.js):
bash
python3 geodump.py
Visualize Results:
Open where.html in a web browser
📊 Data Structure
The where.js file contains an array myData with the following structure for each entry:
javascript
[latitude, longitude, 'University Name']
Example:
javascript
[50.065703299999996, 19.918958667058632, 'AGH University of Science and Technology']
📸 Required Screenshots
Terminal Output showing successful geoload.py execution
Database Snapshot from DB Browser showing records
Map Visualization with multiple location pins in where.html
🙏 Acknowledgments
This project was developed under the guidance of Dr. Charles Russel Severance (University of Michigan) as part of the "Python for Everybody" curriculum. Data provided by OpenStreetMap under the Open Database License.
📄 License
MIT License - See LICENSE for details
