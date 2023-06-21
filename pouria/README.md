# Fachprojekt "Routing Algorithms"
## Dependencies and assumptions
It will be assumed that the person interested in the project already has a working and running version of the base project, including the gurobi license and a correctly running anaconda instance. 
If not, please look up the instructions given in the **[README_base.md](README_base.md)**

## Install
To start working on this project, it is necessary to clone/download this repository.
The download location is not important.

## Running the project
To run the project, one has to (similarly to the base project) open up a terminal and enter the following commands:

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
cd FaPro_P2/pouria/
```
```bash
chmod +x *.py
chmod +x *.sh
```
```bash
./pouria.topo.sh
```
```bash
python3 nanonet_batch.py
```
To view the results as a box plot diagram, run the following command
```bash
python3 gen_boxplot.py
```
and open up **[batch_result001.pdf](batch_result001.pdf)**

*Note: When looking at the .csv or .pdf, the results all seem to be identical. The cause of this might be the 2 minute timeout when running the script. It seems that my computer aborts the calculation when reaching the time limit. This might not happen for you, if your computer has sufficient processing power.*

### Additional options/flags
To reduce the overall computation time, flags are introduced.
The code can be run with multiple options.
These are given by flags that are always at the top of each python file.
```bash
nanonet_batch.py
bool all_tests = False  // just pouria.topo will be run
bool all_tests = True   // all topos will be run
```
By default, the boolean is set to **False**.
If set to **True**, all topos will be run.
This will drastically increase the computation time.
```bash
nanonet_batch.py
int num_of_tests = 5
```
Please keep in mind that the overall computation time is 
```bash
num_of_tests * test_cases * 8 minutes
```
So, if **num_of_tests = 5** and **all_tests = True**, the overall compututation time is 5x3x8 >= 120 minutes

## Additional information
The file **[network_origin.pdf](network_origin.pdf)** contains additional information about the network and the demands within that network.