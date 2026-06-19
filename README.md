# WinHardwarePoller
Modular hardware monitoring application for Windows

## Features

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