# VerificationIP
OSVVM Verification IP  (aka Verification Components, Transaction Level Models, ...) 

## Downloading

By cloning this repository, you download the latest version of all listed OSVVM-style Verification IPs.

```bash
git clone --recursive https://github.com/OSVVM/VerificationIP.git
```

## Dependencies
### External Dependencies
  * VHDL-2008 (see list of [supported simulators](#supported-simulators) below)
  * [OSVVM Library](https://github.com/OSVVM/OSVVM)
  
### Embedded Dependencies (Git Submodules)
* [OSVVM Scripts](https://github.com/OSVVM/OSVVM-Scripts)
* [Common Files](https://github.com/OSVVM/osvvm_vip)

### Intra IC Bus Protocols:
* AMBA - Advanced Microcontroller Bus Architecture
  * [AXI - Advanced eXtensible Interface Bus](https://github.com/OSVVM/AXI4)
    * AXI4 (planned)
    * AXI4-Lite
    * AXI4-Stream
* WB - Wishbone (planned)

### External Low-Speed Protocols
* [UART - Universal Asynchronous Receiver Transmitter](https://github.com/OSVVM/UART)
* I²C (planned)
* SPI (planned)

## Supported Simulators
* ModelSim, QuestaSim
* Active-HDL, Riviera-PRO
* [GHDL](https://github.com/GHDL/GHDL)


## License

Licensed under [Apache License 2.0](LICENSE.md).
