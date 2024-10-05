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
flowchart
  VCC[5V] --> A{Probe A}
  VCC --> GND[GND]
  A --> r1[4 Ohms]
  r1 --> B{Probe B}
  B --> r2[2 Ohms]
  r2 --> GND
```
