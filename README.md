# UAlberta FSAE Low Voltage & Data Acquisition

Repository for our Formula SAE team's Low Voltage (LV) and Data Acquisition (DAQ) work. It holds the shared data, code, and documentation.

---
### Installation

Install GitHub Desktop [https://desktop.github.com/download/] 
If you forget to pull, you won't see updated information. 
Start off with pulling and syncing your repo and checking the repo log online. 
Nothing is lost on git. We can always restore older versions as long as you regularly push. 
You don't need to learn the terminal commands, GitHub Desktop has buttons for everything. 

---

## On Contributions:

1. **Fork this repository.** Don't work directly in this repo. Fork it and use the data we've posted here in your own copy.
2. **Pushes and merges need approval.** Direct pushes and merges to this repository are not permitted without sign-off. Please message **Ashwin** or **Duru** to push to this repo.
3. **Report anything broken** (bad data, failing scripts, dead links, errors in docs) to **Ashwin** or **Duru**.

## Suggested workflow

### 1. Fork the repo on GitHub, then clone your fork. 
Do not clone the original repo. First, find the 'fork' button on the top right. It's between 'watch' and 'star'. 
Edit the name of the fork and add your name in the beginning. This will help you distinguish the fork and the upstream repo. 
When the main page of the fork opens, click on the green 'code' button and choose 'open with GitHub Desktop'. 
On GitHub Desktop it will ask you for a local path. Press 'clone repo'. This is the local alias for your repo. 

### 2. Track the original repo to pull in updates
Simply click 'fetch origin' on GitHub Desktop. 

You can also do this in the terminal:
``` bash
git remote add upstream https://github.com/<team-org>/<repo-name>.git
git fetch upstream
git merge upstream/main
```
### 3. Work and commit in your fork
``` bash
git checkout -b my-feature
git add .
git commit -m "Describe what you did in this update"
git push origin my-feature
```
If you do this often, especially before and after major changes, we will never lose your work. It will also 
never be hard to restore your previous work if anything breaks. 

When you have changes that should go into this repo, message admin rather than opening a merge yourself.

---

## Libraries

Software libraries and tools used across LV and DAQ work.

| Library / Tool | Purpose | Version | Link |
| -------------- | ------- | ------- | ---- |
| KiCAD Library | FSAE KiCAD library to standardize PCB builds: symbols, footprints, 3D models, design blocks, and the shared [design rules](https://github.com/UAlbertaFSAE/UA_KICAD_LIB/blob/main/DESIGN_RULES.md). | [0.1] | [UA_KICAD_LIB](https://github.com/UAlbertaFSAE/UA_KICAD_LIB) (private; also at `lib/UA_KICAD_LIB`) |
| KiCAD Netlist | Netlist to send to KiCAD checker later. It describes which component pins are connected to which nets. | v0.1 | [link](nets.realnets.csv) |
| Harness tooling | UA-27 LV harness design tools (`hk.py`): reads the board repos read-only to check connector pins and net names against the harness | - | [ashwin-conrad/harness-template](https://github.com/ashwin-conrad/harness-template) (private, personal; ask Ashwin) |
| X | X | [x.y.z] | [link] |



## Boards

Each PCB keeps its own repository; this repo links them as git submodules under `boards/` (pinned to a commit), plus
the shared library under `lib/`. Nothing moved: work in the board repos as before. Board repos are private; you need
org access to open them.

Clone everything at once: `git clone --recurse-submodules https://github.com/UAlbertaFSAE/LowVoltageElectronics-DataAquisition.git`
(GitHub Desktop fetches submodules on clone). Update the pinned boards later: `git submodule update --remote`.

| Group | Board repo | KiCad project | Status |
| --- | --- | --- | --- |
| Control and computing | [UA_VCU_V04](https://github.com/UAlbertaFSAE/UA_VCU_V04) | `TeensyECU_V04` (vehicle control unit) | design |
|  | [UA_LV_COMPUTER_V1](https://github.com/UAlbertaFSAE/UA_LV_COMPUTER_V1) | `UA_LV_COMPUTER_V1` | template, empty |
|  | [UA_DL_HMI_V1](https://github.com/UAlbertaFSAE/UA_DL_HMI_V1) | `UA_DL_HMI_V1` | template, empty |
| Power | [UA_PDM_V1_TM](https://github.com/UAlbertaFSAE/UA_PDM_V1_TM) | `UA_PDM_V1_TM` (power distribution module) | template, empty |
|  | [UA_CAN_RELAY_V1](https://github.com/UAlbertaFSAE/UA_CAN_RELAY_V1) | `UA_Front_PDM_V1` (front PDM) | design (PCB empty) |
|  | [UA_LV_BMS_V1_JW](https://github.com/UAlbertaFSAE/UA_LV_BMS_V1_JW) | `UA_LV_BMS_V1_JW` (LV BMS) | template, empty |
| DAQ and sensors | [UA_DAQ_TEENSYDLU](https://github.com/UAlbertaFSAE/UA_DAQ_TEENSYDLU) | `TeensyDLU_V01` (data logger) | design |
|  | [UA_STRAIN_DAQ_V1_DP](https://github.com/UAlbertaFSAE/UA_STRAIN_DAQ_V1_DP) | `UA_STRAIN_DAQ_V1_DP` | template, empty |
|  | [UA_GNSS_IMU_V1_DV](https://github.com/UAlbertaFSAE/UA_GNSS_IMU_V1_DV) | `UA_GNSS_IMU_V1_DV` | template, empty |
| Communication | [UA_CAN_USB_V1_NK](https://github.com/UAlbertaFSAE/UA_CAN_USB_V1_NK) | `hardware/fsae-devboard` (CAN-USB) | design |
|  | [UA_TEL_USB_V1_AY](https://github.com/UAlbertaFSAE/UA_TEL_USB_V1_AY) | `UA_TEL_USB_V1_AY` (telemetry) | template, empty |
| Autonomous interface | [UA_AUTO_STEER_V1_DP](https://github.com/UAlbertaFSAE/UA_AUTO_STEER_V1_DP) | `UA_AUTO_STEER_V1_DP` | template, empty |
| Function to confirm | [UA_ACC_V1_KD](https://github.com/UAlbertaFSAE/UA_ACC_V1_KD) | `UA_ACC_V1_KD` | template, empty |
|  | [UA_DC_V1](https://github.com/UAlbertaFSAE/UA_DC_V1) | `UA_DC_V1` | template, empty |

All 14 boards are in `boards/<repo>`. Boards marked "template, empty" got their first commit from
[UA_BOARD_TEMPLATE](https://github.com/UAlbertaFSAE/UA_BOARD_TEMPLATE) (KiCad project skeleton, library submodule,
ERC/DRC CI); their owners start the design there.

New boards: create the repo from [UA_BOARD_TEMPLATE](https://github.com/UAlbertaFSAE/UA_BOARD_TEMPLATE)
(**Use this template**), then follow the [design rules](https://github.com/UAlbertaFSAE/UA_KICAD_LIB/blob/main/DESIGN_RULES.md) and add
the library as a submodule (`lib/UA_KICAD_LIB`, see its README).

## Documents

Reference material for the LV and DAQ systems.

- **XX:** [Link or path]

---

## Links

- **Shared drive:** [https://drive.google.com/drive/u/0/home]
- **LV Master Project Tracker:** [https://docs.google.com/spreadsheets/d/1VbT29XEA2qAB6c5AbIkguSezSsc0WxWq/edit?gid=221281115#gid=221281115]

---
