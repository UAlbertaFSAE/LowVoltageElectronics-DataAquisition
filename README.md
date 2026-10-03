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

# Suggested workflow

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
| KiCAD Library | FSAE KiCAD library to standardize PCB builds | [0.0] | [link coming soon] |
| X | X | [x.y.z] | [link] |
| X | X | [x.y.z] | [link] |
| X | X | [x.y.z] | [link] |



## Documents

Reference material for the LV and DAQ systems.

- **XX:** [Link or path]

---

## Links

- **Shared drive:** [https://drive.google.com/drive/u/0/home]
- **LV Master Project Tracker:** [https://docs.google.com/spreadsheets/d/1VbT29XEA2qAB6c5AbIkguSezSsc0WxWq/edit?gid=221281115#gid=221281115]

---
