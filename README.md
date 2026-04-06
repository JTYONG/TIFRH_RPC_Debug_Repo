# TIFRH_RPC_Debug_Repo
Ongoing debuging code to setup a simulation for TIFRH RPC.


## Nebem_FieldPlot_Test
This code is used to extract the electric field computed by the `ComponentNebem3D` at sample points in the gas gap region. 

There are currently two files in the directory:
1. `Nebem_FieldPlot.C` - Initialize `ComponentNebem3D`, sample field points, compute and write to `Nebem_FieldPlot.root` file. Creates the contour plot.
2. `Read_NebemPlot.cpp` - Read `Nebem_FieldPlot.root` and create TH2D and TH3D of the fields, saved to `Plot_Nebem_FieldPlot.root`

To execute the  `Nebem_FieldPlot.C`:
1. Enter the `build` directory.
```bash
cd build
```
2. execute the below command in bash terminal:
```bash
# remove all files in the build directory.
rm -rf *

# use cmake to compile the cpp script into executable file
cmake .. && make -j16
```
3. execute the executable.
```bash
./Nebem_FieldPlot
```

To read the root file:
1. From `\build`, move to generated .root file to the home directory (`\Nebem_FieldPlot_Test`)
```bash
mv *.root .. 
```
2. execute command below:
```bash
root

.x Read_NebemPlot.cpp("Nebem_FieldPlot.root")
```
