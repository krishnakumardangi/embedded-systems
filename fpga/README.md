# FPGA (Field-Programmable Gate Array)
Software Setup and Usage

We have three big "parts" of software that we use in 6.205. You need access to all three of them and should go through the installation steps below for each:

- [GTKWave/iVerilog](https://fpga.mit.edu/6205/F23/documentation/iVerilog): The open-source software we use to simulate and test our digital designs!
- [Vivado](https://fpga.mit.edu/6205/F23/documentation/vivado): The propietary software we use to generate our digital designs!
- [openFPGAloader](https://fpga.mit.edu/6205/F23/documentation/openFPGA): An open-source cross-platform bit-file flasher which we use to get our designs on our FPGA!

We also have a growing collection of Windows tips.

Quick Command Reference

These commands contain the arguments that work in most use cases - every once in a while you'll need to modify them slightly, but these are their most common forms:

- Building a project:
    * With lab-bc (remote): ``./remote/r.py build.py build.tcl {whatever files you need to include}``
    * Locally: ``vivado -mode batch -source build.tcl``
- Flashing the FPGA: ``openFPGALoader -b arty_s7_50 out.bit``
- Simulating a testbench:
    * ``iverilog -g2012 -o foo.out sim/foo_tb.sv src/foo.sv`` followed by ``vvp foo.out``
    * Add all the files that iVerilog should be aware of to the command line args. For instance, if your testbench foo_tb makes an instance of foo and foo contains an instance of bar, then you'll need to add the files that contain foo and bar to the command line args.
- Opening GTKWave:
    * Windows/Linux: ``gtkwave foo.vcd``
    * macOS: ``open foo.vcd``
    * Remember that you don't need to close your GTKWave window and reopen it after every simulation! It's way faster to reload the waveform inside your existing window.

SystemVerilog Standard 2017

- [2017 SystemVerilog Standard](https://fpga.mit.edu/6205/_static/F23/documentation/1800-2017.pdf)

External Hardware and IP Cores

- [Camera Board software](https://fpga.mit.edu/6205/F23/documentation/ov7670)
- [DRAM (for reference from the Nexys boards...we are currently working on something for the Urbana board)](https://fpga.mit.edu/6205/F23/documentation/dram)
- [Starter Designs (kind of janky). These were all developed for the Nexys board, but can at least get you started. Reach out Piazza for particular things like some modifications for the SD card)](https://github.mit.edu/6205/starter_designs)
- [How to Debug](https://fpga.mit.edu/6205/F23/documentation/debugging)

Verilog References

- [Verilog Style Guide](https://fpga.mit.edu/6205/F23/documentation/verilog_style)

IP Simulation

- [Quick notes on how to simulate IP](https://fpga.mit.edu/6205/F23/documentation/ip_simulation)

