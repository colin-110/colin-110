<img src="assets/banner.svg" width="100%" alt="Colin K Thomas. I build backends that survive kill -9, Linux tools that make 60 Hz screens run at 96, and a boat that clears water hyacinth from ponds.">

<p align="center">
  <a href="https://www.linkedin.com/in/colin-k-thomas"><img src="https://img.shields.io/badge/LinkedIn-colin--k--thomas-0A66C2?style=flat-square" alt="LinkedIn"></a> <img src="https://img.shields.io/badge/Chennai-India-22C55E?style=flat-square" alt="Chennai, India"> <img src="https://img.shields.io/badge/VIT_Chennai-B.Tech_CSE_2027-7C3AED?style=flat-square" alt="VIT Chennai, B.Tech CSE, 2027">
</p>

I'm a computer science student at VIT Chennai. Most of what I write is backend code in Python, and the part I enjoy most is working out what happens when things fail: a broker restarting mid-stream, a worker dying halfway through a job, an API running out of quota. I cause those failures on purpose, fix what breaks and write down what I measured.

<img src="assets/numbers.svg" width="100%" alt="60 to 96 Hz with linuxcru; 30,000 rupees of college funding for the hyacinth boat; 98% Recall@5 in Lumen; notes 14.8 s after stopping in Meeting Summarizer; 0 readings lost in FleetOps chaos tests; 17 of 20 chart pages without paid vision calls">

## Latest project: water hyacinth collection boat

<table>
<tr>
<td width="64%" valign="top">

An autonomous boat that spots floating water hyacinth with a camera and collects it from ponds. **My college funded it with ₹30,000.** It was a team project, and I designed, built and programmed the boat, then tested it in a pond in October 2026.

The code and design stay private while a patent application is prepared.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/Jetson_Orin_Nano-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="Jetson Orin Nano"> <img src="https://img.shields.io/badge/Computer_vision-5C3EE8?style=flat-square" alt="Computer vision">

</td>
<td width="36%" valign="top" align="center">
  <img src="assets/screens/hyacinth-boat-pond.jpg" width="268" alt="The boat on a pond during testing">
  <br><sub>Pond test, October 2026</sub>
</td>
</tr>
</table>

## Currently working on

<table>
<tr>
<td width="52%" valign="top">

### [linuxcru](https://github.com/colin-110/linux-cru)

Windows has CRU for adding custom refresh rates. On Linux, `xrandr` can't add modes on Wayland, and the reliable route, a boot-time EDID override, means working out a dozen timing values by hand, building a binary EDID and editing GRUB.

linuxcru does all of that from one number. It calculates the timings, writes a valid EDID and installs it as a kernel firmware override, on Wayland or X11 and with Secure Boot. Only a small helper runs as root, and every change can be previewed with `--dry-run`.

I built it so anyone can use it. It's open source, installs with pipx and works on Ubuntu, Debian, Linux Mint and other GRUB-based distros.

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/Qt_/_PySide6-41CD52?style=flat-square&logo=qt&logoColor=white" alt="Qt / PySide6"> <img src="https://img.shields.io/badge/EDID-F43F5E?style=flat-square" alt="EDID"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest">

</td>
<td width="48%" valign="middle">
  <img src="https://raw.githubusercontent.com/colin-110/linux-cru/main/docs/images/main-window.png" alt="linuxcru main window with a 96 Hz mode added">
</td>
</tr>
</table>

## Projects

<table>
<tr>
<td width="50%" valign="top">

### [FleetOps](https://github.com/colin-110/robot-fleet-platform)
<sub><a href="https://robot-fleet-platform.vercel.app">Live demo</a> · <a href="https://github.com/colin-110/robot-fleet-platform">Code</a></sub>

<a href="https://robot-fleet-platform.vercel.app"><img src="assets/screens/fleetops.jpg" alt="FleetOps live dashboard with fleet status and robots on the map"></a>

Monitoring and control for a robot fleet. Readings are acknowledged only after they're committed and robots keep an on-disk outbox, so chaos tests that killed the robots, the API or the broker lost nothing. A shared predictor cuts robot messages by 55%.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="MQTT"> <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black" alt="TimescaleDB"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">

</td>
<td width="50%" valign="top">

### [Lumen](https://github.com/colin-110/lumen)
<sub><a href="https://lumen-three-nu.vercel.app">Live demo</a> · <a href="https://github.com/colin-110/lumen">Code</a></sub>

<a href="https://lumen-three-nu.vercel.app"><img src="assets/screens/lumen.jpg" alt="Lumen comparing an invoice with a services agreement, with citations"></a>

A self-hosted document assistant that answers with citations. Hybrid search with ColBERT reranking takes 25 ms where a cross-encoder took 1.2 s, and numbers in each answer are checked against the passages they cite.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" alt="Qdrant"> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white" alt="Celery"> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer)
<sub><a href="https://meeting-summarizer-recorder.vercel.app">Live app</a> · <a href="https://github.com/colin-110/meeting-summarizer">Code</a></sub>

<a href="https://meeting-summarizer-recorder.vercel.app"><img src="assets/screens/meeting-summarizer.jpg" alt="Meeting Summarizer upload and record page"></a>

Turns a recording into a transcript, a summary, decisions and action items. Jobs run exactly once on a SQLite queue with leases and heartbeats instead of Redis and Celery, and long meetings are summarized while they're still being recorded.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Whisper-10A37F?style=flat-square" alt="Whisper"> <img src="https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white" alt="FFmpeg">

</td>
<td width="50%" valign="top">

### [Papercut](https://github.com/colin-110/papercut)
<sub><a href="https://colin-110-papercut.vercel.app">Live app</a> · <a href="https://github.com/colin-110/papercut">Code</a></sub>

<a href="https://colin-110-papercut.vercel.app"><img src="assets/screens/papercut.jpg" alt="Papercut photo to PDF converter"></a>

I built this for friends who aren't technical and needed to turn photos into PDFs, and they still use it. Everything runs in the browser with PDF.js, pdf-lib and Canvas, so files never leave the device.

<img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"> <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite"> <img src="https://img.shields.io/badge/PDF.js-F43F5E?style=flat-square" alt="PDF.js">

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### [Fact Knowledge Layer](https://github.com/colin-110/fact-knowledge-layer)
<sub><a href="https://drive.google.com/file/d/11Ns9VgLIaBC0U2QHDBuwt0iK0OEf-YCN/view?usp=drive_link">Demo video</a> · <a href="https://github.com/colin-110/fact-knowledge-layer">Code</a></sub>

<a href="https://drive.google.com/file/d/11Ns9VgLIaBC0U2QHDBuwt0iK0OEf-YCN/view?usp=drive_link"><img src="assets/screens/fkl-relationships.jpg" width="49%" alt="Relationships tab: facts from an earnings presentation flagged as likely contradictions, each linked to its source page"></a> <a href="https://drive.google.com/file/d/11Ns9VgLIaBC0U2QHDBuwt0iK0OEf-YCN/view?usp=drive_link"><img src="assets/screens/fkl-ask.jpg" width="49%" alt="Ask tab: an answer about FY24 revenue with the facts it used"></a>

Extracts facts from PDFs, links each one to the page it came from and flags when two reports disagree. Plain code normalizes currencies and periods, rules settle the clear cases, and only the ambiguous pairs go to an LLM.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Chroma-FF6446?style=flat-square" alt="Chroma"> <img src="https://img.shields.io/badge/PyMuPDF-8B5CF6?style=flat-square" alt="PyMuPDF">

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### [Self-levelling platform on a line-following robot](https://github.com/colin-110/esp32-self-levelling-platform)

A line-following robot with a servo-mounted platform on top that stays level while it drives. The ESP32 runs line following on one core and levelling on the other.

Instead of PID, I wrote a controller that steps the servo towards level in small, bounded steps. Getting it stable on the real hardware took a lot of tuning: a four-stage filter on the tilt signal, a cap on each step and a check that stops correcting once the angle settles. I also built a [PID version](https://github.com/colin-110/mpu6050-servo-pid-controller) to compare. PID corrected faster, but my controller held the platform level too.

<img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/FreeRTOS-2E7D32?style=flat-square" alt="FreeRTOS"> <img src="https://img.shields.io/badge/MPU6500-6D28D9?style=flat-square" alt="MPU6500">

</td>
</tr>
</table>

## Other things I've built

<table>
<tr>
<td width="45%" valign="top">

**[NeetCode and LeetCode sync checker](https://github.com/colin-110/neetcode_leetcode_syncer)**

A Chrome extension that highlights problems I've ticked off on NeetCode but never actually solved on LeetCode. I use it most days when I practise.

<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"> <img src="https://img.shields.io/badge/Chrome_extension-4285F4?style=flat-square&logo=googlechrome&logoColor=white" alt="Chrome extension">

</td>
<td width="55%" valign="middle">
  <img src="assets/screens/neetcode-sync-checker.png" alt="A NeetCode problem ticked as solved but with no accepted LeetCode submission, highlighted in red">
</td>
</tr>
</table>

- [Robot kinematics simulator](https://github.com/colin-110/robot-kinematics-ik-simulator): forward and inverse kinematics for a 6-DOF arm, with a live 3D view
- [Algal bloom forecasting](https://github.com/colin-110/hab_project_ml): an XGBoost model that predicts harmful algal blooms from satellite and climate data

## Tools

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square" alt="SQL"> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="MQTT"> <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white" alt="Celery"><br>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black" alt="TimescaleDB"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis"> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" alt="Qdrant"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js"><br>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square" alt="AWS"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"> <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus"> <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/FreeRTOS-2E7D32?style=flat-square" alt="FreeRTOS">
