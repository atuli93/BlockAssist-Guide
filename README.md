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
Install Node.js
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt update
sudo apt install -y nodejs
node -v

Install NVIDIA Game Ready Driver (IMPORTANT)

Go to the NVIDIA Driver Download
.

Select your GPU, Windows version → Find.

Click View & Download → Install.

Restart your PC.

Install VcXsrv Windows X Server

Download and run VcXsrv
.

Open XLaunch:

Check Multiple windows

Check Start no client

Check Disable access control

Finish setup → runs in background.

❗ Open XLaunch every time before playing.

Set DISPLAY and Audio in ~/.bashrc
echo -e '\n# WSL2 VcXsrv display setup\nexport DISPLAY=$(ip route | grep -m1 default | awk "{print $3}"):0.0\nexport LIBGL_ALWAYS_INDIRECT=0\nexport LIBGL_DEBUG=verbose' >> ~/.bashrc
source ~/.bashrc

Test VcXsrv
xeyes


If a new tab pops up with eyes, VcXsrv is set up correctly.

Get Hugging Face API token

Sign up at Hugging Face
 and verify your email.

Generate a new access token:

Click profile → Access Tokens → New Token

Name: BlockAssist

Role: Write → Create → Copy token

Clone & move to blockassist Repo
git clone https://github.com/gensyn-ai/blockassist.git
cd blockassist

Install Java 1.8.0_152
./setup.sh

Install pyenv
curl -fsSL https://pyenv.run | bash

Add pyenv to shell
cat <<'EOF' >> ~/.bashrc

# Pyenv setup
export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init - bash)"
eval "$(pyenv virtualenv-init -)"
EOF
source ~/.bashrc

Install Python 3.10 and required packages
pyenv install 3.10
pip install psutil readchar

Run BlockAssist 🚀

Move to blockassist directory:

cd blockassist


Activate environment:

pyenv local 3.10.18
python -m venv blockassist-venv
source blockassist-venv/bin/activate


Make sure XLaunch (VcXsrv) is running.

Start BlockAssist:

python run.py


Enter Hugging Face token.

Login to Gensyn Testnet via browser: http://localhost:3000

Play Minecraft:

Two windows pop up (may take a while)

Press ENTER in Ubuntu/WSL terminal

Go to first Minecraft window → Press Enter twice → Move with WASD keys

How to Play?

Watch the demo video.

Check logs
tail -f blockassist/logs/malmo.log

FAQ ❓
1️⃣ How to start the next day:
cd blockassist
source blockassist-venv/bin/activate
python run.py


Make sure XLaunch is running in background.
