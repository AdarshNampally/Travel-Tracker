🚀 Features:

🌐 Interactive world map

✅ Add countries by name

🗺️ Highlight visited countries in teal

🧮 Display total countries visited

🗃️ Persistent data storage using PostgreSQL

🖥️ Clean and intuitive frontend using EJS templates




🛠️ Tech Stack:


| Layer        | Technology                | Purpose                      |
| ------------ | ------------------------- | ---------------------------- |
| **Backend**  | Node.js, Express          | Server logic, routing        |
| **Database** | PostgreSQL (`pg` module)  | Store country and visit data |
| **Frontend** | HTML, CSS, EJS            | UI layout and rendering      |
| **Other**    | body-parser, static files | Middleware and asset serving |




🧑‍💻 Implementation Details
1. Server Setup (index.js)
Initializes an Express server

Connects to a PostgreSQL database named world

Uses body-parser for form parsing and serves static assets from /public

2. Database Logic
Connects using pg.Client

On homepage (/), fetches all country codes from the visited_countries table

On POST to /add:

Checks if country exists in countries table using case-insensitive partial match

Inserts its country code into visited_countries

Handles duplicate insertions and invalid countries gracefully with error messages

3. Frontend (EJS Template)
Input form to type country name

Displays an SVG world map (your <path> elements with id=country_code assumed)

Uses JavaScript to fill visited countries with a different color (teal)

Shows the total number of countries visited



📝 Future Improvements


Add user login to personalize travel tracking

Enable removal of countries

Add autocomplete suggestions for country names

Improve map responsiveness on mobile devices

Visual analytics (continent-wise stats, visited %)
