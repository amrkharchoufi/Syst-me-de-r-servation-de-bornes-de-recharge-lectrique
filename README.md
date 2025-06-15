EV Charging Reservation System

A JavaFX + Gradle demo application that simulates electric vehicles sharing a limited number of charging stations. Cars arrive at adjustable intervals, queue if all stations are busy (using a semaphore), charge for a random duration, and then depart—while the UI displays real-time status, statistics, and charts.

🛠️ Features

Configurable simulation

Set total number of cars

Set arrival interval (ms)

Semaphore-based synchronization

Cars wait when all stations are occupied

Stations release upon charging completion

Real-time dashboard

Queue listing (“Voiture #”)

Stations view (green = free, red = occupied)

Live statistics

Average waiting time (ms)

Average service (charging) time (ms)

Total number of cars charged

Pie chart

Breakdown of “En attente / En charge / Terminés”

📦 Prerequisites

Java Development Kit (JDK) 11+

Gradle 7+ (the wrapper is included)

Internet access (to download JavaFX modules via Maven Central)

🚀 Getting Started

Clone the repo

git clone https://github.com/<your-username>/ev-charging-system.git
cd ev-charging-system

Build & run with GradleThis project uses the [org.openjfx.javafxplugin].

./gradlew run

The run task will download JavaFX, compile sources, and launch the app.

Or import into your IDE

Open the project as a Gradle project.

Ensure the org.openjfx.javafxplugin block is present in build.gradle.

Use the Gradle “run” task, or configure your Run Configuration with:

VM options:
  --module-path <your-javafx-sdk>/lib
  --add-modules=javafx.controls,javafx.fxml

🎮 Usage

In the Nb. voitures field, enter how many cars you want to simulate.

In the Intervalle (ms) field, enter the delay (in milliseconds) between car arrivals.

Click Démarrer.

Watch:

The File d’attente list fills as cars arrive.

The station boxes turn red when occupied and show “Voiture #” below each.

Statistics and the Pie Chart update in real time.

📁 Project Structure

ev-charging-system/
├── build.gradle           # Gradle build & JavaFX plugin config
├── settings.gradle        # rootProject.name
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── Main.java
│   │   │   ├── controller/
│   │   │   │   └── SimulationController.java
│   │   │   ├── model/
│   │   │   │   ├── Car.java
│   │   │   │   ├── ChargingStation.java
│   │   │   │   ├── ParkingLot.java
│   │   │   │   └── Statistics.java
│   │   │   └── util/
│   │   │       └── TimerUtil.java
│   │   └── resources/
│   │       └── view/
│   │           └── DashboardView.fxml
└── README.md

🤝 Contributing

Fork the repo

Create a feature branch (git checkout -b feature/YourIdea)

Commit your changes (git commit -m "Add some feature")

Push to your branch (git push origin feature/YourIdea)

Open a Pull Request

Please follow standard Java coding conventions and include unit tests where applicable.

📄 License

This project is released under the MIT License. See LICENSE for details.

👤 Author

Amr Kh / Wiame hamrane

