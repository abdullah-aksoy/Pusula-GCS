<div align="center">
  <img src="./Readme Images/icon.png" alt="Pusula Logo" width="100">
  <h1>Pusula Ground Control Station (GCS)</h1>
</div>

## 📋 Overview

Pusula Ground Control Interface (GCS) is a custom-built software that enables real-time communication with our unmanned surface vehicle (USV). Through telemetry, it allows us to both send commands and receive live data from the Pixhawk Cube Orange Plus flight controller. The interface displays real-time system information and vehicle status, including location, orientation, and sensor data. With integrated mapping functionality, users can monitor the vehicle’s live position and visualize assigned waypoints on the map, ensuring better mission awareness and control.

## 🛠️ Technical Stack

### Backend

<div>
  <img src="https://skillicons.dev/icons?i=python" alt="Python" title="Python" />
  <img src="https://skillicons.dev/icons?i=flask" alt="Flask" title="Flask" />
  <img src="https://skillicons.dev/icons?i=fastapi" alt="FastAPI" title="FastAPI" />
  <img src="https://skillicons.dev/icons?i=docker" alt="Docker" title="Docker" />
</div>

### Frontend

<div>
  <img src="https://skillicons.dev/icons?i=javascript" alt="JavaScript" title="JavaScript" />
  <img src="https://skillicons.dev/icons?i=html" alt="HTML5" title="HTML5" />
  <img src="https://skillicons.dev/icons?i=css" alt="CSS3" title="CSS3" />
  <img src="https://skillicons.dev/icons?i=leaflet" alt="Leaflet" title="Leaflet.js" />
</div>

## 🖥️ Core Features

- **Real-time Telemetry** - Monitor vehicle status, GPS, battery, and sensor data
- **Mission Planning** - Create and manage waypoint-based missions
- **Command Interface** - Direct control and command input
- **Map Integration** - Real-time vehicle tracking on interactive maps
- **Data Logging** - Record and analyze mission data
- **Multi-vehicle Support** - Control multiple USVs from a single interface

## 🖼️ Visual

<div align="center">
  <img src="./Readme Images/real_life_example_1.png" alt="Dashboard Preview" width="90%">
  <p><em>Figure 1: Pusula GCS Dashboard Interface</em></p>
  
  <img src="./Readme Images/adding_waypoints_dashboard.png" alt="Waypoint Management" width="90%">
  <p><em>Figure 2: Waypoint Management Interface</em></p>
  
  <img src="./Readme Images/points_added_dashboard.png" alt="Mission Planning" width="90%">
  <p><em>Figure 3: Mission Planning with Multiple Waypoints</em></p>
</div>

## 👥 Developers

- [Ali Haydar Sucu](https://github.com/alihaydarsucu)
- [Abdullah Aksoy](https://github.com/abdullah-aksoy)

## Features

### Dashboard Features

- 🎛️ **Real-time USV monitoring** - ARM status, flight mode, GPS, battery, failsafes
- 🗺️ **Interactive map** with vehicle position and waypoint management
- 🎯 **Button-based control interface** - Direct command execution via intuitive buttons
- 🎨 **Color detection display** - Shows "Renk Bekleniyor" for İHA color detection
- 📊 **System status panels** with telemetry data
- 🚀 **Mission control** - Start/stop algorithms, mode switching

### YKI Integration

- ✅ **Button-to-command mapping** - Dashboard buttons mapped to YKI macros via yki_server.py
- 🔄 **Status polling** - Regular telemetry updates from YKI backend
- 📡 **Serial communication** - Direct interface with Pixhawk via YKI
- 🛡️ **Error handling** - Graceful handling of connection issues
- 🎯 **Streamlined UX** - Terminal interface removed per Teknofest Aselsan jury feedback

## Usage

### Control Interface

The dashboard provides intuitive button-based controls that communicate with the backend yki_server.py to execute commands. This streamlined interface was implemented following Teknofest Aselsan jury feedback for improved user experience.

**Available Controls:**

- **ARM/DISARM buttons** - Vehicle arming controls with safety confirmation
- **Mode selection** - Manual/Guided mode switching via dropdown
- **Mission controls** - Algorithm start/stop buttons
- **Navigation controls** - Waypoint-based navigation through map interface

**Backend Commands (executed via yki_server.py):**

**Basic Commands:**

- `STATUS` - Get telemetry data
- `ARM` / `ARM MANUAL` - Arm the vehicle safely
- `DISARM` - Disarm the vehicle
- `MODE MANUAL` - Switch to manual mode
- `MODE GUIDED` - Switch to guided mode

**Algorithm Commands:**

- `ALGO BASLA` - Start algorithm/mission
- `ALGO DUR` - Stop algorithm/mission
- `ALGO HAREKETLEN` - Algorithm movement command

**Navigation Commands:**

- `GOTO lat lon alt` - Navigate to coordinates
- `RC TEST` - Test RC channels
- `MOTOR_TEST` - Test motors

### Waypoint Management

1. Click on map to add waypoints
2. Use "Gönder" button to upload waypoints to YKI
3. Waypoints are converted to `GOTO` commands automatically

### Color Detection

The "Renk Bekleniyor" section is preserved for future İHA color detection integration. When implemented, it will display:

- Detected color (Kırmızı/Yeşil/Siyah)
- Color code
- Real-time updates

## Competition Requirements

This integration supports the İnsansız Deniz Aracı (USV) competition requirements:

- ✅ **YKI (Ground Control Station)** - Web-based dashboard with button controls
- ✅ **Control Interface** - Intuitive button-based command execution
- ✅ **Telemetry Display** - Real-time status monitoring
- ✅ **Mission Control** - Algorithm start/stop functionality
- ✅ **Navigation** - Waypoint management and GPS display
- ✅ **Safety Features** - ARM/DISARM controls and failsafe monitoring
- ✅ **Color Detection Ready** - UI prepared for İHA integration
- ✅ **Jury Compliance** - Interface optimized per Teknofest Aselsan feedback

## License

This project integrates with the existing YKI system and maintains compatibility with the original architecture while providing a modern web interface for USV control and monitoring.
