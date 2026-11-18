# Contributing to LV and DAQ

The short version of the README's "On Contributions", for this repo and every LV board repo.

1. **Fork** the repo on GitHub (name the fork `<yourname>-<repo>`), open it in GitHub Desktop, clone with submodules.
2. **Branch** in your fork, commit often, push to your fork.
3. **Open a pull request** to `main` of the UAlbertaFSAE repo, then **message Ashwin or Duru with the link**. Do not
   push or merge into the org repo yourself; the review is recorded on the PR.
4. **CI** (board repos) runs ERC and DRC on the PR. Fix errors before review; warnings are in the report artifact.
5. **Labels:** `sub:lv` / `sub:daq`, a `type:` label, and `harness-impact` when a harness connector, pinout or net
   name changes (net names follow C-06, see the library's
   [DESIGN_RULES.md](https://github.com/UAlbertaFSAE/UA_KICAD_LIB/blob/main/DESIGN_RULES.md)).
6. **Releases:** after review, the board owner tags `main` as `V<n>-<rev>` (e.g. `V1-AA`, two-letter PDM revision);
   CI attaches gerbers, drill, schematic PDF, BOM and placement to a GitHub Release.

## Where things are

| What | Where |
| --- | --- |
| Every LV board | `boards/<repo>` (submodules; `git clone --recurse-submodules`) |
| Shared KiCad library and design rules | `lib/UA_KICAD_LIB` |
| New board | create from [UA_BOARD_TEMPLATE](https://github.com/UAlbertaFSAE/UA_BOARD_TEMPLATE), or open a "New board" issue |
| Work tracking | the org Project "LV & DAQ" |
| Big files | no Git LFS; STEP and fab exports go on Releases, files over 50 MB on the shared drive |
