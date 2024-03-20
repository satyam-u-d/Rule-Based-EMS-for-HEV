
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

<h2>Driving Cycles for Testing (in brief)</h2>

 - <b>NEDC (New European Driving Cycle):</b> Tests fuel consumption and emission levels.
<p align="center">
<img src="" height="85%" width="85%" alt="NEDC (New European Driving Cycle)"/>
</p>
  
 - <b>FTP-75 (Federal Test Procedure):</b> Tests fuel consumption and emissions in various driving conditions including city driving, aggressive driving, and highway driving.
<p align="center">
<img src="" height="85%" width="85%" alt="FTP-75 (Federal Test Procedure)"/>
</p>


<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/krRFrK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>

<p align="center">
<img src="https://i.imgur.com/3d3CEwZ.png" height="85%" width="85%" alt="RDP event fail logs to iP Geographic information"/>
</p>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
