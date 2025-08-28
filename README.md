# Introduction 📔
BlockAssist is an AI assistant that learns from its user’s actions in Minecraft. The assistant appears in-game with you, starting with only basic knowledge of the game’s commands. As you play, it learns how to assist you in building, learning directly from your actions. It shows an early demo of assistance learning—a new paradigm for aligning agents to human preferences across domains.

---

## 👨🏻‍💻 Genysn BlockAssist Guide 👨🏻‍💻

### Device/System Requirements 💻
- Minimum RAM: 8GB  
- Disk space: 50-100 GB  
- Multi-core CPU  
- **Note:** Won’t work in VPS (CPU-based), GPU required  

**Mac users:** Do not need VcXsrv; just install dependencies. Start command differs slightly.

---

## Pre-Requirements 🛠

### Install dependencies
```bash
sudo apt-get update -y && sudo apt-get install -y \
make build-essential gcc libssl-dev zlib1g-dev libbz2-dev libreadline-dev \
libsqlite3-dev libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev \
libffi-dev liblzma-dev curl git unzip zip mesa-utils x11-apps x11-xserver-utils \
libxi6 libxrender1 libxtst6 libxrandr2 libglu1-mesa libopenal1
