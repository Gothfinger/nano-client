# nano-client [Apex External Cheat For Linux]

# Important Info
My own fork from the famous zap-client, which in turn came from xap-client.
https://www.unknowncheats.me/forum/apex-legends/628823-zap-client-legitbot-ragebot-glow-esp.html

Linux has been banned on Apex Legends since Nov 1 - 2024. This however doesn't make it impossible to use Linux, you simply need to fix a VM and some GPU passthrough etc.

# Core Info

By Gothfinger

All credits to original owners

Instructions are down below

Never cheat on a main account, its not worth it

# Information

The write to mouse is wonky - much better to hide pids and use write to memory. There is no way any AC could find it anyway if done correctly.

<details>
<summary><b>Feature List</b></summary>

    Legitbot - Aimbot, RCS, Visuals
    Ragebot - Aimbot, RCS
    Flickbot
    Triggerbot
    Glow - Player, Viewmodel & Item
    ESP - Enemy & Teammate, Spectator List, Crosshair, Radar
    Misc - Movement, Camera (Quick Turn), Rapid Fire (For Semi-Auto & Burst Weapons), Skin Changer (Basic, not to be confused with a model changer)
    Settings - Disable Overlay, Disable ESP, FPS Cap
    Configs - Custom Configs, Premade Configs

</details>

# Other Repositories:
https://github.com/Gerosity/zap-client-Read-Only-   - A read memory only version

https://github.com/Gerosity/Apex-Protection         - A protection guide, not fully tested but its not like its going to hurt using it

# Before Installation
**Install Linux**

    Not hard at all, use Google & YouTube. Search "How to dual boot Linux and windows"
    NOTE: It is recommened to use GNOME or Cinnamon as your desktop environment. KDE Plasma is known not to allow the overlay to be drawn above the game.
    Other desktop environments may work

**Install Steam & Apex**
  
    Use YouTube & Google for this.
    if upon opening apex you get a black screen and it does not open, follow this: https://www.unknowncheats.me/forum/4012140-post13.html

    # Installation
**1 Install dependencies**
<details>
<summary><b>Debian dependencies</b></summary>
    
    sudo apt-get install -y libudev-dev
    sudo apt install cmake xorg-dev libglu1-mesa-dev libxrandr-dev libxinerama-dev libxcursor-dev libxi-dev
    sudo apt install -y libudev-dev libglu1-mesa-dev libxkbcommon-dev libwayland-dev git cmake g++ gcc libinput-dev libsoil-dev
    sudo apt-get install build-essential
    sudo apt-get install libx11-dev
    sudo apt-get install libxtst-dev

</details>
<details>
<summary><b>Arch dependencies - Look through the UC thread for any more information</b></summary>
    
    sudo pacman -Sy libudev0 cmake xorg-server git base-devel libx11 libxtst

</details>

**2.Build glfw**

    git clone https://github.com/glfw/glfw.git
    cd glfw
    mkdir build
    cd build
    cmake ..
    make
    sudo make install

**3. Exit the terminal and re-open it (So that you dont build the cheat directly into the GLFW build folder, wont work otherwise)**

**4. Clone repo**

    git clone https://github.com/Gerosity/zap-client.git
    cd zap-client

**5. Build & Run**

    mkdir build
    cd build
    cmake ..
    make
    chmod +x run.sh
    ./run.sh

**6. Press Insert to toggle the Menu (You can only interact with the Menu and the game when the menu is active).**
**Note: You will need to alt+tab between the cheat overlay and apex.**

**7 How to manually hide the process from AC**

    Don't worry, there's no need to access that file or anything, just do the following.
        Start Apex
        Wait until you're in main menu
        Open terminal
        Run this command: sudo sysctl -w kernel.yama.ptrace_scope=2
        Run this command: sudo mount -o remount,rw,nosuid,nodev,noexec,relatime,hidepid=2 /proc
        Start nano-client
    
    When you close Apex again, follow these steps to undo it so you can properly launch Apex the next time:
        Close Apex
        Open terminal
        Run this command: sudo sysctl -w kernel.yama.ptrace_scope=1
        Run this command: sudo mount -o remount,rw,nosuid,nodev,noexec,relatime,hidepid=0 /proc

# Credits:
    https://github.com/Gerosity/zap-client
    https://github.com/Nexilist/xap-client - for the base, massive credits to them
    https://github.com/arturzxc/grinder - alternate aimbot mode, most of the misc features
    https://github.com/Braziliana/T_TApe - custom config system
    https://www.unknowncheats.me/forum/apex-legends/ - A TON of help, offsets, many additional features & more
    wafflesgaming - aimbot help, Extra ESP Features such as 2D Corners
    0xAgartha & ghostrazzor - run.sh script (Randomises nanoclient binary & Hides PID before execution)
    hir0xy - Version Checker, Overlay Fixes, Cleaner GUI & optimizations here and there
