# fc-emulator-rs
Rust FC (Famicom/NES) Emulator

## Project Description

This project is a practice emulator, starting with the classic Famicom (FC) console, following the step-by-step guides in [this Zhihu blog](https://www.zhihu.com/column/dustpg).

It is written in Rust and aims to implement a complete FC emulator, including the CPU, PPU, APU, mappers, etc., and ultimately run FC games.

## Test File Description

`nestest.nes` is a test ROM. Documentation: [nestest.txt](http://www.qmtpro.com/~nes/misc/nestest.txt)  
Note: The internal initial state of `0x4000 - 0x401F: APU and I/O registers` should be set to `0xFF`.

## Input Instructions

- `W`, `A`, `S`, `D`: Directional keys
- `J`, `K`: A and B buttons
- `Enter`: Start
- `Space`: Select

## Progress

- [x] Passes `nestest.nes` test ROM
  - [x] ROM loading and parsing
  - [x] CPU instruction decoding
  - [x] Basic/control CPU instruction emulation
  - [x] Extended CPU instruction emulation
- [ ] Multithreading
  - [x] Naive implementation
  - [ ] Pipeline naming cleanup
- [ ] PPU (Picture Processing Unit)
  - [ ] Test ROM passing
  - [ ] Interrupt interaction
  - [ ] Background rendering
    - [x] Naive rendering
  - [ ] Sprite rendering
    - [x] OAM DMA implementation
- [ ] Clock synchronization
  - [ ] PPU NMI sync
  - [ ] PPU line sync
  - [ ] CPU instruction delay
  - [ ] APU (Audio) emulation
- [ ] Input
  - [x] Keyboard input
  - [ ] Controller input
  - [ ] Dual-controller simulation
  - [x] Single-controller simulation
- [ ] TAS simulation
- [ ] Super-resolution
- [ ] Multi-platform support
- [ ] Performance optimization
