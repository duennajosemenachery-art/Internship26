# Project Report

Upload the final report (TEAM_1.pdf) here.

# PROJECT OVERVIEW
The Digital Energy Meter is a Verilog HDL based digital hardware design that measures electrical energy by calculating power from the supplied voltage and current inputs. The design uses a Finite State Machine (FSM) to perform power calculation, energy computation, and energy accumulation in a sequential manner. The project was implemented and verified using Cadence EDA tools through the complete ASIC design flow, including synthesis, floorplanning, power planning, placement, clock tree synthesis, routing, and simulation.
The design accepts 4-bit voltage and current inputs and produces a 32-bit accumulated energy output. The accumulated energy is updated every clock cycle, making the design suitable for digital energy monitoring applications.
# DESIGN METHODOLOGY
The project was developed using a structured RTL design methodology in Verilog HDL. The implementation consists of three major stages controlled by a Finite State Machine (FSM).
Step 1 – Power Calculation
The first stage calculates instantaneous power by multiplying the 4-bit voltage and current inputs.
Power = Voltage × Current
The calculated power value is stored in an 8-bit register.
Step 2 – Energy Calculation
In the second stage, the calculated power is multiplied by a fixed time interval of 10 ns representing one clock period.
Energy = Power × Time
The resulting energy value is stored in a 12-bit register.
Step 3 – Energy Accumulation
The calculated energy is added to the previously accumulated energy value stored in a 32-bit register.
Final Energy = Previous Energy + Current Energy
This sequence repeats continuously after every three FSM states until the reset signal is asserted.
The complete design was verified using a Verilog testbench with multiple voltage and current combinations. Functional simulation was performed using Cadence SimVision, followed by synthesis and physical implementation using Cadence Innovus.
# RESULTS AND DISCUSSION
The Digital Energy Meter was successfully designed, simulated, synthesized, and implemented using Cadence tools.
Simulation results confirm that the FSM correctly performs power calculation, energy computation, and cumulative energy accumulation for different input combinations.
The synthesis reports indicate that the design is synthesizable and suitable for ASIC implementation. Floorplanning, power planning, placement, clock tree synthesis, routing, and signoff were successfully completed without major design rule violations.
The final routed design demonstrates proper connectivity and successful implementation of the Digital Energy Meter.
(Insert your Simulation, Synthesis, Floorplan, Placement, CTS and Routing screenshots here.)
# TEAM MEMBER CONTRIBUTIONS
Team Member
Contribution
Vivekanand P
Designed the Verilog RTL, developed the FSM architecture, and verified functionality using simulation.
Fariz K Muhammed
Performed synthesis, floorplanning, power planning, placement, CTS, routing, and ASIC implementation using Cadence tools.
Duenna Jose
Prepared the block diagrams, documentation, project report, analyzed simulation results, and managed the GitHub repository.
# CONCLUSION
The Digital Energy Meter was successfully implemented using Verilog HDL and Cadence EDA tools. The FSM-based architecture accurately calculated power, computed energy, and accumulated the total energy over multiple clock cycles. Functional verification through simulation confirmed the correctness of the design, while synthesis and physical implementation demonstrated its suitability for ASIC realization. This project provided practical experience in RTL design, verification, and the complete ASIC implementation flow.
