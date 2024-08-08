# EpiStimulator

## WHAT IS IT?
This model of the transmission of a virus simulates how infected persons (carriers) can affect the health of an entire population of individuals. It illustrates the effectiveness of public health measures, quarantine, and vaccinations on the spread of the virus. The model is based on NetLogo simulators Virus and epiDEM Basic.

## HOW IT WORKS
- The model operates with individual agents who randomly wander around the world. Once they come in contact with an infected person, they can contract the virus. The user decides how contagious ("transmission rate") and deadly ("mortality") the virus is and how long it takes for an infected person to become contagious ("incubation period"). The mortality rate impacts the chance of recovery.
- The user can set vaccinations and quarantine as public health measures to slow down the spread of the virus. Vaccination rate and effectiveness can be adjusted respectively. The quarantine setting stops people from moving. It is also possible to adjust how many people there are ("population size") and how fast they move ("mobility").
- The colors indicate the health status of the person. People can be carriers (orange; infected and contagious, but not yet sick), sick (red), susceptible (green; not yet infected with the virus), recovered (blue; recovered from the sickness), or dead (black). Once recovered, the agents are completely immune to the virus.
- The graphs and boxes to the right depict the development of the health status of the agents over time.

## HOW TO USE IT
- **SETUP**: Creates a scenario according to the chosen parameter values. After setting up the model, pushing the GO button will run the simulation. After each change in parameters, the SETUP button needs to be pressed to apply the changes. RESET will set all values to the default values.
- **GO**: Runs the simulation.
- **RESET**: Sets all values to the default values.
- **Ticks Slider**: Adjusts the speed of the simulation ("slower" or "faster").

Try changing the parameters to see how it affects the spread of the virus and the health status of people. To try out the “Interventions”, turn on the switches for “quarantine” and “vaccinations”. After switching on vaccinations, you can adjust the vaccination rate (how many people are vaccinated) and effectiveness (how effectively the virus is stopped). The effectiveness of the quarantine is hardcoded by restricting the movement of quarantined agents.

## THINGS TO TRY
- **Agent settings**:
  - **Show-age**: How does the virus affect people of different age groups?
  - **Carrier tracking**: How much did initial carriers move that started the epidemic?

- **Population size**:
  - How does population size and density impact the spread of the virus?

- **Virus Settings**:
  - How do transmission rate and mortality impact the spread of the virus?
  - How does it impact the number of recoveries and deaths?

- **Interventions**:
  - How do interventions impact infection rates, recoveries, and deaths?

## PAIR-C Framework

### Pattern:
- The disease Spread Plot visualizes epidemic progression.
- The simulation starts out with Susceptibles and Carriers, and ends with Vaccinated/Recovered or Dead.

### Agents:
- **Turtles**: Individual agents with tracked health and movement.
- Initial Carriers and Susceptible turtles.

### Interactions:
- When a susceptible turtle comes into contact with a carrier, it gets infected.
- Infected turtles continue to infect other susceptible turtles.
- This later results in the death or recovery of said turtle.
- Adjustable Factors which affect Interactions include:
  - Transmission Rate
  - Vaccination rate
  - Vaccination effectiveness
  - Mobility
  - Population size

### Relations:
- **Health & Movement**: Links between health status and mobility.
- **Vaccination & Susceptibility**: The percentage vaccinated affects susceptibility.
- **Age & Mortality**: Older turtles have increased mortality rates.

### Causality:
- **Transmission and Mortality**:
  - **Cause**: Carriers moving around in space.
  - **Effect**: Susceptible turtles get infected.
- **Public Health Interventions**:
  - **Cause**: Actions like vaccination, lockdown, social distancing, and quarantine.
  - **Effect**: Changes in the number of sick, recovered, and dead turtles.

### Interaction Features:
- **Distinct set/ Same Set**: Distinct (Different starting turtles, Carriers and Susceptibles)
- **Restricted/ Random**: Mostly random, but can be restricted (when in Quarantine state)
- **Serial Order/ Simultaneous**: Simultaneous (Agent movement is simultaneous)
- **Dependent/ Independent**: Independent (Agents act independently of one another)

### Inter-level Features:
- **Incremental Change/ Converging Change**: Converging (It eventually converges and reaches a balanced state)
- **Cumulative Summing/ Collective Summing**: Collective (Simultaneous and Non-linear)

### Implication Features:
- **Presence of Causal Agent**: Yes, Carriers.
- **Alignment**: Lack of alignment

This epidemic simulator features both emergent and sequential processes. Disease spreading, reflecting its natural progression through the population, is an emergent process, while vaccination is a sequential process.

### Illustration

<img width="1427" alt="image" src="https://github.com/user-attachments/assets/a33fec7f-06b2-426c-a180-797aa34ef502">

