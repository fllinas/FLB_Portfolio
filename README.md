# Energy Analyst/Consultant Portfolio
**Fabrizio Llinás Biava**

##### List of projects:

1. Master Thesis: Optimization of integrated energy plant
2. Condensing capacity increase on an industrial refrigeration system
3. Compressor sequencing algorithm for an industrial refrigeration system
4. Savings estimation for instalation of a new coal boiler economizer
5. Analysis of parameter influences on an absorption system
6. Discharge pressure reduction on an industrial refrigeration system
7. Machine learning algorithms for energy savings estimation
8. Tecnoeconomic analysis of instalation of a solar thermal field


## Project 1
Master Thesis: Optimization of the design of a and scheduling of a biomethane plant integrated with a reversible Solid Oxide Cell and a PV solar field.

##### Objective:
The objective of this thesis is to model and numerically optimize the design and scheduling of an integrated biogas-based energy plant. Optimization is carried out by formulating and implementing a mixed integer linear program (MILP) in Python, in order to obtain the optimal plant configuration, components sizing and operational strategy under different scenarios, whilst targeting the solution with the minimum annualized costs. 

![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/a2bb6337-e691-42e1-81dc-61433e203bdc)


##### Components of Energy System:
The energy system modelled and optimized in this thesis comprises the following six sections:
1. A biomethane production section, featuring the anaerobic digestion of organic fraction of municipal
solid waste (OFMSW) and biogas upgrading. Upgrading is based on amine-scrubbing and produces
two streams: biomethane in specification for natural gas grid injection and nearly pure CO2;
2. A photovoltaic solar field (PV);
3. An electro-chemical section including a reversible SOEC/SOFC cell (rSOC) and a Sabatier
methanation process, which can work in two modes: (i) as Power-to-Gas system that produces CH4
via methanation from H2 (from water electrolysis in SOEC mode) and CO2 from biogas upgrading;
(ii) as Gas-to-Power system that converts biogas into electricity (SOFC mode);
4. A battery energy storage system (BESS);
5. Gas and heat storage units aimed at decoupling the continuous biomethane production process from
the alternate, discontinuous, electro-chemical processes;
6. A boiler, working as a hot utility to satisfy peak thermal duties.

![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/23474321-872f-41ab-82ec-9ace319ff09e)


##### Selection of best input hourly profiles and forecasting scenarios:

Due to the high amount of data corresponding to years of simulation, a k-means clustering algorithm is used to reduce inputs into more manageable amount of information. In this work, the annual data corresponding to ambient temperature, solar irradiance, gas prices and electricity prices is reduced into 6 different clusters combining typical and extreme periods whilst considering different time frames in the form of days and weeks (typical days and/or typical weeks and extreme periods to evaluate plant performance).

![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/f4fe3414-df8e-4b13-b342-6a1b33bb3022)

Furthermore, forecasted scenarios are inputed to evaluate results in different present and futuristic possiblities. This result in the combination of 12 different scenarios for the simulation.

![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/8238d77f-55bc-4eee-b7a2-7fbc105871bd)


#### Simulation and Results

The python MILP algorithm was proven to being able to simulate the operation of the integrated energy plant and obtain the optimal results on selection of equipment, optimal sizing and hour by hour operation whilst maximizing the annual profits.

Results per Scenario:
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/233e6455-eee6-425f-b11f-a3b6a8d882b9)

Annualized and Normalized Energy and Material Balances:
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/48603e18-43da-44e6-921d-4bf4dbc5ab0b)


## Project 2
Condensing capacity increase on an industrial refrigeration system



