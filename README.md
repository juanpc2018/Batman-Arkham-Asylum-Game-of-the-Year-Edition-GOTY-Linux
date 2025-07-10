# Batman Arkham Asylum Game of the Year Edition "GOTY" on Linux

32-Bit game </br>
[Works Ok](https://odysee.com/@MyAwesomeChannel3:7/2025-07-09-19-59-00:9) </br>

All maximum settings. </br>

3440x1440x50fps  </br>
incl. [PhysX](https://en.wikipedia.org/wiki/Category:Video_games_using_PhysX) </br>

[X] VSync in the game. </br>
[X] Vsync in NVIDIA X Settings. *Optional, Not Required. </br>

[Steam GOTY](https://store.steampowered.com/app/35140/Batman_Arkham_Asylum_Game_of_the_Year_Edition/) </br>
[GOG GOTY](https://www.gog.com/en/game/batman_arkham_asylum_goty).[(2009)](https://www.gog.com/dreamlist/game/batman-arkham-asylum-2009) </br>
[Epic](https://store.epicgames.com/en-US/p/batman-arkham-asylum) </br>

-------------------------

GPU: Nvidia [GTX 1050Ti 4GB (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) </br>

Linux Driver: 470-propietary </br>
Legacy OpenGL drivers: </br>
Libgl1 </br>
vdpau to gl </br>

i have a [dual fan version from MSI](https://msi.com/Graphics-Card/GeForce-GTX-1050-Ti-GAMING-X-4G/Specification) </br>
when 1x fan gets stuck because a blade bends, and jams the fan, </br>
the other fan spins at 100% until you manually unstuck the other fan. </br>

-------------------------------------

[LG 34GP63A](https://www.lg.com/us/monitors/lg-34gp63a-b-gaming-monitor) </br>

can have 160fps using DisplayPort v1.4 </br>
but... </br>
Not Real, its compressed h.264, Bits are reduced. </br>

True 160fps at 3440x1440 Requires latest generation DP 2.0 </br>
HDMI is limited to 50fps at 3440x1440 </br>
works ok. </br>

is possible to lower resolution & increase frame rate, </br>
Higher resolution does Not require Anti-aliasing, </br>
Anti-Aliasing consumes more GPU. </br>
Higher resolution looks better, 50fps is enough. </br>

Latest RTX 5000 GPU's dont work with 32-Bit PhysX on Windows, </br>
Linux Unknown, probaly the same if its Hardware or Propietary driver feature removed. </br>

Linux is Tricky to make it work with 32-Bit games. </br>
different GPU require different drivers. </br>
Not all drivers support Legacy 32-Bit OpenGL on Linux. </br>

1050 Ti Works driver 470, almost Flawless at 3440x1440x50fps. </br>
requires a Fast CPU like 7600x or 12700k </br>

----------------------

Sound: Focusrite Scarlett mk2 USB </br>
6.3 Kernel lowlatency or liquorix </br>
requires: Qjackctl, </br>
does Not sound with Pulse Audio. </br>
maybe its a configuration problem with Wine, maybe winetricks or protontricks could solve. </br>

JackAudio works "out of the box" </br>
Sample Rate: 48kHz </br>
Frames: 256 </br>
Buffer: 2 </br>
Latency 10.7ms </br>
alsa </br>
i/o Device: hw:USB </br>

----------------------

OS: </br>
[pearOS 20.04.4 LTS](https://archive.org/details/pearOS_Monterey_64bit-12-beta-2021.07.01) </br>
"modified Ubuntu/Kubuntu" Not updated to 20.04.6 LTS </br>

Original [Ubuntu 20.04.4](https://old-releases.ubuntu.com/releases/focal/) has a problem with: </br>
pulseaudio-module-jack = Not recommended for JackAudio. </br>

Haven't tested [Kubuntu 20.04.4 LTS](https://web.archive.org/web/20220312054528/http://cdimage.ubuntu.com/kubuntu/releases/20.04.4/release/kubuntu-20.04.4-desktop-amd64.iso.torrent) | [SHA256SUM](https://web.archive.org/web/20220305015630/http://cdimage.ubuntu.com/kubuntu/releases/20.04.4/release/SHA256SUMS) | [archive](https://web.archive.org/web/20220305014143/https://cdimage.ubuntu.com/kubuntu/releases/20.04.4/release/) </br>

pulseaudio-moduile-jack is required to play audio from Firefox & any other software Not designed for JackAudio. </br>

install: </br>
Synaptic </br>
cpupower-gui </br>
cpu-x </br>

set: CPU to: Performance mode. </br>

Maybe other OS & configurations could work, but Untested. </br>

-------------------

Game installer / Loader: </br>
[Lutris v0.5.18 .deb](https://github.com/lutris/lutris/releases) </br>

[EAappinstaller.exe](https://www.ea.com/ea-app#downloads) </br>

[Wine 32-Bit Focal stable](https://gitlab.winehq.org/wine/wine/-/wikis/Debian-Ubuntu) </br>

```
$ sudo dpkg --add-architecture i386 
$ sudo mkdir -pm755 /etc/apt/keyrings
$ wget -O - https://dl.winehq.org/wine-builds/winehq.key | sudo gpg --dearmor -o /etc/apt/keyrings/winehq-archive.key -
$ sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/focal/winehq-focal.sources
$ sudo apt install --install-recommends winehq-stable
```

------------------------

Game complains twice that 1050 Ti is Not recommended when activating PhysX, because that GPU did Not exist, </br>
but works Flawless 90% of the time. </br>
sometimes 1050Ti has frame drops "less than 50fps" at 3440x1440 with all Max. + PhysX </br>

Does Not require installing PhysX Legacy driver, Nor a better GPU, </br>
smoke & particles are working fine "out of the box" </br>
[PhysX v9.13](https://www.nvidia.com/en-us/drivers/physx/physx-9-13-0604-legacy-driver/) | [PhysX v9.12](https://www.nvidia.com/en-us/drivers/physx/9_12_1031/physx-9-12-1031-legacy-driver/) | [Latest v9.19](https://www.nvidia.com/en-us/drivers/physx/9_19_0218/physx-9-19-0218-driver/) </br>
*Untested. </br>

the most GPU demanding part / scene is at the beginnig, a lot of steam falling. </br> 
GTX 1060 6GB or GTX 1070 could be better at 50fps "100% stable / No occacional frame drops." </br>
GTX Titan 6GB / Black are older versions of the GTX 1060 6GB </br>
GTX 780 / 780-Ti have 3GB of Ram, there is a 4GB version, similar to GTX 1060 3GB. </br>
AMD HD 7950 = GTX 1050 Ti, but... when PhysX is Enabled, 1050-Ti is Far better. </br>
To play without PhysX removes [Smoke/Fog & particles](https://www.youtube.com/watch?v=ceD4bFi-zk0&t=9s) </br>

Running the game without Vsync is pointless, unless its a Benchmark. </br>
generates more fps = consumes more energy = generates more heat = requires louder fans but monitor cannot display. </br>

Batman does [Not have in-game Benchmark GOTY v1.1](https://steamcommunity.com/app/35140/discussions/0/792924412089062355/?ctp=1) </br>
but... </br>
[Unigine Tropics-1.3](https://benchmark.unigine.com/tropics) </br>
[.run](https://assets.unigine.com/d/Unigine_Tropics-1.3.run) </br>

its a pure 32-Bit benchmark, </br>
if Tropics works, Batman works. </br>

[Heaven-4.0](https://benchmark.unigine.com/heaven) its a 64-Bit Benchmark </br>
[.run](https://assets.unigine.com/d/Unigine_Heaven-4.0.run) </br>

If Heaven-4 works, does Not test / guarante if Batman will. </br>


OBS 25.03.3 </br>
AMD 7600x </br>
ASRock x670e UEFI v2.10 </br>

OBS can record the whole Screen / all with: </br>
Screen Capture (XSHM) </br>
3D games look ok on screen, but recording .h264 .mkv has Tearing... </br>

3D Requires another source with higher priority: </br>
Window Capture (Xcomposite) </br>
[X] Lock X server when capturing to BATMAN Window,</br>
Option is only visible when game is Running. </br>
and/or Turn-Off Screen Capture (XSHM) </br>

--------------------------------------------

#### Quadro 6000 (2010) 

Requires Driver 390-propietary, </br>
installing that driver in 20.04.4 LTS is Tricky. </br>


