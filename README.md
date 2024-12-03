my-web-ngspice
==============
Integrate [EEcircuit](https://eecircuit.com/) and mermaid.js

Convert
```
My circuit
vcc a 0 dc 12v
r1 a b 4
r2 b 0 2
.op
.end
```
to
```mermaid
flowchart LR
  VCC[5V]---|Probe A|r1["<svg width='10' height='10' xmlns='http://www.w3.org/2000/svg'><circle style='fill:red' cx='5' cy='5' r='5'/></svg>" Resistor 4 Ohms]
  r1---|Probe B|r2["<svg width='10' height='10' xmlns='http://www.w3.org/2000/svg'><circle style='fill:red' cx='5' cy='5' r='5'/></svg>" Resistor 2 Ohms]
  r2 --> GND
  VCC --> GND[GND]
```
with injected calucated value
