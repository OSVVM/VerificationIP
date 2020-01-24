# The OSVVM Model Library
The OSVVM model library is a growing set of models 
commonly used for FPGA and ASIC verification.  

This respsitory, **VerificationIP**, includes all of the OSVVM model library as submodules.
Download the entire OSVVM model library using git clone with the "--recursive" flag:  
    `git clone --recursive https://github.com/OSVVM/VerificationIP.git`

Note that submodules are not included in the GitHub zip files.

## Current Models - Submodules
 - [AXI4 Lite](https://github.com/OSVVM/AXI4)
   - Master
   - Slave transactor model
 - [AXI Stream](https://github.com/OSVVM/AXI4)
   - Master
   - Slave
 - [UART](https://github.com/OSVVM/AXI4)
   - Transmitter (aka master) - with error injection
   - Receiver (aka slave) - with error injection
 - [OSVVM Common - Required](https://github.com/OSVVM/OSVVM-Common)
   - Shared transcript interfaces
 - [OSVVM Scripts](https://github.com/OSVVM/OSVVM-Scripts)
   - Recommended.  Script layer on top of tcl
   - Common simulator compilation and execution methodology


## Models vs TBM vs VVC vs BFM 
We use the word models as short hand for 
Transaction Based Models (TBM). 
They are simply an entity and architecture coded in 
an effective manner for verification.
Some use other terminology such as 
VHDL verification components (VVC) - 
these are the same thing.
Historically we used Bus Functional Models (BFM). 
However, recently we abandoned BFM due to others using BFM to 
refer to their own lesser capable subprogram based approach.

## OSVVM Interfaces 
OSVVM models use records for the transaction interfaces, 
so connecting them to your testbench is simple - 
connect only a single signal.

Currently this methodology requires that the records 
use element types with resolution functions. 
See the OSVVM Utility library package, 
ResolutionPkg.vhd.  

When VHDL-2019 is implemented, we plan to 
transition to the new interface feature.
This feature is also based on records and for OSVVM only requires the addition of a mode 
view declaration in the package and an update to the model port declarations.

## Model Testbenches are Included 

Testbenches are in the Git repository, so you can 
run a simulation and see a live example 
of how to use the models.
