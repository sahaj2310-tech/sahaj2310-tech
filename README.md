<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d0f10,50:1c2022,100:FF4E17&height=170&section=header&text=Sahaj%20Sinha&fontSize=54&fontColor=EDE8E1&animation=fadeIn&fontAlignY=36&desc=AI%20and%20Big%20Data%20%C2%B7%20Woosong%20University%2C%20Daejeon&descAlignY=58&descSize=16" width="100%" alt="Sahaj Sinha" />

<a href="https://sahaj-sinha.netlify.app">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=20&duration=3200&pause=900&color=FF4E17&center=true&vCenter=true&width=760&height=42&lines=Turning+sensor+noise+into+a+map+a+machine+can+act+on;Pose+estimation+%26+computer+vision+at+the+Woosong+AI+Lab;SLAM+%C2%B7+Robotics+%C2%B7+Real-time+systems+%C2%B7+Applied+AI" alt="What I work on" />
</a>

[![Portfolio](https://img.shields.io/badge/Portfolio-FF4E17?style=flat-square&logoColor=white)](https://sahaj-sinha.netlify.app)
[![CV](https://img.shields.io/badge/CV-1c2022?style=flat-square)](https://sahaj-sinha.netlify.app/cv)
[![Email](https://img.shields.io/badge/Email-1c2022?style=flat-square&logo=gmail&logoColor=white)](mailto:sahajsinha2310@gmail.com)

</div>

---

### Currently

Researcher at the **Woosong University AI Lab** — working on **pose estimation and computer vision**, alongside autonomous robotic platforms and model training. Co-authoring papers with faculty for IEEE submission.

Holding a 100% merit scholarship and full GPA across four consecutive semesters, and serving as a Global Peer Leader.

---

### Selected work

| Project | What it does | Stack |
| :--- | :--- | :--- |
| **[AETHER-SLAM](https://github.com/sahaj2310-tech/AETHER-SLAM)** | Live dense 3D room scanning from a single webcam — monocular visual SLAM, neural depth, TSDF fusion, streamed to a browser. No LiDAR. | Python · PyTorch · Open3D · MiDaS · CUDA |
| **[TerraVanguard](https://github.com/sahaj2310-tech/TerraVanguard)** | Autonomous terrain rover: differential drive, triple-ultrasonic avoidance, gyro-stabilised camera gimbal, live MJPEG — all on one MCU. | ESP32-S3 · C++ · MPU9250 |
| **[WatchCore RTOS](https://github.com/sahaj2310-tech/WatchCore-RT-OS)** | Fault-tolerant FreeRTOS supervisor for a simulated 4-spacecraft constellation, with anomaly detection and autonomous recovery. | FreeRTOS · C · TypeScript · SQLite |
| **[AeroSense](https://github.com/sahaj2310-tech/AeroSense)** | Real-time air quality monitoring and forecasting — 13 sensing channels, XGBoost classification plus LSTM forecasting. | ESP32 · Python · XGBoost · TensorFlow |
| **[UniMate](https://github.com/sahaj2310-tech/UniMate)** | University assistant that refuses to guess: source-grounded RAG with citations, 14 languages, injection guards. | FastAPI · pgvector · Ollama · React |
| **[Voice AI Assistant](https://github.com/sahaj2310-tech/Voice-AI-Assistant)** | Self-hosted Korean voice front desk — Whisper STT, local LLM over RAG, edge-tts, Twilio phone integration. | Whisper · Ollama · FastAPI · Twilio |
| **[Glassly](https://github.com/sahaj2310-tech/Glassly-AI)** | On-device AI skin analysis. Real-time facial landmarking, nothing leaves the phone. → [www.glasslyai.com](https://www.glasslyai.com/) | MediaPipe · TensorFlow.js · Capacitor |
| **[ClarityDeck](https://github.com/sahaj2310-tech/claritydeck)** | Turns messy input into a structured, shareable card using a local LLM. No cloud, no rate limits. | Next.js · FastAPI · Ollama |

Also building an **AI-based reconnaissance rover** — stereo VSLAM and custom YOLO detection on a Raspberry Pi 5 with an AI accelerator. Field hardware, no public repo.

---

### How the work fits together

Everything below runs the same loop: raw sensor data in, a usable understanding of the world out, then something acts on it.

```mermaid
flowchart LR
    S["📷 Sensors<br/>camera · IMU · ultrasonic · gas"] --> P

    subgraph P["Perception"]
        direction TB
        CV["Computer Vision<br/><i>features · landmarks · detection</i>"]
        DEPTH["Depth &amp; Geometry<br/><i>MiDaS · stereo · TSDF</i>"]
        CV --> DEPTH
    end

    P --> M

    subgraph M["Understanding"]
        direction TB
        SLAM["SLAM<br/><i>pose graph · loop closure</i>"]
        SEM["Semantics<br/><i>what the thing is</i>"]
        SLAM --> SEM
    end

    M --> A

    subgraph A["Action"]
        direction TB
        PLAN["Planning<br/><i>occupancy · paths</i>"]
        CTRL["Control<br/><i>drive · gimbal · recovery</i>"]
        PLAN --> CTRL
    end

    A --> OUT["🤖 A system that moves,<br/>reports, or answers"]

    style S fill:#0d0f10,stroke:#FF4E17,color:#EDE8E1
    style OUT fill:#0d0f10,stroke:#FF4E17,color:#EDE8E1
    style P fill:transparent,stroke:#8b9195
    style M fill:transparent,stroke:#8b9195
    style A fill:transparent,stroke:#8b9195
```

AETHER-SLAM is the whole loop in one system. TerraVanguard and the recon rover are the loop on hardware that has to survive contact with the ground. WatchCore is the loop when failure is the interesting case.

---

### By the numbers

| | |
| :-- | :-- |
| **9** | shipped projects, from monocular SLAM to a self-hosted voice agent |
| **1** | peer-reviewed paper, first author, in *Sensors* (MDPI) |
| **10** | verified credentials — Microsoft, AWS, PAMS, Korea University |
| **4** | consecutive semesters at full GPA, on a 100% merit scholarship |
| **3** | languages: English and Hindi fluent, Korean to Level 3 |

---

<details>
<summary><b>What I am reaching for next</b></summary>

<br/>

- **Pose estimation that survives the real world** — occlusion, motion blur, and the moments a tracker normally gives up.
- **Perception that runs where the sensors are.** Cloud inference is a latency budget nobody actually has on a moving robot.
- **Systems that admit uncertainty.** UniMate refuses to answer when its sources do not cover the question; I want that instinct everywhere.
- **More papers.** Further work with faculty is in preparation for IEEE venues.

</details>

<details>
<summary><b>Hardware I have actually put in the field</b></summary>

<br/>

| Platform | Compute | Sensing |
| :--- | :--- | :--- |
| Recon Rover | Raspberry Pi 5 (16 GB) + AI HAT accelerator | ORB stereo camera |
| TerraVanguard | ESP32-S3 | MPU9250 IMU · 3× HC-SR04 · DHT11 · camera |
| AeroSense | ESP32 | MQ-135 · DHT22 · PM sensing, 13 channels |

</details>
---

### Published

> **Sinha, S.**, Lee, S., & Singh, S. (2026). *Survey on Reconnaissance Autonomous Robotic Systems for Disaster Management.* **Sensors** (MDPI), 26(5), 1659.
>
> [![DOI](https://img.shields.io/badge/DOI-10.3390%2Fs26051659-FF4E17?style=flat-square)](https://doi.org/10.3390/s26051659) [![Read](https://img.shields.io/badge/Read%20on%20MDPI-1c2022?style=flat-square)](https://www.mdpi.com/1424-8220/26/5/1659)

Further papers in preparation with faculty, for IEEE journals and other venues.

---

### Stack

<details open>
<summary><b>Languages</b></summary>

<br/>

![Python](https://img.shields.io/badge/Python-1c2022?style=flat-square&logo=python&logoColor=FF4E17)
![C++](https://img.shields.io/badge/C%2FC%2B%2B-1c2022?style=flat-square&logo=cplusplus&logoColor=FF4E17)
![TypeScript](https://img.shields.io/badge/TypeScript-1c2022?style=flat-square&logo=typescript&logoColor=FF4E17)
![SQL](https://img.shields.io/badge/SQL-1c2022?style=flat-square&logo=postgresql&logoColor=FF4E17)
![R](https://img.shields.io/badge/R-1c2022?style=flat-square&logo=r&logoColor=FF4E17)
![Java](https://img.shields.io/badge/Java-1c2022?style=flat-square&logo=openjdk&logoColor=FF4E17)

</details>

<details>
<summary><b>Perception &amp; learning</b></summary>

<br/>

![PyTorch](https://img.shields.io/badge/PyTorch-1c2022?style=flat-square&logo=pytorch&logoColor=FF4E17)
![TensorFlow](https://img.shields.io/badge/TensorFlow-1c2022?style=flat-square&logo=tensorflow&logoColor=FF4E17)
![OpenCV](https://img.shields.io/badge/OpenCV-1c2022?style=flat-square&logo=opencv&logoColor=FF4E17)
![Open3D](https://img.shields.io/badge/Open3D-1c2022?style=flat-square)
![CUDA](https://img.shields.io/badge/CUDA-1c2022?style=flat-square&logo=nvidia&logoColor=FF4E17)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1c2022?style=flat-square&logo=scikitlearn&logoColor=FF4E17)

</details>

<details>
<summary><b>Embedded &amp; systems</b></summary>

<br/>

![FreeRTOS](https://img.shields.io/badge/FreeRTOS-1c2022?style=flat-square&logo=freertos&logoColor=FF4E17)
![ESP32](https://img.shields.io/badge/ESP32-1c2022?style=flat-square&logo=espressif&logoColor=FF4E17)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-1c2022?style=flat-square&logo=raspberrypi&logoColor=FF4E17)
![ROS](https://img.shields.io/badge/ROS%2FROS2-1c2022?style=flat-square&logo=ros&logoColor=FF4E17)
![Arduino](https://img.shields.io/badge/Arduino-1c2022?style=flat-square&logo=arduino&logoColor=FF4E17)
![Docker](https://img.shields.io/badge/Docker-1c2022?style=flat-square&logo=docker&logoColor=FF4E17)

</details>

<details>
<summary><b>Interfaces &amp; services</b></summary>

<br/>

![React](https://img.shields.io/badge/React-1c2022?style=flat-square&logo=react&logoColor=FF4E17)
![Next.js](https://img.shields.io/badge/Next.js-1c2022?style=flat-square&logo=nextdotjs&logoColor=FF4E17)
![FastAPI](https://img.shields.io/badge/FastAPI-1c2022?style=flat-square&logo=fastapi&logoColor=FF4E17)
![Node.js](https://img.shields.io/badge/Node.js-1c2022?style=flat-square&logo=nodedotjs&logoColor=FF4E17)
![Three.js](https://img.shields.io/badge/Three.js-1c2022?style=flat-square&logo=threedotjs&logoColor=FF4E17)
![Tailwind](https://img.shields.io/badge/Tailwind-1c2022?style=flat-square&logo=tailwindcss&logoColor=FF4E17)

</details>

---

### Certified

`DP-900` Azure Data Fundamentals · `AI-900` Azure AI Fundamentals · `CLF-C02` AWS Cloud Practitioner · Korean Language Level 3, Korea University

---

<div align="center">

### Pinned work

<a href="https://github.com/sahaj2310-tech/AETHER-SLAM">
  <img width="49%" src="https://github-readme-stats.shion.dev/api/pin/?username=sahaj2310-tech&repo=AETHER-SLAM&theme=dark&hide_border=true&bg_color=0d0f10&title_color=FF4E17&text_color=8b9195&icon_color=FF4E17" alt="AETHER-SLAM" />
</a>
<a href="https://github.com/sahaj2310-tech/WatchCore-RT-OS">
  <img width="49%" src="https://github-readme-stats.shion.dev/api/pin/?username=sahaj2310-tech&repo=WatchCore-RT-OS&theme=dark&hide_border=true&bg_color=0d0f10&title_color=FF4E17&text_color=8b9195&icon_color=FF4E17" alt="WatchCore RTOS" />
</a>
<a href="https://github.com/sahaj2310-tech/TerraVanguard">
  <img width="49%" src="https://github-readme-stats.shion.dev/api/pin/?username=sahaj2310-tech&repo=TerraVanguard&theme=dark&hide_border=true&bg_color=0d0f10&title_color=FF4E17&text_color=8b9195&icon_color=FF4E17" alt="TerraVanguard" />
</a>
<a href="https://github.com/sahaj2310-tech/UniMate">
  <img width="49%" src="https://github-readme-stats.shion.dev/api/pin/?username=sahaj2310-tech&repo=UniMate&theme=dark&hide_border=true&bg_color=0d0f10&title_color=FF4E17&text_color=8b9195&icon_color=FF4E17" alt="UniMate" />
</a>

<br/><br/>

### Contribution graph, eaten

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/sahaj2310-tech/sahaj2310-tech/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/sahaj2310-tech/sahaj2310-tech/output/github-snake.svg" />
  <img alt="Snake eating my contribution graph" src="https://raw.githubusercontent.com/sahaj2310-tech/sahaj2310-tech/output/github-snake.svg" width="100%" />
</picture>

<br/>


![Stats](https://github-readme-stats.shion.dev/api?username=sahaj2310-tech&theme=dark&hide_border=true&hide_title=true&icon_color=FF4E17&text_color=8b9195&bg_color=0d0f10)
![Languages](https://github-readme-stats.shion.dev/api/top-langs/?username=sahaj2310-tech&theme=dark&hide_border=true&layout=compact&text_color=8b9195&bg_color=0d0f10&title_color=FF4E17)

<br/>

![Streak](https://streak-stats.demolab.com?user=sahaj2310-tech&theme=dark&hide_border=true&background=0d0f10&stroke=1c2022&ring=FF4E17&fire=FF4E17&currStreakLabel=8b9195&sideLabels=8b9195&dates=565d61)

<br/>


---

**[sahaj-sinha.netlify.app](https://sahaj-sinha.netlify.app)** · Daejeon, South Korea

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF4E17,50:1c2022,100:0d0f10&height=90&section=footer" width="100%" alt="" />

</div>
