# Energy Analyst Portfolio
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
**Master Thesis: Optimization of the design of a and scheduling of a biomethane plant integrated with a reversible Solid Oxide Cell and a PV solar field.**

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


#### Conclusions:

The key results of this thesis are:
1. A MILP optimization model for the design and scheduling of an integrated multi-energy plant
is developed in PYTHON (Anaerobic Digester + Biogas Upgrading + rSOC + methanator +
PV + BESS).
2. The model is based on linearized on-design/off-design performances and costs starting from
detailed first principle models (Aspen Plus, Matlab, etc.) of the components.
3. Different "typical periods" are assessed in order to get a reasonable trade-off between
computational time and accuracy. The selected approach is with 6 typical days + 3 extreme
ones.
4. Twelve alternative scenarios are investigated, each one reflecting different capital costs (present
day vs 2050-time horizon) and constraints (e.g. no net energy import, 100%-renewable, and
carbon related incentives/restrictions). Results show that SOFC is installed in "no net energy
import" scenarios and in case of higher market penetration (i.e. year 2050).
5. Sensitivity is carried out for a number of parameters. The most interesting one is on the
"additional premium tariff" (i.e. incentives) the plant will receive for ancillary services on the
electricity market. Results show that in case the Ancillary Service Factor (i.e. additional
revenue for the plant for the energy storage service) is 50% on top of the electricity price then
the electrolysis cell mode is selected for this 2050 scenario. The system now acts as a “big
battery” enabling interactions between the fully decarbonized electricity grid and a “greener”
gas grid, by absorbing exceeding electric power coming from peak RES afternoon and
converting it into biomethane
Economic analysis on 3 interesting scenarios (1D, 3C and ASF=1.75) of the plant design show
that a retrofit option is of big interest for 2050 old anaerobic digesters that might be thought of
being dismantled; on the other hand, the full plant option (including AD) requires a gross
financing for the different plant designs with gate fees of over 90 €/ton.
7. The interactions amongst the different units in matter of energy and material streams are indeed
of interest as the system selects the multiple conversion and storage units whilst satisfying for
their multiple and variable demands of electricity and heat. The system can be optimized for
different power-to-gas, gas-to-power and power-to-power scenarios.




## Project 2
**Condensing capacity increase on an industrial refrigeration system**

##### Objective:
The objective of this project is to detect the necessity of a condensation capacity increase for an compressed NH3 refrigeration system whilst estimating the potential savings that could be achieved on installing different sizes. An analysis and further simulation is done on Python to carry out the task.


##### Actual state of the system:

Through the analysis of 6 monhts of data on a 10 minute granularity an initial data analysis is done to detect the behaviour of the important parameters. These being: flow rates, discharge pressures, suction pressures, compressor consumptions all from both lower and high stage pressure levels. Anomalies are detected on the high variations on ranges of discharge pressures mainly when an increase in demand is observed (high flow rates)

High stage flow rate (Y axis) vs Low stage flow rate (X axis). Ligher colors indicate higher discharge pressures.
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/75675ff7-e693-4ec0-ad85-d048358989a0)


Discharge pressure (Y axis) vs Estimated plant demand (X axis).
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/00e8a339-9c56-4a76-93e8-813ace73236e)



##### Energy efficiency of the industrial site:

A calculation of the systems COP (Coefficient of Performance) is done using enthalpies of ammonia whilst considering the changes of state of the substance through the consumers. COP is further evaluated and is found to start reducing when plant starts to exceed a given value.

COP (y axis) vs Plant demand (TR)

![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/f6eb6268-6ba9-4826-b888-88c2e42bd00a)



#### Simulations and results:

A simulation is done with the expected increase in condensation capacity and estimated reduction in discharge pressure for every point of data. Through a machine learning model the expected power consumption is calculated and estimated savings for the installation of new equipment is obtained. Results are not shown for disclosure but through them the industrial site could decide which equipment size was better for their needs.


## Project 3
**Compressor sequencing algorithm for an industrial refrigeration system**

##### Objective:

The objective of this project was to develop an optimized sequencing algorithm (Python) on the turn on/turn off from 9 compressors from an industrial ammonia vapour compression refrigeration site. 

##### Actual state of the system:

Initially, we analyze more than 8 months of data on a 5 minute granularity to obtain necessary information on improvement possibilities. We can observe through the demand flow rates that the nature of the plant is quite variable through time, and so the possibilities of sequencing start becoming realistic.

Demand distribution for all 3 main user groups (flow rate in gpm):
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/4957689d-808f-4c4c-a96c-410cdab90c6a)


As we manipulate the data in python in order to being able to analyze sequence by sequence of compressors, we detect different efficiencies for the vast combination of compressor sequences that occur on the system.

Flow rate (X axis) vs Efficiency (Y axis) - feature: sequences in colors:
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/675d5923-18a1-435e-be98-fbec57bcec74)

Different efficiences for the different sequences conclude certainly on the possibility of improving performance through the use of more efficient sequences:
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/a776c0b4-5d33-4341-8273-d75d67f74a01)


##### Algorithm Development:

Through the selection of the most optimal sequences and optimization of the load factor, we simulate the possible behaviour of the system on the possible implementation of the algorithm.

Current load factor (orange) vs Simulated load factor (blue):
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/587b9065-c288-43c6-8cf9-d24950b97133)


##### Results:

After implementation of the algorithm outputs on site, a considerable increase in the load factor was achieved with savings estimated at around 5% of total consumption. 

Load Factor Distribution - before (blue) and after implementation (red):
![image](https://github.com/fllinas/fllinas.github.io/assets/55508521/2d057b55-a32a-4c7a-9065-0e81504403c2)


