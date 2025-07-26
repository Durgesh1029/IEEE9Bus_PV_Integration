IEEE 9-Bus System with PV Penetration Analysis
Overview
This repository contains the analysis of photovoltaic (PV) penetration on the IEEE 9-bus system, focusing on voltage stability and power loss reduction. The study uses MATPOWER 8.0 to simulate various scenarios, including stressed loads and PV integration, and compares PV performance with conventional Static Var Systems (SVS).
Objectives

Assess the impact of PV systems on voltage profiles and power losses in the IEEE 9-bus system.
Compare PV integration with conventional SVS solutions for voltage support.
Analyze technical metrics such as voltage stability and loss reduction.

Methodology

Tool: MATPOWER 8.0 for power flow simulations.
Base File: Modified case9.m for scenarios (e.g., stressed loads, PV integration).
Data Extracted: Bus voltage magnitudes (pu) and total system losses (MW).
Approach: Systematic power flow analysis using Newton-Raphson method to solve power flow equations.
Scenarios:
Base case: Voltage stability within 0.95–1.05 pu.
Stressed load at Bus 6 (135 MW, 45 MVAr).
PV integration at Bus 8 (25 MW, 50 MW, 75 MW) and Bus 5.


Key Metric: Voltage at the collapse point (V_critical) to quantify proximity to instability.

Results

Base Case: All bus voltages within 0.95–1.05 pu (e.g., Bus 8: 1.000 pu).
PV at Bus 8 (50 MW): Maintains voltage at 1.000 pu, but losses increase to 4.78 MW from 3.85 MW.
PV at Bus 8 (25 MW): Total losses 4.122 MW, voltage 1.000 pu, offering moderate benefits.
PV at Bus 8 (75 MW): High PV penetration scenario analyzed (results incomplete in document).
Stressed Load at Bus 6: Voltage drops to 0.988 pu, total losses 5.05 MW, less vulnerable than Bus 8.
PV at Bus 5: Preliminary analysis indicates balanced voltage support (details incomplete).
Key Finding: PV outperforms SVS in reducing losses and supporting voltage, especially at Bus 5 and 8.

Conclusions

PV integration enhances voltage support, particularly at Bus 8, and reduces losses when optimally placed (e.g., Bus 5).
Distributed PV balances voltage across buses.
MATPOWER effectively analyzes voltage and loss impacts.
Future Work:
Optimize PV sizing and placement.
Conduct dynamic stability analysis (dV/dt = f(P, Q, t)).
Explore economic optimization of PV placement.



Repository Contents

case9_pv.m: Modified MATPOWER case file for IEEE 9-bus system with PV integration.
CITATION.cff: Citation file for referencing the original papers.
citation.md: Markdown file with citation details.

Setup and Usage

Install MATPOWER:
Download and install MATPOWER 8.0 from MATPOWER's official website.
Ensure MATLAB or Octave is installed.


Run Simulations:
Clone this repository: git clone <repository-url>.
Open MATLAB/Octave and navigate to the repository directory.
Run the case9_pv.m script to simulate the IEEE 9-bus system with PV integration:runpf('case9_pv');




Modify Scenarios:
Edit case9_pv.m to adjust PV penetration levels or stressed load conditions as described in the study.



References

Channi, H. K., Sandhu, R., Kaur, H., Singh, P., Gaba, S., & Kaur, J. (2023). An Approach for Load Flow and Load Dispatch Analysis of IEEE-9 Bus System. 2023 2nd International Conference on Ambient Intelligence in Health Care (ICAIHC), Bhubaneswar, India.
Rahman, Tasnim Ikra. (2023). Impact of Solar Generation on IEEE 9-bus System. Electronic Theses and Dissertations, 3818.
Loji, K., Davidson, I. E., & Tiako, R. (2019). Voltage Profile and Power Losses Analysis on a Modified IEEE 9-Bus System with PV Penetration at the Distribution Ends. 2019 Southern African Universities Power Engineering Conference/Robotics and Mechatronics/Pattern Recognition Association of South Africa.

Acknowledgments
This work builds upon the research conducted in the referenced papers. Special thanks to the authors for their contributions to power system analysis.
