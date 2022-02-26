</br>

---

![logo](Images/logo.png)

---

</br>


![Size](https://img.shields.io/github/repo-size/Nalinkumar2002/barrel_shifter_snps_cc?color=red)
![Last Commit](https://img.shields.io/github/last-commit/Nalinkumar2002/barrel_shifter_snps_cc?color=green)
![license](https://img.shields.io/github/license/Nalinkumar2002/barrel_shifter_snps_cc?color=blue)

</br>

# 8x4 Right Barrel Shifter using NMOS Pass Transitor Logic



In this repository, It gives a detailed report on the design of a 8x4 Right Barrel Shifter using NMOS Pass Transistor logic using 28nm technology node. This design is implemented and simulated using **Synopsys Custom Design Compiler** for the event [_Cloud Based Analog IC Design Hackathon_](https://hackathoniith.in) conducted by the [Department of Electrical Engineering at IIT Hyderabad](https://ee.iith.ac.in), and sponsored by [Synopsys India](https://www.synopsys.com/company/contact-synopsys/office-locations/india/about-synopsys-india.html) and [VLSI System Design (VSD) Corp.](https://www.vlsisystemdesign.com) 

# Introduction

An Arithmetic logic unit (ALU) in a processor can performs various arithmetic operations and logical operations. Multiplication operation is done by multiplying of data using AND gate and addition of partial products using full adders or half adders. It also requires a shifter to shift partial products so that they can be added in correct format and can be validated. Hence these modules play an important role in characterizing the performance of processors. 

 Thereare different types of shifters like serial shifter, parallel shifterswhich shifts data based on clock cycle of microprocessor.They require n cycle to shift n-data bits. To overcome thisdisadvantage, Barrel shifters are used. Barrel shifter is used to shift or rotate n-bits in single clock cycle based on the control shift bits configuration. It is usually consists of multiplexers connected parallel to each other. It works completely on combinational logic and shifts data in a single clock cycle. Due to its advantage, RISC processors use these barrel shifters embedded in ALU.

# 8x4 Right Barrel Shifter

## Circuit Schematic

![bsintro](Images/bs_intro.png)

## Truth Table for Control Shift Bits in 8 × 4 Barrel Shifter

<table>
 <tr><th colspan="5" style="text-align:center" > Control Shift Bits </th><th colspan="5"> Output </th></tr>
 <tr><td>Sh0</td><td>Sh1</td><td>Sh2</td><td>Sh3</td><td>Sh4</td><td>Out0</td><td>Out1</td><td>Out2</td><td>Out3</td></tr>
 <tr><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td><td>In0</td><td>In1</td><td>In2</td><td>In3</td></tr>
 <tr><td>0</td><td>1</td><td>0</td><td>0</td><td>0</td><td>In1</td><td>In2</td><td>In3</td><td>In4</td></tr>
 <tr><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>In2</td><td>In3</td><td>In4</td><td>In5</td></tr>
 <tr><td>0</td><td>0</td><td>0</td><td>1</td><td>0</td><td>In3</td><td>In4</td><td>In5</td><td>In6</td></tr>
 <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>1</td><td>In4</td><td>In5</td><td>In6</td><td>In7</td></tr>
</table>



## Circuit Output Waveforms

![bsintroout](Images/bs_intro_out.png)

# Tools used

🌟 OS: CentOS Linux 7.9.2009

 * The CentOS Linux distribution is a stable, predictable, manageable and reproducible platform derived from the sources of Red Hat Enterprise Linux (RHEL)

🌟 Synopsys Custom Compiler

 * The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. It delivers industry-leading productivity, performance, and ease-of-use while remaining easy to adopt for users of legacy tools.
    
   🔗 https://www.synopsys.com/implementation-and-signoff/custom-design-platform/custom-compiler.html

🌟 PrimeSim 

 *  PrimeSim™ SPICE is a high-performance SPICE circuit simulator for analog, RF, and mixed-signal applications. PrimeSim SPICE offers a unique multi-core/multi-machine scaling and heterogeneous compute acceleration on GPU/CPU delivering faster runtime with sign-off accuracy.

   🔗 https://www.synopsys.com/implementation-and-signoff/ams-simulation/primesim-spice.html

🌟 Synopsis SAED 32/28nm PDK

 * The Synopsys 28nm Process Design Kit(PDK)

# Synopsis Custom Compiler Platform

![bssnps](Images/bs_snps_0.png)

![bssnps](Images/bs_snps_1.png)

![bssnps](Images/bs_snps_2.png)

![bssnps](Images/bs_snps_3.png)

# Implemented Circuit Design using Synopsis

## Schematics

![bssch](Images/bs_sch.png)

## Symbol

![bssym](Images/bs_sym.png)

## Testbench Design

![bstb](Images/bs_sch_tb2.png)

# Resultant Waveforms

![bstbout](Images/bs_plot_tb2.png)

## Resultant Waveforms For Different Control Shift Input 

![bstbout](Images/bs_plot_tb0.png)

![bstbout](Images/bs_plot_tb1.png)

![bstbout](Images/bs_plot_tb3.png)

![bstbout](Images/bs_plot_tb4.png)



# Author
 
 🖊️ Nalinkumar S, Pre-Final year student, B.E. ECE, Madras Institute of Technology, Anna University, Chennai, India
 
 
# Acknowledgements

 📖 Kunal Ghosh, Co-Founder of VLSI System Design (VSD) Corp. Pvt. Ltd. - kunalpghosh@gmail.com
 
 📖 [Synopsys Team/Company](https://www.synopsys.com/)
 
 📖 Chinmay panda, Technical Officer, Department of Electrical Engineering, IIT Hyderabad

# Reference

📔 P. Ashok Babu, V. Siva Nagaraju, Ramya Mariserla, Rajeev Ratna
Vallabhuni, ”Realization of 8 x 4 Barrel shifter with 4-bit binary to Gray
converter using FinFET for Low Power Digital Applications,” in Journal
of Physics: Conference Series, 2021.

📔 Bari, Surajit De, Debashis Sarkar, Angsuman , ”Design of low power,
high speed 4 bit binary to Gray converter with 8 × 4 barrel shifter using
nano dimensional MOS transistor for arithmetical, logical and telecommunication circuit and system application,” Microsystem Technologies,
2019.

📔 J. S. Deepak Vudatha, N. Kota, P. Gutha, B. Sreeja and S. P. Rajeev,
”VLSI Design of Low Power 8 × 4 Barrel Shifter using 90 nm TG
technology,” 2021 Fourth International Conference on Microelectronics,
Signals Systems (ICMSS), 2021.

