# WinHardwarePoller
Modular hardware monitoring application for Windows

## Features 

### Service
- Continuous hardware monitoring
- Configurable polling interval per system/resource constraints
- Modular sensor providers for different hardware components
- Data normalization into unified format(s)
- In-memory buffering of sensor readings for efficient processing
- Batched persistence of telemetry data to a local database
- Session tracking from application start to shutdown
- Automatic session finalization and cleanup on shutdown events
- Lightweight processing for basic aggregation (min/max/avg)
- Rule-based alerting for configurable threshold violations and anomalies
- Background orchestration of polling, processing, and storage pipelines
- Configurable monitoring profile (enabled sensors, intervals, retention)

## UI
- Overview dashboard for current and historical system sessions
- Session browser with date & duration filter
- Per-component breakdown of hardware metrics over time
- Graphical visualization of time-series sensor data
- Comparison view between multiple sessions
- Access to automatically generated shutdown reports
- Export and view reports in multiple formats (JSON, HTML, PDF)
- Configuration interface for monitoring settings and sensor selection
- Real-time notification display for alerts and threshold breaches

## Project Structure

```
app
├── telemetry
│   ├── providers        # Sensors
│   ├── polling         # scheduling + polling engine
│   └── models          # raw sensor data structs
│
├── processing
│   ├── rules           # rules for notifications/alerts
│   ├── aggregation     # averages, trends
│   └── analysis        # "CPU hotter than baseline"
│
├── storage
│   ├── database
│   ├── repositories
│   └── migrations
│
├── reporting
│   ├── generators
│   ├── formats        # pdf/json/html
│   └── sessions       # session reports
│
├── application
│   ├── service         # orchestration layer
│   ├── scheduler
│   └── config
│
├── presentation
│   ├── ui
│   ├── viewmodels
│   └── notifications
│
└── shared
    ├── logging
    ├── extensions
    └── primitives
```
