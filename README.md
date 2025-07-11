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

+/-5%: </br>
* [Quadro 6000 6GB (2010)](https://www.nvidia.com/docs/IO/40049/NV_DS_QUADRO_6000_Oct10_US_LR.pdf) = [GTX 470 1.2GB (2010)](https://www.techpowerup.com/gpu-specs/geforce-gtx-470.c267) </br>
* [GTX Titan 6GB (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan.c1996) = [Quadro K6000 12GB (2013)](https://www.nvidia.com/content/PDF/data-sheet/NV_DS_Quadro_K6000_OCT13_NV_US_LR.pdf) = [GTX 970 4GB (2014)](https://www.techpowerup.com/gpu-specs/geforce-gtx-970.c2620) = [GTX 780 3GB (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-780.c1701) = [GTX 1650 4GB (2019)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1650.c3366) </br>
* [Quadro K5200 8GB (2014)](https://images.nvidia.com/aem-dam/en-zz/Solutions/design-visualization/documents/DS-NV-Quadro-K5200-JUL24-US-NV-r-HR.pdf) = [GTX 1050Ti 4GB (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) </br>
* [Titan Black 6GB (2014)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan-black.c2549)  = [GTX 1060 6GB (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1060-6-gb.c2862) = [GTX 780Ti 3GB (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-780-ti.c2512) </br>
* [Titan X Maxwell 12GB (2015)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan-x.c2632) = [Quadro M6000 12GB (2015)](https://images.nvidia.com/content/pdf/quadro/data-sheets/NV_DS_Quadro_M6000_FEB15_NV_US_FNL_HR.pdf) </br>
* [Quadro M6000 24GB (2016)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/NV-DS-Quadro-M6000-24GB-US-NV-fnl-HR.pdf) = [GTX 980Ti 6GB (2015)](https://www.techpowerup.com/gpu-specs/geforce-gtx-980-ti.c2724) = [GTX 1070 (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1070.c2840) = [RTX 3050 8GB (2022)](https://www.techpowerup.com/gpu-specs/geforce-rtx-3050-8-gb.c3858) </br>
* [Titan X Pascal 12GB (2016)](https://www.techpowerup.com/gpu-specs/titan-x-pascal.c2863) = [Quadro P6000 24GB (2016)](https://images.nvidia.com/content/pdf/quadro/data-sheets/192152-NV-DS-Quadro-P6000-US-12Sept-NV-FNL-WEB.pdf) = [GTX 1080Ti 11GB (2017)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1080-ti.c2877) = [Quadro RTX 5000 16GB (2018)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/quadro-rtx-5000-data-sheet-us-nvidia-704120-r4-web.pdf) = [RTX 3060Ti 8GB (2020)](https://www.techpowerup.com/gpu-specs/geforce-rtx-3060-ti.c3681) </br>

GTX 1650 4GB (2019) is an improved > GTX 1050Ti (2016) with a weird name, some claim [+17%](https://gpu.userbenchmark.com/Compare/Nvidia-GTX-1650-vs-Nvidia-GTX-1050-Ti/4039vs3649) some [24%](https://technical.city/en/video/GeForce-GTX-1050-Ti-vs-GeForce-GTX-1650), </br>
but ¿works with driver 470? probably Not, most likely requires driver 5xx ¿works with 32-Bit Legacy LibGL1 ? Unknown. </br>

M6000 24GB (2016) works with driver 470-propietary, havent tested Server-470 driver, GTX 1050Ti feels more stable with driver 470, at 50fps there is little improvement in drop frames, the steam falling down at the beginning. </br>
its safe to assume cards [from 2016](https://www.techpowerup.com/gpu-specs/?released=2016&sort=name) work with driver 470, exept cards from [2010](https://www.techpowerup.com/gpu-specs/?released=2010&sort=name) that require driver 390. </br>
from [2011](https://www.techpowerup.com/gpu-specs/?released=2011&sort=name), [2012](https://www.techpowerup.com/gpu-specs/?released=2012&sort=name), [2013](https://www.techpowerup.com/gpu-specs/?released=2013&sort=name), [2014](https://www.techpowerup.com/gpu-specs/?released=2014&sort=name), [2015](https://www.techpowerup.com/gpu-specs/?released=2015&sort=name) maybe, [2017](https://www.techpowerup.com/gpu-specs/?released=2017&sort=name), [2018](https://www.techpowerup.com/gpu-specs/?released=2018&sort=name), [2019](https://www.techpowerup.com/gpu-specs/?released=2019&sort=name), [2020](https://www.techpowerup.com/gpu-specs/?released=2020&sort=name),[2021](https://www.techpowerup.com/gpu-specs/?released=2021&sort=name) </br>
probably wont work with GPU's from [2022](https://www.techpowerup.com/gpu-specs/?released=2022&sort=name), [2023](https://www.techpowerup.com/gpu-specs/?released=2023&sort=name), [2024](https://www.techpowerup.com/gpu-specs/?released=2024&sort=name), [2025](https://www.techpowerup.com/gpu-specs/?released=2025&sort=name) </br>

Top of the line Quadro cards usually have more memory vs. GTX "Gaming" cards, but older games do Not use that amount of memory. </br>
Older cards have Larger transistor size = more power consumption at same performance level. </br>
outdated [Legacy CUDA Compute Capability](https://developer.nvidia.com/cuda-legacy-gpus) version, </br>
older OpenGL version, [RTX cards "Newer" Compute capability](https://developer.nvidia.com/cuda-gpus) </br>
The advantage is compatibility with 32-Bits. </br>

[Quadro P400 2GB (2017)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/productspage/quadro/quadro-desktop/quadro-pascal-p400-data-sheet-us-nv-704503-r1.pdf) works with driver 470, but barely, 13 fps to 15 fps, All Max. + PhysX </br>
![Screenshot_20250709_140924](https://github.com/user-attachments/assets/b9fd9a31-76d9-4202-9185-cbf5bf58e95f)
![Screenshot_20250705_191843](https://github.com/user-attachments/assets/65611782-bb87-4d63-b91e-b372af7ee25d)
![Screenshot_20250711_124838](https://github.com/user-attachments/assets/ac0648fc-9948-4b34-bc75-bc02c863b2f5)
![Screenshot_20250711_110606](https://github.com/user-attachments/assets/610e1ccf-5a89-49af-a40e-d87459641599)
![Screenshot_20250711_110808](https://github.com/user-attachments/assets/c42f4984-9755-449a-ba37-e73374ea6296)

HW Accelerated PhysX has 2 settings: Medium & High, </br>
there is almost No improvement in dropped frames at the beginning Steam falling, </br>
15fps vs. 16fps, using GTX 1050Ti vs. M6000 24GB "GTX 980Ti / 1070" </br>
i've read somewhere that PhysX is limited by CPU x32 instructions. </br>
or maybe the game really requires 2x GPU's </br>

intel Z790 i3-12100 gen CPU's are faster in 32-Bit vs. AMD x670e 7600x, using Rebirth 338 Benchmark, intel is twice faster. </br>
Server boards have more PCIe lanes, but CPU's are slower, GPU's improve with a fast CPU. </br>

maybe the P400 can be used as 2nd GPU + GTX 1050Ti. </br>

problem of gamer boards & CPU's using 2x GPU's is that have very little PCIe lanes [20 vs 24](https://www.cpu-monkey.com/en/compare_cpu-intel_core_i3_12100-vs-amd_ryzen_5_7600x) </br>
Board goes crazy if install more PCIe than available, </br>
requires to remove CR2032 battery to restore Defaults, & wait a few minutes to auto-reconfigure again. </br>

--------------------------

Wine vs. [Proton vs. Proton-GE](https://www.reddit.com/r/SteamDeck/comments/wkx8v9/proton_vs_proton_ge_va_experimental/) </br>

[what version of Proton?](https://www.gamingonlinux.com/guides/view/why-are-there-so-many-different-proton-versions-proton-8-proton-9-experimental-ge-proton/) </br>

[Releases](https://github.com/GloriousEggroll/proton-ge-custom/releases) </br>

---------------------------
