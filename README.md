
<h1>Rule-based Energy Management System for Hybrid Electric Vehicle</h1>

<h2>Description</h2>
<b>During a seminar presentation within our curriculum, we devised an Energy Management System for a Hybrid Electric Vehicle (Mercedes-Benz A 170 CDI (W168)) aimed at minimizing fuel consumption through electromobility principles.
</b>
<br />
<br />

<h2>Languages Used</h2>

- <b>MATLAB and Simulink</b>

<h2>Library Used</h2>

- <b>QSS Toolbox (MATLAB)

<h2>Vehicle Specifications</h2>

- <b>Model:</b> Mercedes-Benz A 170 CDI (W168)
- <b>Diesel Engine:</b> 66 kW / 180 Nm nominal, 60 kW / 187 Nm measured
- <b>Electric Motor:</b> 12 kW / 60 Nm
- <b>Battery:</b> 16.38 kW / 0.468 kWh / 48 V
<p align="center">
<img src="pehv.jpg" width="45%" alt="PHEV"/><br>
<em>PHEV</em>
</p>

<h2>Model Components</h2>

- <b>Driving Cycle Map:</b> Provides vehicle speed, acceleration, gear ratio, and total traveled distance.
- <b>Vehicle Model:</b> Represents the Mercedes-Benz A 170 CDI (W168) in the simulation.
- <b>Engine Model:</b> Represents the diesel engine.
- <b>Electric Motor Model:</b> Represents the electric motor.
- <b>Battery Model:</b> Represents the battery.
- <b>Gearbox Model:</b> Applies gear ratios to adjust vehicle parameters.
- <b>Control Unit (Energy Management) Model:</b> Contains logic for engine and electric motor operation.
- <b>Fuel Tank Model:</b> Calculates fuel consumption based on engine power.
- <b>Total Equivalent Fuel Consumption Model:</b> Calculates overall fuel consumption from both engine and electric motor power.
<p align="center">
<img src="Vehicle-model-in-Simulink.png" width="85%" alt="Model Components"/><br>
<em>QSS Model Components</em>
</p>

<h2>Driving Cycles for Testing (in brief)</h2>

 - <b>NEDC (New European Driving Cycle):</b> Tests fuel consumption and emission levels.
<p align="center">
<img src="NEDC.png" width="60%" alt="NEDC (New European Driving Cycle)"/><br>
<em>NEDC (New European Driving Cycle)</em>
</p>
  
 - <b>FTP-75 (Federal Test Procedure):</b> Tests fuel consumption and emissions in various driving conditions including city driving, aggressive driving, and highway driving.
<p align="center">
<img src="ftp-75.png" width="60%" alt="FTP-75 (Federal Test Procedure)"/><br>
<em>Figure: FTP-75 (Federal Test Procedure)</em>
</p>


<h2>Rule-Based Strategy</h2>

- <b>Load Point Shifting:</b> Technique to optimize ICE operating point for better fuel economy.
- <b>Energy Management System:</b> Implemented using rule-based strategy in MATLAB.
- <b>Interpreted MATLAB Function:</b> Used to define rules for switching between modes.

<h2>Rule Conditions and Results</h2>

- <b>Rule 1:</b> Regeneration when TMGB < 0.
- <b>Rule 2:</b> LPS (Motor mode) when TMGB ≥ TED,max.
- <b>Rule 3:</b> LPS (Gen. mode) when TED,th < TMGB < TLPS,gen,th.
- <b>Rule 4:</b> Electric Driving when TMGB < TED,th and wMGB < wMGB,th.
- <b>Rule 5:</b> Conventional (Engine only) as default.

<h2>Mode Descriptions</h2>

- <b>A. Electric:</b> Default mode with engine OFF and torque split ratio u = 1.
- <b>B. Hybrid:</b> Engine continually running, torque split ratio u varies.
- <b>C. Charging:</b> Electric device charges battery, u < 0.
- <b>D. Regenerative Braking:</b> Engine OFF, 0 < u < 1, TMGB < 0.
- <b>E. Conventional:</b> Default mode when none of the rules apply.

<p align="center">
<img src="NEDCmodes.png" width="90%" alt="Rule-based strategy on NEDC"/><br>
<em>Figure: Rule-based strategy applied on NEDC</em>
</p>
<p align="center">
<img src="FTP-75modes.png" width="90%" alt="Rule-based strategy on FTP-75"/><br>
<em>Figure: Rule-based strategy applied on FTP-75</em>
</p>

<h2>Optimization of Parameters</h2>
<h2>Optimal Parameters</h2>

- <b>Torque threshold for LPS in motor mode (TED,max):</b> 33 Nm
- <b>Torque threshold for LPS in generator mode (TLPS,gen,th):</b> 34 Nm
- <b>Torque threshold for Electric mode (TED,th):</b> 29 Nm
- <b>Velocity threshold for Electric mode (wMGB,th):</b> 300 rad/s
- <b>Maximum torque-split factor for LPS (uLPS,max):</b> 0.01
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
