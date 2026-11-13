<div align="center">
  <img src="assets/banner.svg" width="100%" alt="Hi, I'm Colin. I build backends that survive kill -9, and Linux tools that make 60 Hz screens run at 96.">
  <br><br>
  <a href="https://www.linkedin.com/in/colinkthomas"><img src="https://img.shields.io/badge/LinkedIn-let's_connect-0A66C2?style=for-the-badge" alt="LinkedIn"></a> <a href="https://leetcode.com/u/OKTRBpaERN"><img src="https://img.shields.io/badge/LeetCode-profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode"></a> <img src="https://img.shields.io/badge/open_to-SWE_roles-22C55E?style=for-the-badge" alt="Open to software engineering roles">
</div>

## 👋 About me

I'm a CS student at **VIT Chennai**, and I'm happiest when something is broken in an interesting way. I love finding out *why*: why a broker restart can lose messages it had already acknowledged, why `xrandr` can't add a display mode on Wayland, why meeting notes took a whole minute to appear. Then I build the fix and measure whether it actually worked.

### ✨ Things I get excited about

- 🔪 **Breaking my own systems on purpose.** I test FleetOps by running `kill -9` on the robots, the API and the broker mid-stream, then counting what survived. (Everything did.)
- 🖥️ **Making hardware do more than it says on the box.** My laptop panel was sold as 60 Hz. It runs at 96 Hz now, and that's how [linuxcru](https://github.com/colin-110/linuxcru) started.
- 🗃️ **Simple tech that goes surprisingly far.** One SQLite file gave Meeting Summarizer a job queue, rate limits, a cache and full-text search.
- 🧮 **Replacing guesswork with arithmetic.** If plain code can normalize a number or settle a comparison, it shouldn't cost an LLM call.
- 💸 **Tiny servers.** Two of my live demos run on $5 and $7/month servers, sized from measurements instead of guesses.
- 🤖 **Robots.** Away from backends, I'm tuning ESP32 balancing robots and working out kinematics for a 6-DOF arm.

## 📊 By the numbers

<img src="assets/numbers.svg" width="100%" alt="60 to 96 Hz with linuxcru; 0 readings lost in FleetOps chaos tests; 98% Recall@5 in Lumen; notes 14.8 s after stopping in Meeting Summarizer; 1,000 robots on about 40% of one core; 17 of 20 chart pages without paid vision calls">

## 🚀 Now building: [linuxcru](https://github.com/colin-110/linuxcru)

<table>
<tr>
<td width="52%" valign="top">

My newest project, and it started with my own laptop screen.

Many laptop panels sold as 60 Hz run fine at a higher refresh rate. Windows has CRU for this. On Linux, you have to work out a dozen timing values by hand, build a binary EDID file and edit GRUB.

**linuxcru does all of that from one number.** Type a refresh rate, and it calculates the timings, writes a valid EDID and installs it as a kernel firmware override. It works on Wayland, X11 and with Secure Boot.

- 🪟 A Qt window *and* a CLI, with `--dry-run` for every change
- 🔒 Only a small helper runs as root, and GRUB recovery mode always boots without the override
- 🧪 The installer is tested against a fake filesystem, and the timing math is checked against `cvt` and `edid-decode`

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/Qt_/_PySide6-41CD52?style=flat-square&logo=qt&logoColor=white" alt="Qt / PySide6"> <img src="https://img.shields.io/badge/EDID-F43F5E?style=flat-square" alt="EDID"> <img src="https://img.shields.io/badge/GRUB-6D28D9?style=flat-square&logo=gnu&logoColor=white" alt="GRUB"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux"> <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest">

</td>
<td width="48%" valign="top">
  <img src="https://raw.githubusercontent.com/colin-110/linuxcru/main/docs/images/main-window.png" alt="linuxcru main window with a 96 Hz mode added">
</td>
</tr>
</table>

<img src="assets/terminal.svg" width="100%" alt="linuxcru calc 96 output: 1920x1080 at 95.999 Hz, 227 MHz pixel clock">

## 🛠️ Projects I'm proud of

<table>
<tr>
<td width="50%" valign="top">

### 🤖 [FleetOps](https://github.com/colin-110/robot-fleet-platform)
<a href="https://robot-fleet-platform.vercel.app"><img src="https://raw.githubusercontent.com/colin-110/robot-fleet-platform/main/docs/images/dashboard-overview.png" alt="FleetOps dashboard"></a>

A live map, alarms and commands for a robot fleet. A reading is acknowledged only after it's committed, and every robot keeps an on-disk outbox, so crash tests lose nothing. The robots and the server share a predictor, which cuts messages by 55%.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="MQTT"> <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=flat-square&logo=timescale&logoColor=black" alt="TimescaleDB"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">

**[▶ live demo](https://robot-fleet-platform.vercel.app)**

</td>
<td width="50%" valign="top">

### 💡 [Lumen](https://github.com/colin-110/lumen)
<a href="https://lumen-three-nu.vercel.app"><img src="https://raw.githubusercontent.com/colin-110/lumen/main/docs/screenshot-chat.png" alt="Lumen chat with a cited answer"></a>

Ask questions across your documents and get answers with citations. Hybrid search plus ColBERT reranking takes 25 ms, compared with 1.2 s for a cross-encoder. Every number in an answer is checked against the passage it cites.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" alt="Qdrant"> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis"> <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white" alt="Celery"> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">

**[▶ live demo](https://lumen-three-nu.vercel.app)**

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🎙️ [Meeting Summarizer](https://github.com/colin-110/meeting-summarizer)

Record a meeting and get a transcript, decisions and action items. Instead of Redis and Celery, a SQLite job queue with leases and heartbeats runs every job exactly once across worker processes. Summaries are written *while you're still talking*.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Whisper-10A37F?style=flat-square" alt="Whisper"> <img src="https://img.shields.io/badge/FFmpeg-007808?style=flat-square&logo=ffmpeg&logoColor=white" alt="FFmpeg">

**[▶ live app](https://meeting-summarizer-recorder.vercel.app)**

</td>
<td width="50%" valign="top">

### 🔎 [Fact Knowledge Layer](https://github.com/colin-110/fact-knowledge-layer)

Extracts facts from PDFs, links each one to its page and flags when two reports disagree. Code normalizes currencies and periods, rules settle the clear cases, and only ambiguous pairs go to an LLM. It has 120 tests running in CI.

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Chroma-FF6446?style=flat-square" alt="Chroma"> <img src="https://img.shields.io/badge/PyMuPDF-8B5CF6?style=flat-square" alt="PyMuPDF">

</td>
</tr>
</table>

## 🔧 Away from the server

<table>
<tr>
<td width="34%">⚖️ <a href="https://github.com/colin-110/custom-pid-free-stabilization-robot"><b>PID-free stabilization robot</b></a></td>
<td>A balancing robot on an ESP32, with adaptive control, IMU filtering and dual-core FreeRTOS tasks. <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" alt="ESP32"></td>
</tr>
<tr>
<td>🦾 <a href="https://github.com/colin-110/robot-kinematics-ik-simulator"><b>Robot kinematics simulator</b></a></td>
<td>Forward and inverse kinematics for a 6-DOF arm, with a live 3D view. <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"></td>
</tr>
<tr>
<td>📄 <a href="https://github.com/colin-110/papercut"><b>Papercut</b></a></td>
<td>Converts between images and PDFs entirely in the browser, without uploading files. <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"></td>
</tr>
<tr>
<td>🌊 <a href="https://github.com/colin-110/hab_project_ml"><b>Algal bloom forecasting</b></a></td>
<td>Predicts harmful algal blooms from satellite and climate data. <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/XGBoost-189FDD?style=flat-square" alt="XGBoost"></td>
</tr>
</table>

## 🧰 Toolbox

<p>
<b>Languages</b><br>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"> <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"> <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge" alt="SQL"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
</p>
<p>
<b>Backend & data</b><br>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/REST-0EA5E9?style=for-the-badge" alt="REST"> <img src="https://img.shields.io/badge/WebSockets-4F46E5?style=for-the-badge" alt="WebSockets"> <img src="https://img.shields.io/badge/MQTT-660066?style=for-the-badge&logo=mqtt&logoColor=white" alt="MQTT"> <img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white" alt="Celery"><br>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/TimescaleDB-FDB515?style=for-the-badge&logo=timescale&logoColor=black" alt="TimescaleDB"> <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite"> <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis"> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge&logo=qdrant&logoColor=white" alt="Qdrant">
</p>
<p>
<b>Infra & ops</b><br>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/AWS-FF9900?style=for-the-badge" alt="AWS"> <img src="https://img.shields.io/badge/CloudFormation-E7157B?style=for-the-badge" alt="CloudFormation"> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions"> <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus"> <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana">
</p>
<p>
<b>Retrieval, Linux & hardware</b><br>
<img src="https://img.shields.io/badge/RAG-9333EA?style=for-the-badge" alt="RAG"> <img src="https://img.shields.io/badge/Hybrid_search-DB2777?style=for-the-badge" alt="Hybrid search"> <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux"> <img src="https://img.shields.io/badge/EDID-F43F5E?style=for-the-badge" alt="EDID"> <img src="https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white" alt="ESP32"> <img src="https://img.shields.io/badge/FreeRTOS-2E7D32?style=for-the-badge" alt="FreeRTOS">
</p>

<br>

<a href="https://www.linkedin.com/in/colinkthomas"><img src="assets/footer.svg" width="100%" alt="Thanks for scrolling this far. Come say hi on LinkedIn."></a>
