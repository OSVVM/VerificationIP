# Deprecated:  Please see [OSVVM Libraries](https://github.com/OSVVM/OsvvmLibraries)
Change is inevitable.   Sometimes sooner than expected.
The Verification IP repository has been replaced by the
OsvvmLibraries repository.   

See:  [OSVVM Libraries](https://github.com/OSVVM/OsvvmLibraries)

"Git" the entire OSVVM model library using git clone with the "--recursive" flag:  
    `git clone --recursive https://github.com/OSVVM/OsvvmLibraries.git`

# Verification IP Library
This repository is current through the 2020.07 release.

Why deprecate? 
With OsvvmLibraries includes the
OSVVM utility, documentation, scripts, and verification component repositories
as submodules.

The Verification IP library includes just the 
OSVVM scripts and verification component repositories
as submodules.  

It is easier to manage a single repository rather than 
having separate repositories.  

## About OSVVM
[OSVVM](https://OSVVM.github.io) provides 
[utility](https://github.com/OSVVM/OSVVM) and model libraries that simplify 
your FPGA and ASIC verification tasks.
Using these libraries you can create a simple, readable, and 
powerful testbench that is suitable for either a simple FPGA block
or a complex ASIC.

## Current Models - Submodules
 - [AXI4 Full](https://github.com/OSVVM/AXI4)
   - Master - includes burst support
   - Memory Responder model - includes burst support
   - Transaction Responder model - but it does not support bursts
 - [AXI4 Lite](https://github.com/OSVVM/AXI4)
   - Master
   - Transaction Responder model
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
Historically we called the models 
Bus Functional Models (BFM). - which in they are. 
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
