# Batman Arkham Asylum Game of the Year Edition "GOTY" on Linux

32-Bit game </br>
[Works Ok](https://odysee.com/@MyAwesomeChannel3:7/2025-07-09-19-59-00:9) </br>

All maximum settings. </br>

3440x1440x50fps  </br>
incl. [Phys](https://en.wikipedia.org/wiki/Category:Video_games_using_PhysX) [X](https://list.fandom.com/wiki/List_of_games_with_hardware-accelerated_PhysX_support) </br>
but... Dual GPU PhysX does Not work, only 1x GPU. </br>
Hardware Accelerated PhysX: </br>
NORMAL does Not show flags on the ceiling. </br>
HIGH shows all, but requires very fast CPU. </br>

32-Bit PhysX on CPU Requires the fastest CPU on the planet, or will drop to 15fps.  </br>
CPU's are slower in 32-Bit </br>
installing the fastest GPU with CPU PhysX only increase to 16fps. </br>
The only way to play with CPU PhysX is using NORMAL setting. </br>

#### HW tested: </br>
AMD 7600x </br>
[ASRock X670E PG](https://pg.asrock.com/mb/AMD/X670E%20PG%20Lightning/index.asp) UEFI v2.10 </br>
intel i3-12100 </br>
[ASRock Z790 LiveMixer](https://www.asrock.com/mb/Intel/Z790%20LiveMixer/Specification.asp) UEFI v9.04 </br>

[X] VSync in the game. </br>
[X] Vsync in NVIDIA X Settings. *Optional, Not Required. </br>

[Steam GOTY](https://store.steampowered.com/app/35140/Batman_Arkham_Asylum_Game_of_the_Year_Edition/) </br>
[GOG GOTY](https://www.gog.com/en/game/batman_arkham_asylum_goty).[(2009)](https://www.gog.com/dreamlist/game/batman-arkham-asylum-2009) </br>
[Epic](https://store.epicgames.com/en-US/p/batman-arkham-asylum) </br>

-------------------------

### Mistery Solved: </br>

2x GPU does Not work, Not Win8.1 x64, Not Linux 20.04.4 LTS. </br>

Windows driver allows to select PhysX mode: </br>
CPU, GPU1 or GPU2 </br>

Linux Driver 470.xx does Not allow to select PhysX mode. </br>
Linux 470 driver Default: PhysX CPU. </br>

## Problem: </br>
Nvidia DELETED 32-Bit PhysX Hardware support since 2016-Q4, </br>
if you install a (2016-Q4) GPU like GTX 1050 Ti + Quadro P400 (2017) or similar </br>
Nvidia driver 416.xx allows to select PhysX GPU, but does Not work, with Batman Arkham Asylum v1.1 </br>

At the beginning of the game, there is a tunnel with steam falling. </br>
IF activate PhysX HIGH setting in Linux or Windows BMlauncher.exe  </br>
Only works using CPU PhysX. </br>
problem using PhysX on CPU is that frames drop to 15fps on a modern i3-12100 or 7600x </br>
Requires 1-core, 100% CPU load, CPU PhysX does Not have Multi-Thread. </br>
CPU´s are slower in 32-Bit </br>
but CPU PhysX works, Windows & Linux. </br>

*haven't tested Linux 390.xx / 340.xx drivers </br>

to make PhysX work with GPU HW, in Windows: </br>
Requires installing an older GPU from (2008-2016-Q1/Q2) </br>
2016-Q3 Unknown. </br>

### Confirmed GPU´s working with 32-Bit PhysX HW / on GPU die: </br>

* GTX 260, 9800 GTX, GTX 280, [GTX 275](https://www.techpowerup.com/gpu-specs/geforce-gtx-275-physx-edition.c1951), GTX 470, GTX 580, Quadro 6000 (2010) </br>
* Quadro M6000 24GB (March 5th, 2016-Q1) Works OK, </br>
* Quadro M6000 12GB (2015) should work ok. </br>
* Quadro M2000 (April 8th, 2016-Q2) works ok. </br>
Probably work: </br>
* GTX 680, GTX Titan 6GB, GTX Titan Black (2014), Quadro K6000 (2013), K5200 (2014) or similar </br>

Unknown: 2016-Q3 </br>

### Don't work: </br>
* GTX 1050 Ti (October 25th, 2016-Q4), P400 (2017) </br>

Seems NVIDIA Christmas Gift for December of 2016 was Deleting 32-Bit PhysX. </br>

### people with mini-ATX boards "1x PCIe x16 slot": </br>
Dual-GPU´s for 32-Bit PhysX are: </br>
[9800 GX2 (2008)](https://www.techpowerup.com/gpu-specs/geforce-9800-gx2.c208), [FX-4700 X2 (2008)](https://www.techpowerup.com/gpu-specs/quadro-fx-4700-x2.c1337) </br>
[GTX 285 X2 (2009)](https://www.techpowerup.com/gpu-specs/geforce-gtx-285-x2.c4140), [GTX 295 Single pcb (2009)](https://www.techpowerup.com/gpu-specs/geforce-gtx-295-single-pcb.c4141), [GTX 295 dual pcb (2009)](https://www.techpowerup.com/gpu-specs/geforce-gtx-295.c239) </br>
[GTX 590 (2011)](https://www.techpowerup.com/gpu-specs/geforce-gtx-590.c281) </br>
[GTX 690 (2012)](https://www.techpowerup.com/gpu-specs/geforce-gtx-690.c361) </br>
[GTX 760 X2 (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-x2.c2521) </br>
[Titan Z (2014)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan-z.c2575) </br>
all should work "the same" with Vsync=On. </br>

A Fast GPU from 2015-2016-Q1/Q2 with 32-Bit PhysX, can be Forced: Video + PhysX on the same GPU, works Ok </br>
No need for Dual-GPU´s. </br>
Quadro M2000 (2016-Q2) works ok, PhysX High, single GPU, FullHD 50fps. </br>

2011-2016-Q1/Q2 Server GPU´s depends on [drivers](https://www.nvidia.com/en-us/drivers/) Could Work, Untested.</br>
| * 3D printed Fan duct required from Thingiverse or similar. </br> 
| ** [MXM to PCIe adapter](https://github.com/a-little-wifi/mxm-immobilizer) required. </br>
#### [2008:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2008&sort=name) </br>
[FX-3600m](https://www.techpowerup.com/gpu-specs/quadro-fx-3600m.c1440) ** | [FX-3800m](https://www.techpowerup.com/gpu-specs/quadro-fx-3800m.c1392) ** | </br>
[Quadro CX](https://www.techpowerup.com/gpu-specs/quadro-cx.c1326) | [FX-4700x2](https://www.techpowerup.com/gpu-specs/quadro-fx-4700-x2.c1337) | [Quadro FX-4800 PC](https://www.techpowerup.com/gpu-specs/quadro-fx-4800.c1320) / [Mac Edition](https://www.techpowerup.com/gpu-specs/quadro-fx-4800-mac-edition.c1322) | [FX-5800](https://www.techpowerup.com/gpu-specs/quadro-fx-5800.c1319) </br>
[Tesla M1060](https://www.techpowerup.com/gpu-specs/tesla-m1060.c1888) </br>
[S1070](https://www.techpowerup.com/gpu-specs/tesla-s1070.c1540) * | [S1075](https://www.techpowerup.com/gpu-specs/tesla-s1075.c1541) *</br>
#### [2009:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2009&sort=name) </br>
[FX 580](https://www.techpowerup.com/gpu-specs/quadro-fx-580.c1324) | [FX 3800](https://www.techpowerup.com/gpu-specs/quadro-fx-3800.c1321) </br>
[Tesla C1060](https://www.techpowerup.com/gpu-specs/tesla-c1060.c1539) | [Tesla C1080](https://www.techpowerup.com/gpu-specs/tesla-c1080.c2449) </br>
#### [2010:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2010&sort=name) </br>
[NVS-5100m](https://www.techpowerup.com/gpu-specs/nvs-5100m.c1466) ** | [Quadro FX-880m](https://www.techpowerup.com/gpu-specs/quadro-fx-880m.c1394) **</br>
#### [2011:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2011&sort=name) </br>
[C2050](https://www.techpowerup.com/gpu-specs/tesla-c2050.c923) | [C2070](https://www.techpowerup.com/gpu-specs/tesla-c2070.c924) | [C2075](https://www.techpowerup.com/gpu-specs/tesla-c2075.c563) | [C2090](https://www.techpowerup.com/gpu-specs/tesla-c2090.c2317) </br>
[M2050](https://www.techpowerup.com/gpu-specs/tesla-m2050.c1534) | [M2070](https://www.techpowerup.com/gpu-specs/tesla-m2070.c1535) | [M2070-Q](https://www.techpowerup.com/gpu-specs/tesla-m2070-q.c1536) | [M2075](https://www.techpowerup.com/gpu-specs/tesla-m2075.c2025) | [M2090](https://www.techpowerup.com/gpu-specs/tesla-m2090.c1537) *</br>
[X2070](https://www.techpowerup.com/gpu-specs/tesla-x2070.c2024) ** | [X2090](https://www.techpowerup.com/gpu-specs/tesla-x2090.c1887) **</br>
[Tesla S2050](https://www.techpowerup.com/gpu-specs/tesla-s2050.c1538) *</br>
#### [2012:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2012&sort=name) </br>
[K10](https://www.techpowerup.com/gpu-specs/tesla-k10.c918) *</br>
[K20X](https://www.techpowerup.com/gpu-specs/tesla-k20x.c2315) *</br>
[K20Xm](https://www.techpowerup.com/gpu-specs/tesla-k20xm.c1884) *</br>
[K20Xc](https://www.techpowerup.com/gpu-specs/tesla-k20c.c564) </br>
#### [2013:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2013&sort=name) </br>
[GRID K520](https://www.techpowerup.com/gpu-specs/grid-k520.c2312) * | [GRID K2](https://www.techpowerup.com/gpu-specs/grid-k2.c1700) * | [GRID K1](https://www.techpowerup.com/gpu-specs/grid-k1.c1699) *</br>
[Tesla K20m](https://www.techpowerup.com/gpu-specs/tesla-k20m.c2029) * | [Tesla K20s](https://www.techpowerup.com/gpu-specs/tesla-k20s.c2044) * | [Tesla K40c](https://www.techpowerup.com/gpu-specs/tesla-k40c.c2505) | [Tesla K40d](https://www.techpowerup.com/gpu-specs/tesla-k40d.c3402) | [Tesla K40m](https://www.techpowerup.com/gpu-specs/tesla-k40m.c2529) | [Tesla K40s](https://www.techpowerup.com/gpu-specs/tesla-k40s.c2528) | [Tesla K40st](https://www.techpowerup.com/gpu-specs/tesla-k40st.c2530) | [Tesla K40t](https://www.techpowerup.com/gpu-specs/tesla-k40t.c3403) </br>
#### [2014:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2014&sort=name) </br>
[GRID K500](https://www.techpowerup.com/gpu-specs/grid-k500.c2597) </br>
[Tesla K8](https://www.techpowerup.com/gpu-specs/tesla-k8.c2619) | [Tesla K80](https://www.techpowerup.com/gpu-specs/tesla-k80.c2616) *</br>
#### [2015:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2015&sort=name) </br>
[GRID M6-8Q](https://www.techpowerup.com/gpu-specs/grid-m6-8q.c3052) ** | [GRID M60](https://www.techpowerup.com/gpu-specs/grid-m60-1q.c3087) </br>
[Tesla M4 LowProfile](https://www.techpowerup.com/gpu-specs/tesla-m4.c2770) * | [Tesla M40](https://www.techpowerup.com/gpu-specs/tesla-m40.c2771) * | [Tesla M40 24GB](https://www.techpowerup.com/gpu-specs/tesla-m40-24-gb.c3838) * | [Tesla M6](https://www.techpowerup.com/gpu-specs/tesla-m6-mobile.c2818) [x2](https://www.techpowerup.com/gpu-specs/tesla-m6-x2-mobile.c4123) ** | [Tesla M60](https://www.techpowerup.com/gpu-specs/tesla-m60.c2760) *</br>
#### [2016:](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2016&sort=name) </br>
Q1 & Q2 should work </br>
[GT 610](https://www.techpowerup.com/gpu-specs/geforce-gt-610-oem.c2842) | [GT 710](https://www.techpowerup.com/gpu-specs/geforce-gt-710.c2614) | [920MX](https://www.techpowerup.com/gpu-specs/geforce-920mx.c2826) ** | [945M](https://www.techpowerup.com/gpu-specs/geforce-945m.c2836) ** | [M6000 24GB](https://www.techpowerup.com/gpu-specs/quadro-m6000-24-gb.c2824) </br>
[Quadro M2000](https://www.techpowerup.com/gpu-specs/quadro-m2000.c2837) </br>
[GTX 1070](https://www.techpowerup.com/gpu-specs/geforce-gtx-1070.c2840) | [GTX 1080](https://www.techpowerup.com/gpu-specs/geforce-gtx-1080.c2839) </br>
[M500M](https://www.techpowerup.com/gpu-specs/quadro-m500m.c2843) ** | [M5500](https://www.techpowerup.com/gpu-specs/quadro-m5500-mobile.c2838) ** | [GTX 980MX](https://www.techpowerup.com/gpu-specs/geforce-gtx-980mx.c2808) ** </br>
[GRID M10-8Q](https://www.techpowerup.com/gpu-specs/grid-m10-8q.c3086) * | [GRID M3-3020](https://www.techpowerup.com/gpu-specs/grid-m3-3020.c3084) | [GRID M40](https://www.techpowerup.com/gpu-specs/grid-m40.c2518) </br> 
[Tesla M10](https://www.techpowerup.com/gpu-specs/tesla-m10.c3035) | [Tesla P100 DGXS](https://www.techpowerup.com/gpu-specs/tesla-p100-dgxs.c3285) | [Tesla P100 12GB](https://www.techpowerup.com/gpu-specs/tesla-p100-pcie-12-gb.c2915) [16GB](https://www.techpowerup.com/gpu-specs/tesla-p100-pcie-16-gb.c2888) | [P100 SXM2](https://www.techpowerup.com/gpu-specs/tesla-p100-sxm2.c3183) **** | </br>
Q3 Unknown: </br>
[M3000 SE](https://www.techpowerup.com/gpu-specs/quadro-m3000-se.c2886) | [GTX 1060 3GB](https://www.techpowerup.com/gpu-specs/geforce-gtx-1060-3-gb.c2867) | [GTX 1060 6GB](https://www.techpowerup.com/gpu-specs/geforce-gtx-1060-6-gb.c2862) | [1060M](https://www.techpowerup.com/gpu-specs/geforce-gtx-1060-mobile.c3016) | [1070M](https://www.techpowerup.com/gpu-specs/geforce-gtx-1070-mobile.c2869) | [1080M](https://www.techpowerup.com/gpu-specs/geforce-gtx-1080-mobile.c2870) </br>
[Titan X Pascal "Not Xp"](https://www.techpowerup.com/gpu-specs/titan-x-pascal.c2863) </br>
[Tesla P4](https://www.techpowerup.com/gpu-specs/tesla-p4.c2879) | [Tesla P10](https://www.techpowerup.com/gpu-specs/tesla-p10.c3750) | [Tesla P40](https://www.techpowerup.com/gpu-specs/tesla-p40.c2878) </br>
Q4 does Not work. </br>
[GTX 1050 2GB](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050.c2875) | [GTX 1050 Ti 4GB](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) </br>
[Quadro GP100](https://www.techpowerup.com/gpu-specs/quadro-gp100.c2994) | [Quadro P5000](https://www.techpowerup.com/gpu-specs/quadro-p5000.c2864) | [Quadro P6000](https://www.techpowerup.com/gpu-specs/quadro-p6000.c2865) |  </br>
Unknown Release date: </br>
[940MX](https://www.techpowerup.com/gpu-specs/geforce-940mx.c2797) ** | [GTX 950](https://www.techpowerup.com/gpu-specs/geforce-gtx-950-oem.c2817) | [GTX 965M](https://www.techpowerup.com/gpu-specs/geforce-gtx-965m.c2796) ** | [Jetson TX2](https://www.techpowerup.com/gpu-specs/jetson-tx2.c3231) </br>
GTX 760 was released in 2013 & re-released in 2016-Q4, Unknown if 2016 version works with PhysX, probably </br>
GTX 760 2016 looks like GTX 760 Ti 2013, better vs. GTX 760 2013, Not as good vs. [GTX 770 2013](https://www.techpowerup.com/gpu-specs/geforce-gtx-770.c1856) </br>
[GTX 760 2013](https://www.techpowerup.com/gpu-specs/geforce-gtx-760.c1857) </br>
[GTX 760 X2 (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-x2.c2521) </br>
[GTX 760 OEM 2013](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-oem.c2455) </br>
[GTX 760 rebrand 2013](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-oem-rebrand.c2454) </br>
[GTX 760 Ti OEM 2013](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-ti-oem.c2491) </br>
[GTX 760 Ti OEM Rebrand 2013](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-ti-oem-rebrand.c2453) </br>
[GTX 760 OEM 2016](https://www.techpowerup.com/gpu-specs/geforce-gtx-760-oem.c3743) </br>

GTX 1070 & 1080 GPUs for PCIe were released on 2016-Q2, Mobile MXM versions were released on 2016-Q3, </br>
Unknown if 2016-Q3 Mobile could work, has similar GP, MXM has GP B </br>

Quadro 6000 (2010) "GTX 470" drops to 30fps + Quadro P400 (2017) as Main-GPU in Win8.1x64 at FullHD 1920x1080x50fps </br>
Quadro P400 works as main-GPU, FullHD, 100% GPU load, requires other card for PhysX </br> 

WQHD monitors 3440x1440x50fps require faster main-GPU: Quadro P1000, M2000, or GTX 1050Ti </br>
Quadro P600 as main-GPU probably works at 2560x1440x30. </br>

### Main-GPU: </br>
(2016 or better):  </br>
1920x1080x60 Quadro P400 "Full size bracket" Win8.1 or better  </br>
3440x1440x50 Quadro P1000 or better < GTX 1050Ti </br>
#### PhysX GPU: (2009-2015) </br>
GTX 280 or 9800 GTX or better should work ok. </br>
GTX 480, GTX 580 (2011), GTX 680, GTX 780 </br>
Quadro K1200 (2015), Quadro M2000 (2016-Q2) </br>
#### Single GPU: PhysX High+Video (2009-2016) </br>
Quadro M2000 (2016-Q2) works ok FullHD 50fps </br>
3440x1440x50 single GPU + PhysX High requires Better GPU, probably: M4000, M6000 or GTX 980. </br>

Batman Arkham Asylum v1.1 GPU load is low: 20% 3D & 10% PhysX on GTX 1050 Ti + Quadro M2000. </br>
Windows Nvidia driver allows PhysX to be activated to the Main GPU "Only 1x GPU" </br>
GPU load increase a lot more = fan noise, but "fps" does Not drop as much as CPU PhysX High. </br>

2016 or Newer GPUs are recomended for Main GPU: </br>
have higher HDMI resolution, more power efficient = Lower fan noise. </br>

There is PhysX [v3.2.x](https://developer.nvidia.com/rdp/physx-downloads), [v3.3.x](https://github.com/yangzhengxing/PhysX-3.3), [v3.4.x](https://github.com/NVIDIAGameWorks/PhysX-3.4), [v4.x](https://github.com/NVIDIAGameWorks/PhysX), & [v5.x](https://github.com/NVIDIA-Omniverse/PhysX) for Linux </br>
Unknown why Linux 470 driver does Not have PhysX option. </br>
Tutorial to compile [PhysX 3.3.4 + NVIDIA GeForce GTX 750 Ti + Ubuntu 14.04](https://codeyarns.com/tech/2015-12-03-how-to-use-physx-on-linux.html#gsc.tab=0).[2](https://stackoverflow.com/questions/22742736/how-to-get-nvidias-physx-3-3-to-link-in-linux) </br>
Tutorial for [20.04.x LTS](https://stackoverflow.com/questions/62894488/how-do-you-compile-standalone-snippets-in-nvidia-physx) </br>

[CodeWeavers CrossOver](https://www.codeweavers.com/compatibility/crossover/nvidia-physx) seems to have better PhysX support since Ubuntu 10.10 vs. WineHQ </br>

there is an [Protontricks Tutorial for Linux](https://www.youtube.com/watch?v=pS9OQ7CW6hE) but seems has the same problem: PhysX on CPU. </br>
```
EA Launch Options:

gamemoderun DXVK_ASYNC=1 PROTON_ENABLE_NVAPI=1 %command%
```
PhysX CPU works without adding / Not needed anymore: 
> gamemoderun DXVK_ASYNC=1 PROTON_ENABLE_NVAPI=1

--------------------------

To Disable intro movies Much Faster vs. Press Enter or Click to Skip.
> C:\Users\NAME\Documents\Eidos\Batman Arkham Asylum\BmGame\Config\UserEngine.ini </br>
````
[FullScreenMovie]
+StartupMovies=baa_logo_run_v5_h264-
+StartupMovies=UTlogo-
+StartupMovies=Legal-
+StartupMovies=Install-
````
add a minus at the end. </br>

-------------------------

GPU: Nvidia [GTX 1050Ti 4GB (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) </br>

Linux Driver: 470-propietary </br>
Legacy OpenGL drivers both 64-Bit & i386 </br>
Libgl1 </br>
libgl1-mesa-dri </br>
mesa-vulkan-drivers </br>
libvdpau-va-gl1 </br>

[dual fan 1050Ti from msi](https://msi.com/Graphics-Card/GeForce-GTX-1050-Ti-GAMING-X-4G/Specification) </br>
when 1x fan gets stuck because a blade bends and jams the fan, </br>
the other fan spins at 100% until manually unstuck the other fan. </br>

-------------------------------------

## [LG 34GP63A](https://www.lg.com/us/monitors/lg-34gp63a-b-gaming-monitor) </br>

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

Linux is Tricky to make it work with 32-Bit games. </br>
different GPU require different drivers, </br>
Not all drivers support Legacy 32-Bit OpenGL on Linux. </br>
20.04.4 requires LibGL1 Mesa Vulkan v21.6, and v21.6 requires Nvidia 470 driver. </br>

1050 Ti Works with driver 470, almost Flawless at 3440x1440x50fps. </br>
requires a Fast CPU: AMD 7600x or intel 12100 </br>
PhysX High setting is designed to require dual GPU or much faster CPU. </br>

----------------------

Sound: Focusrite Scarlett mk2 USB </br>
6.3 Kernel lowlatency or liquorix </br>
Also works with on-board Z790 / X670E HD / AC 97 audio. </br>

IF does Not sound, its a problem in Wine. </br>
requires manual configuration: PulseAudio as Output. </br>
![Screenshot_20250711_215841](https://github.com/user-attachments/assets/89b10904-e675-49bb-9033-25386ba6cebd)

Sometimes Wine configuration audio test pass, but game does Not sound. </br>
requires reboot. </br>

Using: Qjackctl </br>
JackAudio works "out of the box" </br>
just needs to select Jack Audio Sink as Main output in Linux </br>

Sample Rate: 48kHz </br>
Frames: 256 </br>
Buffer: 2 </br>
Latency 10.7ms </br>
alsa </br>
i/o Device: hw:USB </br>

Lutris has an option to lower latency in PulseAudio. </br>
Not required using Low latency Kernel or Liquorix. </br>

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
neofetch </br>
screenfetch </br>
set: CPU to: Performance mode. </br>

Maybe [other OS & configurations could work](https://github.com/lutris/docs/blob/master/InstallingDrivers.md) Untested. </br>

Batman GOTY v1.1 does [Not have in-game Benchmark](https://steamcommunity.com/app/35140/discussions/0/792924412089062355/?ctp=1), older (2009) version did, </br>
Anyway... </br>
[Unigine Tropics-1.3](https://benchmark.unigine.com/tropics) [.run](https://assets.unigine.com/d/Unigine_Tropics-1.3.run) </br>
it's a pure 32-Bit benchmark, </br>
if Tropics works, Batman works. </br>

[Heaven-4.0](https://benchmark.unigine.com/heaven) [.run](https://assets.unigine.com/d/Unigine_Heaven-4.0.run) </br>
it´s a mixed 32/64-Bit Benchmark </br>
If OS is 64-Bit & Heaven-4 works, does Not test if Batman will. </br>
can be forced to run 32-Bit in 64-Bit OS. </br>

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

Game complains twice that 1050 Ti is Not recommended when activating PhysX, </br>
but works Flawless 99% of the time with PhysX NORMAL setting. </br>
All GPU's i've tested have frame drops "10fps" in some parts of the game with PhysX HIGH "Requires 2x GPU's" </br>
at the beggining, steam falling, and outside the asylum 4% of the Game, has severe frame drops with HIGH 1x GPU, but works ok with PhysX Normal. </br>
No matter what GPU, performance drops. </br>

Running the game without Vsync is pointless, unless its a Benchmark. </br>
generates more fps = consumes more energy = more heat = louder fans but monitor cannot display. </br>

Does Not require installing PhysX driver, Lutris/EA/Batman installs PhysX 9.14 </br>
smoke & particles work ok "out of the box", with some occacional frame drops with NORMAL setting. </br>
[PhysX v9.12.10](https://www.nvidia.com/en-us/drivers/physx/9_12_1031/physx-9-12-1031-legacy-driver/) Legacy **</br>
[PhysX v9.13.06](https://www.nvidia.com/en-us/drivers/physx/physx-9-13-0604-legacy-driver/) Legacy * </br>
[PhysX v9.13.12](https://www.nvidia.com/en-us/drivers/physx/9_13_1220/physx-9-13-1220-driver/) oldest version that works with Win8.1x64 </br>
[PhysX v9.14.07](https://www.nvidia.com/en-us/drivers/physx/9_14_0702/physx-9-14-0702-driver/) Default Lutris. </br>
[PhysX v9.15.04](https://www.nvidia.com/en-us/drivers/physx/9_15_0428/physx-9-15-0428-driver/) Works the same. </br>
[PhysX v9.16.03](https://www.nvidia.com/en-us/drivers/physx/9_16_0318/physx-9-16-0318-driver/) *</br>
[PhysX v9.17.05](https://www.nvidia.com/en-us/drivers/physx/9_17_0524/physx-9-17-0524-driver/) *</br>
[PhysX v9.18.09](https://www.nvidia.com/en-us/drivers/physx/9_18_0907/physx-9-18-0907-driver/) *</br>
[PhysX v9.19.02](https://www.nvidia.com/en-us/drivers/physx/9_19_0218/physx-9-19-0218-driver/) *</br>
[PhysX v9.23.10](https://www.nvidia.com/en-us/drivers/physx/physx-9-23-1019-driver/) *</br>
*Untested. </br>
** Fail. </br>

[Overview](https://web.archive.org/web/20211225054318/https://developer.nvidia.com/gameworks-physx-overview) </br>

---------------------

### OBS 25.03.3 
OBS can record the whole Screen with: </br>
* Screen Capture (XSHM) </br>
3D games look ok on screen, but recorded .h264 .mkv has Tearing... .mp4 untested. </br>

3D Game Requires another source with higher priority: </br>
* Window Capture (Xcomposite) </br>
[X] Lock X server when capturing BATMAN Window,</br>
Option is only visible when game is Running, Windowed. </br>
and/or Turn-Off Screen Capture (XSHM) </br>

--------------------------------------------

#### Quadro 6000 (2010) 

Requires Driver 390-propietary, </br>
installing that driver in 20.04.4 LTS is Tricky. </br>

+/-5%: </br>
* [Quadro 6000 6GB (2010)](https://www.nvidia.com/docs/IO/40049/NV_DS_QUADRO_6000_Oct10_US_LR.pdf) = [GTX 470 1.2GB (2010)](https://www.techpowerup.com/gpu-specs/geforce-gtx-470.c267) </br>
* [GTX 580 1.5GB Rev1 (2010)](https://www.techpowerup.com/gpu-specs/geforce-gtx-580.c270) [Rev2 (2011)](https://www.techpowerup.com/gpu-specs/geforce-gtx-580-rev-2.c3009) = [Quadro K4200 4GB (2014)](https://www.techpowerup.com/gpu-specs/quadro-k4200.c2602) </br>
* [GTX 680 2GB (2012)](https://www.techpowerup.com/gpu-specs/geforce-gtx-680.c342) = [Quadro K5200 8GB (2014)](https://images.nvidia.com/aem-dam/en-zz/Solutions/design-visualization/documents/DS-NV-Quadro-K5200-JUL24-US-NV-r-HR.pdf) = [Quadro M4000 (2015)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/documents/75509_DS_NV_Quadro_M4000_US_NV_HR.pdf) = [GTX 1050Ti 4GB (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) </br>
* [GTX Titan 6GB (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan.c1996) = [Quadro K6000 12GB (2013)](https://www.nvidia.com/content/PDF/data-sheet/NV_DS_Quadro_K6000_OCT13_NV_US_LR.pdf) = [GTX 780 3GB (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-780.c1701) = [GTX 970 4GB (2014)](https://www.techpowerup.com/gpu-specs/geforce-gtx-970.c2620)  = [GTX 1650 4GB (2019)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1650.c3366) </br>
* [Titan Black 6GB (2014)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan-black.c2549)  = [GTX 1060 6GB (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1060-6-gb.c2862) = [GTX 780Ti 3GB (2013)](https://www.techpowerup.com/gpu-specs/geforce-gtx-780-ti.c2512) </br>
* [Titan X Maxwell 12GB (2015)](https://www.techpowerup.com/gpu-specs/geforce-gtx-titan-x.c2632) = [Quadro M6000 12GB (2015)](https://images.nvidia.com/content/pdf/quadro/data-sheets/NV_DS_Quadro_M6000_FEB15_NV_US_FNL_HR.pdf) </br>
* [Quadro M6000 24GB (2016-Q1)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/NV-DS-Quadro-M6000-24GB-US-NV-fnl-HR.pdf) = [GTX 980Ti 6GB (2015)](https://www.techpowerup.com/gpu-specs/geforce-gtx-980-ti.c2724) = [GTX 1070 (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1070.c2840) = [RTX 3050 8GB (2022)](https://www.techpowerup.com/gpu-specs/geforce-rtx-3050-8-gb.c3858) </br>
* [GTX 1070Ti 8GB (2017)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1070-ti.c3010) = [Quadro RTX 4000 8GB (2019)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/quadro-rtx-4000-datasheet.pdf) </br>
* [Titan X Pascal 12GB (2016)](https://www.techpowerup.com/gpu-specs/titan-x-pascal.c2863) = [Quadro P6000 24GB (2016)](https://images.nvidia.com/content/pdf/quadro/data-sheets/192152-NV-DS-Quadro-P6000-US-12Sept-NV-FNL-WEB.pdf) = [GTX 1080Ti 11GB (2017)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1080-ti.c2877) = [Quadro RTX 5000 16GB (2018)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/quadro-product-literature/quadro-rtx-5000-data-sheet-us-nvidia-704120-r4-web.pdf) = [RTX 3060Ti 8GB (2020)](https://www.techpowerup.com/gpu-specs/geforce-rtx-3060-ti.c3681) </br>

+/-7% </br>
Quadro P1000 (2017) > GTX 580 (2010) > Quadro M2000 (2016-Q2) </br>
Quadro K6000 (2013) specs. = GTX Titan Black (2014) but K6000 is underclocked & Titan are Overclocked</br>
Quadro K6000 performance = GTX Titan 6GB (2013). </br>
[AMD HD 7950](https://www.techpowerup.com/gpu-specs/radeon-hd-7950.c307) performance = [GTX 1050 Ti](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) No PhysX </br>
No PhysX removes [Smoke/Fog & particles](https://www.youtube.com/watch?v=ceD4bFi-zk0&t=9s) </br>

GTX 1650 4GB (2019) is an improved > GTX 1050Ti (2016) with weird name, some claim [+17%](https://gpu.userbenchmark.com/Compare/Nvidia-GTX-1650-vs-Nvidia-GTX-1050-Ti/4039vs3649) some [+24%](https://technical.city/en/video/GeForce-GTX-1050-Ti-vs-GeForce-GTX-1650), </br>
¿works with driver 470 ? probably Not, most likely requires driver 5xx </br>
¿works with 32-Bit Legacy LibGL1 / Mesa v21.6 ? most likely requires OS 22.04 LTS or 24.04 LTS with Newer LibGL1 </br>

M6000 24GB (2016-Q1) works with driver 470-propietary on Linux but Not PhysX, havent tested Server-470 driver, at 50fps there is No improvement vs. GTX 1050 Ti, with CPU PhysX HIGH. </br>
its safe to assume cards [from 2016](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2016&sort=name) work with driver 470, exept cards from [2010](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2010&sort=name) that require driver 390. </br>
from [2011](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2011&sort=name), [2012](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2012&sort=name), [2013](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2013&sort=name), [2014](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2014&sort=name), [2015](https://www.techpowerup.com/gpu-specs/?mfgr=NVIDIA&released=2015&sort=name) maybe, [2017](https://www.techpowerup.com/gpu-specs/?released=2017&sort=name), [2018](https://www.techpowerup.com/gpu-specs/?released=2018&sort=name), [2019](https://www.techpowerup.com/gpu-specs/?released=2019&sort=name), [2020](https://www.techpowerup.com/gpu-specs/?released=2020&sort=name),[2021](https://www.techpowerup.com/gpu-specs/?released=2021&sort=name) </br>
probably wont work with GPU's from [2022](https://www.techpowerup.com/gpu-specs/?released=2022&sort=name), [2023](https://www.techpowerup.com/gpu-specs/?released=2023&sort=name), [2024](https://www.techpowerup.com/gpu-specs/?released=2024&sort=name), [2025](https://www.techpowerup.com/gpu-specs/?released=2025&sort=name) </br>
[RTX 5000 (2025)](https://www.techpowerup.com/gpu-specs/geforce-rtx-5050.c4220) dont work with 32-Bit PhysX, Only CPU. </br>

Top of the line Quadro cards usually have more memory vs. GTX "Gaming" cards, but older games do Not use that amount of memory. </br>
Older cards have Larger transistor size = more power consumption at same performance level. </br>
outdated [Legacy CUDA Compute Capability](https://developer.nvidia.com/cuda-legacy-gpus) version, </br>
older OpenGL version, [RTX cards "Newer" Compute capability](https://developer.nvidia.com/cuda-gpus) </br>
Advantage is compatibility with 32-Bits. </br>

[Quadro P400 2GB (2017)](https://www.nvidia.com/content/dam/en-zz/Solutions/design-visualization/productspage/quadro/quadro-desktop/quadro-pascal-p400-data-sheet-us-nv-704503-r1.pdf) works with driver 470, </br>
at 3440x1440x50 13 fps to 15 fps, All Max. + PhysX HIGH </br>
P400 works at 1920x1080x60 100% GPU load, PhysX Normal. </br>
P400 is inferior vs. GTX 1050 Ti, but faster vs. recommended GPU´s GTX 260 + 9800 GTX </br>
![Screenshot_20250709_140924](https://github.com/user-attachments/assets/b9fd9a31-76d9-4202-9185-cbf5bf58e95f) </br>
![Screenshot_20250705_191843](https://github.com/user-attachments/assets/65611782-bb87-4d63-b91e-b372af7ee25d) </br>
![Screenshot_20250711_124838](https://github.com/user-attachments/assets/ac0648fc-9948-4b34-bc75-bc02c863b2f5) </br>
![Screenshot_20250711_110606](https://github.com/user-attachments/assets/610e1ccf-5a89-49af-a40e-d87459641599) </br>
![Screenshot_20250711_110808](https://github.com/user-attachments/assets/c42f4984-9755-449a-ba37-e73374ea6296) </br>

CPU PhysX: </br>
there is No improvement in dropped frames </br>
15fps vs. 16fps, using GTX 1050Ti vs. M6000 24GB twice faster! "GTX 980Ti / 1070"  </br>
1920x800 Windowed vs. 3440x1440 Full screen, same. </br>

[CUDA 12 Toolkit removed 32-Bit](https://nvidia.custhelp.com/app/answers/detail/a_id/5615/) </br>

Original [PhysX used X87 instructions](https://www.geeks3d.com/20100711/cpu-physx-x87-sse-and-physx-sdk-3-0/) after Nvidia purchasing the company, re-wrote the code for [CUDA & SSE](https://web.archive.org/web/20170719105146/http://physxinfo.com/news/3391/physx-x87-and-sse/) </br>
32-Bit PhysX is [Limited by CPU](https://hothardware.com/reviews/nvidia-sheds-light-on-lack-of-physx-cpu-optimizations) 32-Bit SSE instructions. </br>
The game was designed to require 2x GPU's with PhysX HIGH setting. </br>

intel Z790 i3-12100 CPU is Twice faster in 32-Bit vs. AMD 7600x + X670E, using Rebirth 338 v2.1 Benchmark,</br>
Server boards have more PCIe lanes, but CPU's are slower, GPU's improve with faster CPU. </br>

problem of gamer boards & CPU's using 2x GPU's is that have very little PCIe lanes [20 vs 24](https://www.cpu-monkey.com/en/compare_cpu-intel_core_i3_12100-vs-amd_ryzen_5_7600x) each GPU has 16x PCIe v3 = 32, </br>
some boards halve 8+8 PCIe lanes, others keep 16x + 4x </br> 
problem is the M.2 NVMe PCIe x4 v5 </br>
Linux allows to boot from USB3 10Gbps, could be an option. </br>
X670E UEFI v2.10 goes crazy if install more PCIe lanes than available, </br>
requires to remove the CR2032 battery to restore Defaults, Turn-On & wait a few minutes to auto-reconfigure again. </br>

removing 1x memory stick "A2" from a dual-channel: B2+A2 </br>
game fps becomes severe affected by Single Channel RAM, </br>
both XMP profile-1 ddr5-5600 </br>

PhysX HIGH problem is Not a 32-Bit only issue. </br>
GPU & CPU utilization is ~20% each </br>
NVIDIA GPUs are very affected by Single-Core CPU speed & single channel memory. </br>
Single-core tests: [2003](https://web.archive.org/web/*/http://http.maxon.net/pub/benchmarks/*), [R10](https://archive.org/download/cinebench_201907), [R11.5](https://www.cpu-monkey.com/en/cpu_benchmark-cinebench_r11.5_64bit_single_core), [R15](https://www.cpu-monkey.com/en/cpu_benchmark-cinebench_r15_single_core), [R20](https://www.cpu-monkey.com/en/cpu_benchmark-cinebench_r20_single_core), [R23](https://www.cpu-monkey.com/en/cpu_benchmark-cinebench_r23_single_core), [2024](https://www.cpu-monkey.com/en/cpu_benchmark-cinebench_2024_single_core) </br>

[Memtest86 Passmark version](https://www.memtest86.com/download.htm) </br>
[Memtest86+](https://github.com/memtest86plus/memtest86plus/releases) [precompiled binary](https://memtest.org/) </br>

[Comparison](https://forums.passmark.com/memtest86/53706-memtest86-v10-vs-memtest86-v6-comparison) </br>
[Ventoy](https://www.ventoy.net/en/download.html) </br>

------------------------------------

## Dual GPU PhysX on Linux

Nvidia propietary driver 470 detects Both GPU's NVIDIA X Control </br>
> /usr/bin/nvidia-settings 

but Linux driver does Not have PhysX option as Windows, to select 1x GPU for PhysX </br>
<img width="768" height="555" alt="2025-07-24_15-23-24" src="https://github.com/user-attachments/assets/1bf753b7-3c66-4cba-b496-6d981e10e8d8" />


> /usr/games/lutris

Detects both GPU's. </br>
but Dual GPU PhysX does Not work, 0% load on the 2nd GPU. </br>

Game recommends: </br>
[GTX 260 (2008)](https://www.techpowerup.com/gpu-specs/geforce-gtx-260.c217) + [9800 GTX (2008)](https://www.techpowerup.com/gpu-specs/geforce-9800-gtx.c207).[+(2009)](https://www.techpowerup.com/gpu-specs/geforce-9800-gtx.c237) similar [+3%](https://gpu.userbenchmark.com/Compare/Nvidia-GTX-260-vs-Nvidia-GeForce-9800-GTX/3160vsm8342) </br>
GTX 1050 Ti (2016) its 300% faster, </br>
M6000 24GB (2016-Q1) is 900% faster, but has severe frame drops in some parts of the game, with CPU PhysX HIGH </br>
IF game does Not detect 2x GPU with PhysX HIGH, falls back to 32-Bit CPU SSE instructions to emulate the 2nd GPU with CPU. </br>
Problem with CPU PhysX is that requires 1x Fast Single-core CPU, does Not have Multi-Threads, 1-Core has 100% CPU Load. </br>
<img width="1720" height="720" alt="PhysX CPU 100% Load" src="https://github.com/user-attachments/assets/73158c23-381e-4ef1-ba88-40f54d17b4a6" />

2011 fastest 4-core/8-thread intel CPU X5687 vs. i3-12100 (2022) is [+100%](https://gadgetversus.com/processor/intel-xeon-x5687-vs-intel-core-i3-12100/) ~ [+122%](https://technical.city/en/cpu/Xeon-X5687-vs-Core-i3-12100) but still has frame drops!</br>
2012 fastest 4-core AMD CPU [Opteron 6308 (2012)](https://www.techpowerup.com/cpu-specs/opteron-6308.c3731) & [8-core 6328](https://www.techpowerup.com/cpu-specs/opteron-6328.c3729) - [vs. 7600x](https://www.cpubenchmark.net/compare/1982vs5033vs4687vs4609/AMD-Opteron-6328-vs-AMD-Ryzen-5-7600X-vs-Intel-i3-12100-vs-Intel-i7-12700K), same, </br>
DDR3-1333 / 1600 vs. DDR5-5600 XMP1, same. </br>
PCIe v2 vs. PCIe v3 v4 v5 </br>
### ¿where is the problem? </br>
Cinebench [R10](https://archive.org/download/cinebench_201907) has 32-bit .exe & 64-Bit .exe </br>
[CPU-Z v2.16 .ZIP](https://www.cpuid.com/softwares/cpu-z.html) also has x32 & x64 .exe same strange result, x32 has lower score. </br>
Real Windows8.1x64: </br>
i3-12100 "Hyper-Threading Enabled."</br>
64-Bits vs. 32-Bits .exe has "37.58%" limit on single-core 32-bits.</br>
![i3-12100-vs-i7-7700k](https://github.com/user-attachments/assets/18618cec-c32e-412b-b18a-c6aaff4972c5)![cpu-zx32](https://github.com/user-attachments/assets/95628498-f41c-40b2-b67c-664ff236c2ed) </br>
7600x No-SMT "No-HyperThreading"</br>
64-Bits vs. 32-Bits .exe has "26.08%" limit on single-core 32-bits.</br>
![7600x-NoSMT-x64](https://github.com/user-attachments/assets/a44dc51e-1779-4813-83df-3fe53bdda2d0)![7600x-NoSMT-x32](https://github.com/user-attachments/assets/d9084ee4-4b9b-40f8-810d-e20356aed869) </br>
7600x SMT "HyperThreading=On"</br>
64-Bits vs. 32-Bits .exe has "26.27%" limit on single-core 32-bits.</br>
![7600x-SMT-x64](https://github.com/user-attachments/assets/c0c25a49-72af-40f2-a101-121b86aa9973)![7600x-SMT-x32](https://github.com/user-attachments/assets/f53dcbd3-55ec-4969-a945-af2e75910962) </br>

#### CPU-Z "Vintage" No 64-Bit ver. 1.04.0.w9x
![Screenshot_20251214_150818](https://github.com/user-attachments/assets/ec440872-bfdf-4160-bfb5-b5f6fef8e1e3)

-----------------------

32-Bit Cinebench [R10](https://archive.org/download/cinebench_201907) .exe gives ~60% of the 64-bit result, does Not matter CPU brand or Wine version or OS. </br>
Linux or Win8.1x64 has a ~60% CPU limit on 32-Bit Cinebench [R10](https://archive.org/download/cinebench_201907) </br>
other people also have [Strange Results](https://commons.m.wikimedia.org/wiki/File:Cinebench_R10_%E2%80%93_Benchmark_Intel_Core_i9-9900K,_Gigabyte_GeForce_RTX%E2%84%A2_3090_EAGLE_OC_24G_2024-04-03_08_24_34-Greenshot_CROP02.png) </br>
OpenGL No change, same result. </br>
Runing Cinebench [R10](https://archive.org/download/cinebench_201907) .exe on different Wine versions: [PlayOnLinux 4.3.4](https://www.playonlinux.com/script_files/PlayOnLinux/4.3.4/PlayOnLinux_4.3.4.deb) + POL Wine x32, x64, Lutris UMU Proton-GE 8.4 x64 </br>

Batman was released in 2009, requires DirectX 9 "from 2009", GOTY v1.1 requires VC 2015 </br>
Cinebench R10 released 5 April 2007 </br>
seems there is a problem with [Visual Studio 2005-2008](https://en.wikipedia.org/wiki/Visual_Studio#History) and error was minimized in later versions. </br>

Cinebench 2003 it´s pure 32-Bit, does Not have 32/64-Bit .exe </br>
there is No way to test if has "the problem", but Results seem consistent: </br>
older 2005 CPUs single-core give less than [<300 cb points](https://www.computerbase.de/news/prozessoren/idf-benchmarks-von-sossaman-und-yonah.14009/) </br>
2011 intel CPU´s overclocked to 6GHz with N2 & Dry Ice, single-core give less than [<1000 cb points](https://hwbot.org/benchmarks/cinebench_-_2003/submissions/3355052) </br>
2011 AMD CPU´s, Top of the line Opteron 63xx stock speed give less than [<500 cb points](https://hwbot.org/benchmarks/cinebench_-_2003/submissions/3923229) </br>
2020-2022 Low-end CPU´s i3-12100 & 7600x give 1200-1500 cb points single-core, stock. </br>
7700x gives [1333 cb points](https://hwbot.org/benchmarks/cinebench_-_2003/submissions/5252595) </br>
9800X3D at 6GHz gives: [1474 cb points](https://hwbot.org/benchmarks/cinebench_-_2003/submissions/5816111) </br>
12900K at 5.3GHz gives: [1864 cb points](https://hwbot.org/benchmarks/cinebench_-_2003/submissions/4979175) </br> 
Ultra 9 285K 5.5Ghz gives [2171 cb points](https://hwbot.org/benchmarks/cinebench_-_2003/submissions/5791499) </br>

is 285K single-core enough to emulate a GPU? 1000 shaders, 100 TMU, 100 SMX? </br>
probably Not. </br>
Old Voodoo GPU´s from 1990-2000 can be emulated using PCem & 86Box, but modern GPU´s are far more complex. </br>

Original game DVD (2009) v1.0 requires MS Live account instead of EAapp to save the game, has PhysX v9.04, if install v12 on POL breaks the system, </br>
does Not have PhysX menu like v1.1, Default: Disabled, No PhysX. </br>
64-Bit POL Wine 4.0.4, PhysX Needs installing v1.1 update </br>
Win8.1x64 Requires [xlib.dll 3.5.88.0](https://www.dll-files.com/xlive.dll.html) in: </br>
C:\Windows\System32 </br>
C:\Program Files (x86)\Eidos\Batman Arkham Asylum\Binaries </br>
Update v1.1 adds PhysX menu in BmLauncher.exe </br>
also installs PhysX v9.09, but v9.09 does Not work in Win8.1x64, requires Newer. </br>
Links: </br>
[1](https://www.gamepressure.com/download/batman-arkham-asylum-v11-eng-patch/z3625f).[2](https://www.moddb.com/games/batman-arkham-asylum/downloads/patch-1-1-11).[3](https://www.patches-scrolls.com/batman_arkham_asylum.php).[3a](https://www.patches-scrolls.com/dl.php?file=batmanaa_gtx480and470_physx_patch.zip).[3b](https://www.patches-scrolls.com/dl.php?file=batman_tu_v1.1_efigs.zip).[4](https://en.ds-servers.com/gf/batman-arkham-asylum/official-patches/batman-arkham-asylum-v1-1-patch.html).[5](https://www.nexusmods.com/batmanarkhamasylum/mods/16).[6](https://www.nexusmods.com/batmanarkhamasylum/mods/16).[]().[]().[]() </br>

````
Physx disabled in Batman Arkham Asylum v1.0 by Default
How to Enable Batman Arkham Asylum Physx
Solution : (posted on filenetworks)
v1.0 PhysX is missing from the BmLauncher.exe Configuration menu.

1. Browse to directory C:\Users\YOURNAME\Documents\Eidos\Batman Arkham Asylum\BmGameConfig
2. Open UserEngine.ini file with a text editor.
3. Change the line PhysXLevel=0 so that it reads
PhysXLevel=1 "NORMAL"
PhysXLevel=2 "HIGH"
*do Not include "Normal" / "High"
4. Save & close. Run the game
````

-----------------------------------

Cinebench [R11.5](https://archive.org/download/cinebench_201907) results: </br>
Proton-GE 8.4 is 86% vs. POL 4.3.4 + Wine v6.17 64-Bit, All tests OpenGL & CPU single & multi. </br>
Real Win8.1x64 is ~88% avg. 32-Bit vs. 64-Bit. single-core 87.7%, multi 88.5%, OpenGL very similar Result almost "No change." </br>

R11.zip can only be extracted with Xarchive, Ark gives Error on Linux. </br>
better download [R11.529.zip](https://web.archive.org/web/*/http://http.maxon.net/pub/benchmarks/*) </br>

Proton-GE has much higher OpenGL score vs. standard POL Wine versions. </br>
because POL Wine sometimes has Vsync Activated, Proton-Ge does Not by Default, maybe winetricks can solve that. </br>

Cinebench 2003 does Not have 64-Bit & 32-Bit .exe but Proton is a bit faster. </br>

![Screenshot_20250714_095125](https://github.com/user-attachments/assets/db8fe8d3-abf0-4f42-af20-9bce559308a9) </br>
havent tested [POL5](https://github.com/PhoenicisOrg/phoenicis) </br>
[4.4-src](https://github.com/PlayOnLinux/POL-POM-4/releases) </br>
POL [Wine-9.0 x86](https://www.playonlinux.com/wine/binaries/phoenicis/upstream-linux-x86/) & POL [Wine-6.17 x64](https://www.playonlinux.com/wine/binaries/phoenicis/upstream-linux-amd64/) </br> 

![Screenshot_20250711_181300](https://github.com/user-attachments/assets/af6c3f81-29a7-48d5-80b7-832b75e6541a) </br>
![Screenshot_20250711_181232](https://github.com/user-attachments/assets/10869173-d961-47df-ad51-fbdfd5a907f0) </br>

Lutris -> UWU -> Wine-ge-8.x -> EA app.exe -> Batman Arkham Asylum -> NVIDIA PhysX 9.14 by Default. </br>
Works ok with 1x GPU. </br>
but Dual GPU does Not. </br>

Lutris cannot be Run in Sudo. </br>
PhysX 9.14 cannot be Uninstalled, but New installer can Override, </br>
installing older Legacy PhysX 9.12 at same time, with Wine Control Panel inside Lutris </br>
Batman does Not work. </br>
![Screenshot_20250711_201123](https://github.com/user-attachments/assets/fa8e3a01-ade9-42af-8d74-c90f81004d95) </br>
![Screenshot_20250711_202119](https://github.com/user-attachments/assets/454e3b6f-9e11-45d2-9a41-e46f3f55d4e6) </br>
installing PhysX as another program, creates an individual dos_c drive, isolated from Batman dos_c drive. </br>

Lutris has a nice GUI, easy to navigate / easy to use, more minimalistic vs. PlayOnLinux 4.3.4 </br>

Lutris allows other "Runners" / versions of Wine, Proton, similar vs. PlayOnLinux </br>
![Screenshot_20250711_110606](https://github.com/user-attachments/assets/4bb96c3e-f8b5-4137-b0f2-6f6d790cbe48) </br>

![Screenshot_20250711_213528](https://github.com/user-attachments/assets/5f6a7d88-ee4f-4485-9503-5a8f2462d933) </br>
![Screenshot_20250711_210020](https://github.com/user-attachments/assets/651d8ce3-e4cc-4807-a2d1-3d4f92b3d0ed) </br>
![Screenshot_20250711_210128](https://github.com/user-attachments/assets/11863cf8-4012-4946-97da-230616733a58) </br>

![Screenshot_20250711_210012](https://github.com/user-attachments/assets/d2ef9c43-ebcb-40e7-83af-148e2f408cd5) </br>
![Screenshot_20250711_205917](https://github.com/user-attachments/assets/618080da-36a6-4cd9-91a9-1d7d9f556dcf) </br>
![Screenshot_20250711_205907](https://github.com/user-attachments/assets/7ea8e940-1125-4486-bdc3-be6ded2663ac) </br>

![Screenshot_20250711_104809](https://github.com/user-attachments/assets/642bca46-41bb-4dee-8cc1-4ff5c957d5d4) </br>
![Screenshot_20250709_143214](https://github.com/user-attachments/assets/a1f46185-d66d-4eb0-bd11-85f8dd520c86) </br>

--------------------------

Wine vs. [Proton vs. Proton-GE](https://www.reddit.com/r/SteamDeck/comments/wkx8v9/proton_vs_proton_ge_va_experimental/) </br>

[what version of Proton?](https://www.gamingonlinux.com/guides/view/why-are-there-so-many-different-proton-versions-proton-8-proton-9-experimental-ge-proton/) </br>

[Releases](https://github.com/GloriousEggroll/proton-ge-custom/releases) </br>

---------------------------
