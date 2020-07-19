# The OSVVM Model Library
The Open Source VHDL Verification Methodology (OSVVM) model library is a growing set of models 
commonly used for FPGA and ASIC verification. 
This library uses the  [OSVVM utility library](https://github.com/OSVVM/OSVVM). 

This respository, **VerificationIP**, includes all of the OSVVM model library as submodules.
Download the entire OSVVM model library using git clone with the "--recursive" flag:  
    `git clone --recursive https://github.com/OSVVM/VerificationIP.git`

Note that submodules are not included in the GitHub zip files.

## About OSVVM
[OSVVM](https://OSVVM.github.io) provides 
[utility](https://github.com/OSVVM/OSVVM) and model libraries that simplify 
your FPGA and ASIC verification tasks.
Using these libraries you can create a simple, readable, and 
powerful testbench that is suitable for either a simple FPGA block
or a complex ASIC.

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

## Copyright and License
Copyright (C) 2006-2020 by [SynthWorks Design Inc.](http://www.synthworks.com/)   
Copyright (C) 2020 by [OSVVM contributors](CONTRIBUTOR.md)   

This file is part of OSVVM.

    Licensed under Apache License, Version 2.0 (the "License")
    You may not use this file except in compliance with the License.
    You may obtain a copy of the License at

  [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
