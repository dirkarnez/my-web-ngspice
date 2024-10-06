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
  A --> r1("<img src='https://res.cloudinary.com/rsc/image/upload/b_rgb:FFFFFF,c_pad,dpr_2.625,f_auto,h_214,q_auto,w_380/c_pad,h_214,w_380/R0131895-01?pgw=1'; width='30' />")
  r1 --> B{Probe B}
  B --> r2[2 Ohms]
  r2 --> GND
```
with injected calucated value
