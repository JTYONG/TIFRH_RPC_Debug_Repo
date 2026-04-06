# TIFRH_RPC_Debug_Repo
Ongoing debuging code to setup a simulation for TIFRH RPC.


## Nebem_FieldPlot_Test
This code is used to extract the electric field computed by the `ComponentNebem3D` at sample points in the gas gap region. 

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
