# Fachprojekt "Routing Algorithms"
## Structure
Each subfolder contains the algorithmic idea of each project member.

## Workflow
To work on a project, just clone the git repository. 
Once cloned, you can go into each subfolder and work on/test it.

```bash
conda activate wan_sr
```
The conda environment seems to have all necessary packages and modules, so no further installations are needed.
From here, you have to delete the following files/folders (via the command line or in file browser).
* the *.topo.sh folders
* the *.throughput.json files
* batch_result*.csv
* the flow_*.txt files

To run the project, you have to (similarrly to the base project) open up a terminal emulator and enter the following commands.
```bash
cd FaPro_P2/<projectFolder>/
```
```bash
chmod +x *.py
chmod +x *.sh
```
```bash
./<testcase.topo.sh>
```
```bash
python3 nanonet_batch.py
```
## Presentation
The final presentation will be located in the **/latex/** subdirectory under the name fapro_p2.pdf.