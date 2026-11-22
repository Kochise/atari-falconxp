# FalconXP Player

Atari application interpreter that runs in the background. Allow to execute them like native applications.

Applications are run as fast as the host can, emulating different CPU (68000 to 68060, FPU and DSP) yet with no cycle accuracy at all.

Drive letters are mapped to host drives or folders. Drag and drop, copy and paste work between host system and interpreted applications.

Hardware accesses may cause the interpreter to crash, don't try running drivers and ST games.

| **EMUL**			| [FalconXP]	|
| :--				| :-:			|
| **Version**		| 4.04			|
| **Date**			| 2023/03/08	|
| **Release mouse**	| (borders)		|
| **Screenshot**	| (host)		|
| **Fullscreen**	| (host)		|
| **Main menu**		| (Tray menu)	|
| **Pause**			| 				|
| **Debug**			| 				|
| **(Cold) Reset**	| 				|
| **Help**			| F11			|
| **Undo**			| F12			|
| **Border**		| 				|
| **Sound**			| 				|
| **Quit**			| (Tray menu)	|

[FalconXP]: https://falcon.xp

**INST** :

* Launch

* A tray icon allows to access parameters and loaded accessories
* Standard Atari application extensions (see below) are registered

<details>
<summary>Application extensions: ACC/CPX, APP/PRG/GTP, TOS/TTP</summary>

```
ACC: ACCessory
CPX: Control Panel eXtension

APP: APPlication (GEM)
PRG: PRoGram (GEM)
GTP: Gem Taking Parameter (GEM)

TOS: Text Output to Screen (VT52)
TTP: Tos Taking Parameter (VT52)
```

</details>

* A few desktop icons are created as shortcuts to screen resolution (see below)

<details>
<summary>Screen resolution shortcuts: ST LOW/ST MED/ST HIGH, TT LOW/TT MED/TT HIGH, 256P/256C, 65K, 16M, 32B</summary>

```
ST LOW: 320x200, 16 colours out of 512(ST)/4096(STe), 4 bitplanes
ST MED: 640x200, 4 colours out of 512(ST)/4096(STe), 2 bitplanes
ST HIGH: 640x400, monochrome (black and white), 1 bitplane

TT LOW: 320x480, 256 colours out of 4096, 4 bitplanes
TT MED: 640x480, 16 colours out of 4096, 2 bitplanes
TT HIGH: 1280x960, monochrome (black and white), 1 bitplane

256P: 256 colours out of 262144, 8 bitplanes (planar)
256C: 256 colours out of 262144, chunky (1 byte per pixel)

65K: 65535 colours, 16 bits RGB (565)
16M: 16777216 colours, 24 bits RGB (888)
32B: 16777216 colours, 32 bits ARGB (8888)
```

</details>

* Double click on an Atari application to run it through the interpreter using default settings

ACC and CPX are added to the tray icon

* Drag an Atari application to a screen resolution shortcut to run it in the desired colour mode
* Drag a disk image (see below) to a screen resolution shortcut to open it in the desired colour mode

<details>
<summary>Disk image format: ST, IMA/IMG/DSK, MSA, IMD/DIM, BIN/STC (cartridge), STX, IPF/CTR, RAW/SCP/HFE, STT/STG/STW</summary>

```
ST: created originally for the PacifiST emulator

IMG: created by the Copy II PC Option board (generic suffixes for IBM FM/MFM raw sectors)

MSA: created by the compression program Magic Shadow Archiver

IMD: ImageDisk image (IBM sectors)
DIM: created by the well-known Atari copy program "FastCopy Pro"

STX: created by the PASTI initiative (Atari ST Imaging & Preservation Tools)

IPF: created by the Software Preservation Society (universal 'golden image' format)
CTR: created by the Software Preservation Society

RAW created by the KryoFLux board (raw bitcells, 1 revolution per track)
SCP: created by the SuperCard Pro board (raw flux, multiple revolutions per track)
HFE: created by the HxC Floppy Emulator (HxC2001.com project)

STT: created for Steem Engine emulator
STG: ST Gost format, created for Steem SSE
STW: ST Write format, created for Steem SSE
```

</details>

* Double click on an Atari picture (see below) to display it through the interpreter using default settings
* Drag an Atari picture (see below) to a screen resolution shortcut to display it in the desired colour mode

<details>
<summary>Atari picture format: ANM, CE1/CE2/CE3, GEM/IMG/XIMG, FLM, NEO/ANI, PAC, PC1/PC2/PC3/PI1/PI2/PI3, RGB, SEQ, TNY/TN1/TN2/TN3, UC1/UC2/UC3</summary>

```
CE1/CE2/CE3: ComputerEyes
GEM/IMG/XIMG: GEM and VDI native
FLM: Animatic Film
NEO/ANI: NEOchrome
PAC: STAD
PC1/PC2/PC3/PI1/PI2/PI3: Degas Elite
RGB: RGB intermediate
SEQ: Cyber Paint Sequence
TNY/TN1/TN2/TN3: Tiny
UC1/UC2/UC3: Imagic
```

</details>

Typically the last digit means '1' for ST LOW, '2' for ST MED and '3' for ST HIGH.

The `Player` version cannot create disk image and debug application.
