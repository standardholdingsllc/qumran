# Khirbet Qumran: Interactive 3D Archaeological Experience

An immersive first-person virtual tour of the ancient Qumran settlement, home to the community believed to have authored the Dead Sea Scrolls. Built with Three.js, this experience recreates the southwest quadrant of the main building as it may have appeared in the 1st Century CE.

![Qumran Experience](https://img.shields.io/badge/Three.js-0.160.0-blue) ![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange)

## Features

### 🏛️ Archaeological Recreation
- **Room 1 (Pantry)**: Storage area with period-accurate cylindrical jars
- **Room 2 (Assembly/Dining)**: Communal gathering space with benches
- **Room 4 (Courtyard)**: Central plastered hub with water basin and support column
- **Room 12 (Workshop)**: Small workroom for repairs and lamp maintenance
- **Room 13 (Passage)**: Transitional corridor connecting spaces
- **Room 30 (Scriptorium)**: The famous writing room with plastered tables and inkwells

### 🎮 Interactive Controls
- **WASD** - Movement (forward, left, backward, right)
- **Click + Drag** - Look around
- **Day/Night Slider** - Transition between sunlit day and oil lamp-lit night

### 🌅 Dynamic Lighting
- Procedural sky with realistic sun positioning
- Oil lamp lighting system with flickering effects
- Smooth day/night transitions affecting ambient, directional, and point lights

### 🏺 Interactive Objects
- Hover over objects to see contextual information
- Storage jars, inkwells, plastered tables, and architectural features
- Zone-based room information panel

### 🐧 Easter Egg
A time-traveling penguin with sunglasses can be found hiding in Room 30 (the Scriptorium). He always faces you as you explore!

## Technical Architecture

### Dependencies
- **Three.js v0.160.0** - 3D rendering engine (loaded via ES modules)
- **Sky addon** - Procedural sky shader

### File Structure
```
qumran_experience/
├── index.html          # Main application (self-contained)
├── image_dd26b9.png    # Penguin easter egg sprite
├── vercel.json         # Deployment configuration
└── README.md           # This documentation
```

### Key Technical Components

#### Scene Setup
- WebGL renderer with antialiasing and soft shadow maps
- Perspective camera with 60° FOV
- Procedural fog for atmosphere and distance fade

#### Materials
- Procedural noise textures for realistic wall/floor surfaces
- Physical materials for water features (clearcoat, metalness)
- Sprite materials with transparency for billboarded elements

#### Collision System
- Bounding box collision detection against walls
- Player radius of 0.5 units
- Collision-free furniture for easier exploration

#### Room Zone System
- Box3 regions define room boundaries
- Dynamic UI updates based on player position
- Contextual facts and descriptions per zone

## Running Locally

1. Start a local HTTP server in the project directory:
   ```bash
   # Python
   python -m http.server 8080
   
   # Node.js
   npx serve
   ```

2. Open `http://localhost:8080` in a modern browser

3. Click "Click to Begin" to start exploring

## Deployment

The project includes a `vercel.json` for easy deployment to Vercel:

```bash
vercel deploy
```

## Browser Compatibility

- Chrome/Edge (recommended)
- Firefox
- Safari (WebGL 2.0 required)

## Historical Context

Qumran was an ancient settlement on the northwest shore of the Dead Sea, inhabited from approximately 150 BCE to 68 CE. The site is famous for its proximity to the caves where the Dead Sea Scrolls were discovered. The scriptorium (Room 30) is particularly significant as it contained plastered writing tables and inkwells, suggesting it was where scrolls may have been copied.

## Credits

- Archaeological layout based on Roland de Vaux's excavation plans
- Three.js library by mrdoob and contributors
- Penguin sprite: Easter egg contribution

## License

Educational and personal use permitted.

---

*"The settlement sat on a desert plateau, exposed to sun and dust-laden winds."*

