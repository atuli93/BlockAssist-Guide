Introduction📔

BlockAssist is an AI assistant that learns from its user’s actions in Minecraft. The assistant appears in-game with you, starting with only basic knowledge of the game’s commands. As you play, it learns how to assist you in building, learning directly from your actions. It shows an early demo of assistance learning - a new paradigm for aligning agents to human preferences across domains.



👨🏻‍💻 Genysn BlockAssist Guide 👨🏻‍💻

image

Device/System Requirements 💻

Minimum RAM = 8GB



50-100 GB disk space



Multi‑core CPU



Wont work in VPS (Cpu based) , GPU require



Installation for Mac user: Follow :::: They dont need to install VcXsrv: just install these dependencies and all the process is same to play the game. just your start command is diff:



Pre-Requirements 🛠

Install dependencies

sudo apt-get update -y \&\& sudo apt-get install -y make build-essential gcc libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev curl git unzip zip mesa-utils x11-apps x11-xserver-utils libxi6 libxrender1 libxtst6 libxrandr2 libglu1-mesa libopenal1

Install node.js

curl -fsSL https://deb.nodesource.com/setup\_20.x | sudo -E bash - \&\& sudo apt update \&\& sudo apt install -y nodejs

Version

node -v

Install NVIDIA Game Ready Driver {IMPORTANT}

Go To: DOWNLOAD



Select your GPU, Window Vrsoin \& Press Find



Click on View \& Download the GeForce Game Ready Driver



After Dow, Open it \& Do all the processes to Install it into Your Machine:



Restart Your PC to make changes:



Install VcXsrv Windows X Server

Download VcXsrv



Now open the XLaunch (VcXsrv) From Start icon:



Check Multiple windows ✔️



Check Start no client ✔️



Check Disable access control ✔️



Next \& Finish: It gonna run on background:



❗Whenever you are going to play the game, you need to open XLaunch everytime and do all the above process:



image

Set DISPLAY and Audio to ~/.bashrc

echo -e '\\n# WSL2 VcXsrv display setup\\nexport DISPLAY=$(ip route | grep -m1 default | awk '"'"'{print $3}'"'"'):0.0\\nexport LIBGL\_ALWAYS\_INDIRECT=0\\nexport LIBGL\_DEBUG=verbose' >> ~/.bashrc

Reload ~/.bashrc

source ~/.bashrc

Test VcXsrv

xeyes

If a New Tab got pop-up with EYES, Than VcXsrv has set-up perfectly:



Screenshot 2025-08-14 005355

Get Hugging Face API token

1\. Go To: huggingface.co \& Sign Up with Mail:

2\. Verify Your Email

3\. Generate a New Access Token

Click your profile icon (top right corner)



Select “Access Tokens” from the dropdown



Click “New token”



Name: something like “BlockAssist”



Role: choose Write



Click “Create”



4\. Copy \& Save the token immediately - you won’t be able to see it again

5\. 📋 Lost it? Just delete the token and create a new one

Clone \& move to blockassist Repo:

git clone https://github.com/gensyn-ai/blockassist.git

cd blockassist

Install Java 1.8.0\_152

./setup.sh

Install pyenv

curl -fsSL https://pyenv.run | bash

Add pyenv to your shell

cat <<'EOF' >> ~/.bashrc



\# Pyenv setup

export PYENV\_ROOT="$HOME/.pyenv"

\[\[ -d $PYENV\_ROOT/bin ]] \&\& export PATH="$PYENV\_ROOT/bin:$PATH"

eval "$(pyenv init - bash)"

eval "$(pyenv virtualenv-init -)"

EOF

Reload

source ~/.bashrc

Install Python 3.10, psutil \& readchar

pyenv install 3.10

pip install psutil readchar

Run BlockAssist 🚀

1\. Move to blockassist Directory

cd blockassist

2\. Activate the blockassist-venv Environment

pyenv local 3.10.18

python -m venv blockassist-venv

source blockassist-venv/bin/activate

3\. Make sure XLaunch (VcXsrv) running in background

4\. Start the BlockAssist

python run.py

5\. Enter Huggingface Token From HERE

6\. Gensyn Testnet login

You will be prompted to log in through your browser:



http://localhost:3000

open \& Login with your mail (Better to use old mail which u are running rl-swarm)



7\. Play Minecraft

After login, two Minecraft windows will be pop-up (could take a while to open)



After that Press ENTER in your UBUNTU/WSL:



Now go to first Minecraft window \& Press Enter twice \& move your player with wasd keys on keyboard:



image\_2025-08-20\_01-03-10

8\. How to Play?

watch the Video



Check logs:

If your node does not start \& got terminated while starting then check logs in new tab: \& debug it:



tail -f blockassist/logs/malmo.log

FAQ❓

1️⃣ How to start next Day:

1\. Move to blockassist directory \& Activate the Environment

cd blockassist

source blockassist-venv/bin/activate

2\. Make sure XLaunch (VcXsrv) running in background: FOLLOW

3\. Run Script \& Follow all the process which u did previously ✔️

python run.py

Grab Block Role 🦾

1\. First of all your have to take SWARM Role: Follow the process if u have not taken yet:

2\. Go to 🐝@The Swarm channel in DC:

3\. Type \& send /block-verify

4\. Now a Form will pop-up

Screenshot 2025-08-24 at 12 06 50 AM

5\. Enter your Huggingface Block model URL from your Profile:

image

6\. Enter READ ONLY Huggingface User Token FROM HERE

DONE:✔️✔️✔️





