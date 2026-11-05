# How to Use This Repo
Run: git clone https://github.com/tejusk2/PowerPCB.git  

git pull to get current changes \n
git checkout -b <branch_name> to create a new branch \n
git push origin <branch name> to push your branch to origin \n
- pushing may require some setup of https or ssh tokens, ask AI how to do this \n
## Repository Structure

```text
├── Protection.kicad_pro       # Master KiCad project definition
├── Protection.kicad_sch       # Schematic (hierarchical symbols embedded)
├── Protection.kicad_pcb       # PCB layout and routing
├── ProtLibrary.kicad_sym      # Project-specific custom symbol definitions
├── protfootprints.pretty/     # Project-specific custom footprint modules (*.kicad_mod)
├── sym-lib-table              # Relative symbol library mapping table
├── fp-lib-table               # Relative footprint library mapping table
├── .gitignore                 # Excludes caches, lock files, and local UI state
└── README.md
```
Keep the file structure shown above, the repository should only and always have these files. \n
If you import an external symbol or footprint, add it to the project specific library. \n
Check the sym-lib-table and fp-lib-table to make sure that you don't have an absolute path to the library, It should look like: \n
Symbols: ${KIPRJMOD}/ProtLibrary.kicad_sym \n
Footprints: ${KIPRJMOD}/protfootprints.pretty \n

Verify gitignore is active, and never push lck files or prl files. \n
When making a PR, make sure all electrical rules and DRC are passed \n
