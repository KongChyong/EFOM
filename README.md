**🧠 About the EFOM Model**

The Energy Futures Optimisation Model (EFOM) is a partial equilibrium, linear programming model developed to analyse long-term decarbonisation pathways and energy system transitions under varying policy, technology, and market assumptions. It is described in detail in Chyong et al. (2024) [https://www.sciencedirect.com/science/article/pii/S2211467X24000294].

EFOM is formulated in AIMMS, a modelling environment for optimisation-based applications, and solved using the IBM CPLEX solver.

The model minimises total energy system costs—including capital and operational expenditures—while satisfying exogenous energy service demand, greenhouse gas (GHG) constraints, and other user-defined restrictions. It operates with hourly resolution and represents 14 European regions, enabling endogenous trade in primary and secondary energy carriers.

**🔧 Key Features:**
- Supply & transformation sectors: Fossil fuels, renewables, nuclear, hydrogen (electrolysis and methane reformation), and synthetic fuels.

- Final consumption: Disaggregated representation of buildings, transport, and industry.

- Technologies: Power generation (CCGT, wind, solar, nuclear, etc.), energy storage (batteries, pumped hydro), end-use appliances (e.g., hybrid heat pumps, electric vehicles).

- Networks: Electricity grids, CH₄, H₂, and CO₂ pipelines, including cross-border flows.

The input dataset representing the net zero scenario modelled in Chyong et al. (2024)—calibrated to the European Commission’s 1.5°C TECH scenario from the 2050 Long-Term Strategy—is provided in the repository under /DATA IN/.

**▶️ How to Run EFOM**

To run the model:

1. Install AIMMS with the IBM CPLEX solver enabled.

2. Open the project by double-clicking the file EFOM.aimms located in the main folder.

3. In the AIMMS interface, run the procedure IMPORT_DATASET to load the scenario dataset.

4. Then run the procedure SOLVE_MODEL to execute the optimisation.

The results will be generated in AIMMS under the model section "MODEL RESULTS" but also stored in decision variables.
