<img src="assets/banner.svg" width="100%" alt="Colin K Thomas. I build backends that survive kill -9, and Linux tools that make 60 Hz screens run at 96.">

<p align="center">
  <a href="https://www.linkedin.com/in/colin-k-thomas"><img src="https://img.shields.io/badge/LinkedIn-colin--k--thomas-0A66C2?style=flat-square" alt="LinkedIn"></a> <img src="https://img.shields.io/badge/Chennai-India-22C55E?style=flat-square" alt="Chennai, India">
</p>

I'm a computer science student at VIT Chennai. Most of what I write is backend code in Python, and the part I enjoy most is working out what happens when things fail: a broker restarting mid-stream, a worker dying halfway through a job, an API running out of quota. I like to cause those failures on purpose and write down what I measured.

Outside backend work, I've built [linuxcru](https://github.com/colin-110/linux-cru), which started because my laptop's panel is sold as 60 Hz but runs fine at 96, and an autonomous boat for clearing water hyacinth from ponds, which my college funded with ₹30,000.

<img src="assets/numbers.svg" width="100%" alt="60 to 96 Hz with linuxcru; 30,000 rupees of college funding for the hyacinth boat; 98% Recall@5 in Lumen; notes 14.8 s after stopping in Meeting Summarizer; 0 readings lost in FleetOps chaos tests; 17 of 20 chart pages without paid vision calls">

## Latest project: water hyacinth collection boat

<table>
<tr>
<td width="70%" valign="top">

An autonomous boat that detects floating water hyacinth with a camera and collects it from ponds. It was a college-funded team project (₹30,000), and I designed, built, programmed and tested it in a pond in October 2026.

A patent application is being prepared, so the code and design aren't public yet.

<img src="https://img.shields.io/badge/College_funded-%E2%82%B930%2C000-D97706?style=flat-square" alt="College funded: 30,000 rupees"> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/Jetson_Orin_Nano-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="Jetson Orin Nano"> <img src="https://img.shields.io/badge/Computer_vision-5C3EE8?style=flat-square" alt="Computer vision">

</td>
<td width="30%" valign="top" align="center">
  <img src="assets/screens/hyacinth-boat-pond.jpg" width="200" alt="The boat on a pond during testing">
  <br><sub>Pond test, October 2026</sub>
</td>
</tr>
</table>

## Currently working on

<table>
<tr>
<td width="52%" valign="top">

### [linuxcru](https://github.com/colin-110/linux-cru)

Windows has CRU for adding custom refresh rates. On Linux, `xrandr` can't add modes on Wayland, and the reliable route, a boot-time EDID override, means working out a dozen timing values by hand, building a binary EDID file and editing GRUB.

linuxcru does that from one number. You type a refresh rate, and it calculates the timings, writes a valid EDID and installs it as a kernel firmware override. It works on Wayland, X11 and with Secure Boot, and every change can be previewed with `--dry-run`.

Only a small helper runs as root, and the installer is tested against a fake filesystem, so the tests never touch a real boot setup.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/Qt_/_PySide6-41CD52?style=flat-square&logo=qt&logoColor=white" alt="Qt / PySide6"> <img src="https://img.shields.io/badge/EDID-F43F5E?style=flat-square" alt="EDID"> <img src="https://img.shields.io/badge/GRUB-6D28D9?style=flat-square&logo=gnu&logoColor=white" alt="GRUB"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest">

</td>
<td width="48%" valign="top">
  <img src="https://raw.githubusercontent.com/colin-110/linux-cru/main/docs/images/main-window.png" alt="linuxcru main window with a 96 Hz mode added">
</td>
</tr>
</table>

<img src="assets/terminal.svg" width="100%" alt="linuxcru calc 96 output: 1920x1080 at 95.999 Hz, 227 MHz pixel clock">

## Projects

<table>
<tr>
<td width="50%" valign="top">

### [FleetOps](https://github.com/colin-110/robot-fleet-platform)
<a href="https://robot-fleet-platform.vercel.app"><img src="assets/screens/fleetops.jpg" alt="FleetOps live dashboard with 20 robots on the map"></a>

Monitoring and control for a robot fleet: a live map, alarms and commands. Readings are acknowledged only after they're committed, and each robot keeps an on-disk outbox until the server confirms. The robots and the server run the same predictor, so robots send 55% fewer messages.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="MQTT"> <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black" alt="TimescaleDB"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">

[Live demo](https://robot-fleet-platform.vercel.app)

</td>
<td width="50%" valign="top">

### [Lumen](https://github.com/colin-110/lumen)
<a href="https://lumen-three-nu.vercel.app"><img src="assets/screens/lumen.jpg" alt="Lumen comparing an invoice with a services agreement, with citations"></a>

A self-hosted document assistant that answers with citations. It uses hybrid search with ColBERT reranking, which takes 25 ms where a cross-encoder took 1.2 s. Numbers in each answer are checked against the passages they cite.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" alt="Qdrant"> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis"> <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white" alt="Celery"> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">

[Live demo](https://lumen-three-nu.vercel.app)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer)
<a href="https://meeting-summarizer-recorder.vercel.app"><img src="assets/screens/meeting-summarizer.jpg" alt="Meeting Summarizer upload and record page"></a>

Turns a meeting recording into a transcript, a summary, decisions and action items. Jobs run on a SQLite queue with leases and heartbeats instead of Redis and Celery, and each one runs exactly once across worker processes. Long meetings are summarized while the recording is still going.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Whisper-10A37F?style=flat-square" alt="Whisper"> <img src="https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white" alt="FFmpeg">

[Live app](https://meeting-summarizer-recorder.vercel.app)

</td>
<td width="50%" valign="top">

### [Papercut](https://github.com/colin-110/papercut)
<a href="https://colin-110-papercut.vercel.app"><img src="assets/screens/papercut.jpg" alt="Papercut photo to PDF converter"></a>

I built this for friends who aren't technical and needed to turn photos into PDFs, and they still use it. It converts photos to PDFs and PDFs to images entirely in the browser. There's no upload API or processing backend: files are read and converted locally with PDF.js, pdf-lib and Canvas, then downloaded straight from the tab.

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite"> <img src="https://img.shields.io/badge/PDF.js-F43F5E?style=flat-square" alt="PDF.js">

[Live app](https://colin-110-papercut.vercel.app)

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### [Fact Knowledge Layer](https://github.com/colin-110/fact-knowledge-layer)

Extracts facts from PDFs, links each one to the page it came from and flags when two reports disagree. Plain code normalizes currencies and periods, rules settle the clear cases, and only ambiguous pairs go to an LLM.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Chroma-FF6446?style=flat-square" alt="Chroma"> <img src="https://img.shields.io/badge/PyMuPDF-8B5CF6?style=flat-square" alt="PyMuPDF">

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### [Self-levelling platform on a line-following robot](https://github.com/colin-110/esp32-self-levelling-platform)

A line-following robot with a servo-mounted platform on top that stays level while it drives, with the ESP32 running each job on its own core.

Instead of using PID, I wrote my own controller that steps the servo towards level in small, bounded steps, and then spent a lot of time tuning it on the real hardware. It took a four-stage filter on the tilt signal, a cap on each servo step and a check that stops correcting once the angle settles before the platform stopped hunting back and forth. I also built a [PID version](https://github.com/colin-110/mpu6050-servo-pid-controller) to compare. PID corrected faster, but my controller held the platform level too.

<img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/FreeRTOS-2E7D32?style=flat-square" alt="FreeRTOS"> <img src="https://img.shields.io/badge/MPU6500-6D28D9?style=flat-square" alt="MPU6500">

</td>
</tr>
</table>

## Other things I've built

- [Robot kinematics simulator](https://github.com/colin-110/robot-kinematics-ik-simulator): forward and inverse kinematics for a 6-DOF arm, with a live 3D view
- [Algal bloom forecasting](https://github.com/colin-110/hab_project_ml): an XGBoost model that predicts harmful algal blooms from satellite and climate data

## Tools

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java"> <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square" alt="SQL"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="MQTT"> <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white" alt="Celery">
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black" alt="TimescaleDB"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis"> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" alt="Qdrant"> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square" alt="AWS"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions">
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus"> <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/FreeRTOS-2E7D32?style=flat-square" alt="FreeRTOS">

---

I'm looking for a software engineering internship. The easiest way to reach me is [LinkedIn](https://www.linkedin.com/in/colin-k-thomas).
