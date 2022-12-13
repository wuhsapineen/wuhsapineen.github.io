---
title: Space Engineers
description: 
created: 2022-11-08 07:30:00 +1000
tags: pages, notes, games, Space Engineers
source: 
author: wuhsapineen
nav: false
reference:
- []

Table of Contents:

-   [To Do][3-01]
-   [Networked Grids][3-02]
-   [Laser Antennae][3-03]
-   [Coordinates][3-04]
-   [Colors][3-06]
-   [Auto LCD][3-07]
-   [Other][3-08]
-   [Station Registry][3-11]
-   [Ship Registry][3-09]
-   [Naming Convention][3-05]
-   [Fleet Blueprints][3-10]


---

Small mining outposts with mining drones and cargo haulers. <br />
Cargo haulers pick up at outposts and deliver to mining hub. <br />
Large cargo ships pick up at mining hubs and deliver to production facility (requires jump drive). <br />

```
(\__/)
( ='.'= )
 (")__(")
```


## <span id="SE-todo">ToDo</span>

-   Mines:
    -   **Platinum\***
    -   Uranium \[1]
    -   Gold
    -   Silver
    -   Cobalt
-   Grid Networking
    -   Build Remote Control blocks on all grids and name them appropriately (Remote Control - \<Grid Name\>)
-   Salvage space station (SalvageStation01)
    -   ~~Located adjacent to SpaceStation01~~ ***with small cargo shuttle between***
    -   ~~Large docking area for collected salvage~~
    -   ~~Grinder ship~~s
    -   ~~Collection cargo containers~~
    -   ~~Dock for componant hauler~~
    -   ~~Cargo "buddy" to drain salvage of Hydrogen, Oxygen, and any scrap componants including ammo~~
-   Moon Mining Hub (MoonStation01 - not exists)
    -   Large collection space
    -   Storage area
    -   O2/H2 Generators (10)
    -   Hydrogen Engines
-   Moon Station (MoonStation02)
    -   ~~Power room with Hydro generators~~ and batteries (NO REACTORS)
    -   Medical room with cryo pod
    -   Control room with LCD panels, programming blocks, and timers; ***might be big***.
        -   PBs:
            -   Whip's Auto Door
            -   MMaster's Advanced LCD 2
        -   Timers:
            -   Doors: 
    -   ~~Air Traffic Control tower with control seats and LCD panels~~
-   ~~Production Facility~~ (ProductionStation)
    -   **Name:** ProductionStation
    -   **Remote Control:** Remote Control - ProductionStation (notexists)
    -   GPS:
        -   GPS:17. ProductionStation Approach 1:-76289.51:19135.81:78707.51:#FFB4D7FF:
        -   GPS:18. ProductionStation Approach 2:-76346.01:19532.63:79626.54:#FFB4D7FF:
        -   GPS:83. Jump - Production Station:-77708.52:15668.42:82215.72:#FFFFD700:
    -   O2/H2 Generators (x80)
    -   Hydrogen Engines (x40)
    -   Solar Panels (x324)
    -   Refineries (x24; 2x Power Module, 2x Yield Module each)
    -   Assemblers (x24; 2x Power Module, 2x Speed Module each)
    -   Storage (x144; Large Industrial Cargo Container)
-   ~~Mining Carrier~~
    -   **Name:** CVU-###
    -   **Blueprint:** M80 Mining Carrier
    -   Has:
        -   Hydrogen thrusters
        -   Plenty of hydrogen storage (>=20 large containers)
        -   Plenty of ore storage space (>=20 large containers)
        -   O2/H2 Generators to refill hydro tanks
        -   Hydrogen Engines to charge batteries
        -   Enough batteries for full systems usage plus drone charging
        -   Cold start reactor
        -   
-   ~~Mining Drones~~ 
    -   **Name:** MD-###
    -   **Blueprint:** M80 Hydro Mining Ship
    -   ~~Rebrand existing PAM drone with M80 colors~~


## <span id="SE-networkedgrids">Networked Grids</span>
Remote control blocks must be placed on each grid with the grid name in its name. E.g. Remote Control - SpaceStation01
-   SpaceStation01
-   ProductionStation


.
<br />
## <span id="SE-laserantennae">Laser Antennae</span>
-   **Stations**
    -   LA-IceStation
        -   GPS:LA-IceStation:-87563.55:-31716.71:66516.79:
    -   LA-Earth01
        -   GPS:LA-Earth01:-44587.08:-345.25:41468.91:
    -   LA-SpaceStation01-01
        -   GPS:LA-SpaceStation01-01:-84470.04:-29839.42:73006.27:
    -   LA-SpaceStation01-02
        -   GPS:LA-SpaceStation01-02:-84533.63:-29842.35:73129.65:
    -   LA-MoonStation02
        -   GPS:LA-MoonStation02:21112.53:128192.23:-113157.68:
    -   LA-MoonOrbitStationUpper
        -   GPS:LA-MoonOrbitStationUpper:23084.2:125817.26:-113062.77:
    -   LA-MoonOrbitStationLower
        -   GPS:LA-MoonOrbitStationLower:23081.96:125852.98:-113061.1:
    -   LA-ProductionStation01
        -   not exists
-   **Comms Relay Antennae**
    -   LA-CommsRelay-01
        -   GPS:LA-CommsRelay-01:-85422.2:-31278.44:69662.29:
    -   LA-CommsRelay-02
        -   GPS:LA-CommsRelay-02:-85419.55:-31282.05:69660.06:
    -   LA-CommsRelay-03
        -   GPS:LA-CommsRelay-03:-85415.87:-31279.86:69666.5:
    -   LA-CommsRelay-04
        -   GPS:LA-CommsRelay-04:-85424.55:-31285.31:69664.98:
    -   LA-CommsRelay-05
        -   GPS:LA-CommsRelay-05:-85335.98:-31581.21:70254.12:
    -   LA-CommsRelay-06
        -   GPS:LA-CommsRelay-06:-85333.33:-31584.81:70251.89:
    -   LA-CommsRelay-07
        -   GPS:LA-CommsRelay-07:-85330.99:-31577.95:70249.2:
    -   LA-CommsRelay-08
        -   GPS:LA-CommsRelay-08:-85339.66:-31583.4:70247.68:
-   **Relay Satellites**
    -   LA-01 (RelaySat01-01)
        -   GPS:LA-01:-79292.76:-25700.44:67608.45:
    -   LA-02 (RelaySat01-02)
        -   GPS:LA-02:-79290.13:-25700.46:67609.89:
    -   RelaySat02-01
        -   GPS:RelaySat02-01:-95807.22:17396.89:34636.56:
    -   RelaySat02-02
        -   GPS:RelaySat02-02:-95808.27:17395.23:34634.29:
    -   RelaySat03-01
        -   GPS:RelaySat03-01:-51255.03:82166.52:-38512.7:
    -   RelaySat03-02
        -   GPS:RelaySat03-02:-51255.25:82164.37:-38514.78:
-   **Connections**
    -   LA-Earth01 - LA-RelaySat01-01
    -   LA-SpaceStation01-01 - LA-RelaySat01-02
    -   LA-SpaceStation01-02 - LA-CommsRelay-08
    -   LA-ProductionStation01 - LA-CommsRelay-01
    -   LA-RelaySat02-01 - LA-CommsRelay-03
    -   LA-RelaySat02-02 - LA-RelaySat03-01
    -   LA-RelaySat03-02 - LA-MoonOrbitStationUpper
    -   LA-MoonOrbitStationLower - LA-MoonStation02


.
<br />
## <span id="SE-coords">Coordinates</span>

-   **RDSR - Rogue Sappers**
    -   GPS:RDSR01:-70809.1:-34070.1:70024.8:
-   **SPRT - Space pirates**
    -   GPS:SPRT01:-94638.0:-34170.0:64923.4:
    -   GPS:SPRT02:-103714.3:-23010.5:72986.6:
-   **SPDC - Specialized Drilling Consortium**
    -   GPS:SPDC01:-93342.4857315367:-34229.8181152937:63928.587241044
-   **UDHS - Unyielding Hauling Service**
    -   GPS:UDHS01:-84776.7402741437:-31475.8978549342:71974.4470085772

### Planets and Moons
Name | X | Y | Z | Actual X | Actual Y | Actual Z | Offset | Radius | Diameter | GPS | GPS X | GPS Y | GPS Z
--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---
Alien | 0 | 0 | 5600000 | 131072 | 131072 | 5731072 |  | 60000 | 120000 | GPS:Center of Alien:131072.50:131072.50:5731072.50:#FFF10000: | 131072.5 | 131072.5 | 5731072.5
Earthlike | -131072 | -131072 | -131072 | 0 | 0 | 0 | 131072 | 60000 | 120000 | GPS:Center of EarthLike:0.50:0.50:0.50:#FFF10000: | 0.5 | 0.5 | 0.5
Mars | 900000 | 0 | 1500000 | 1031072 | 131072 | 1631072 |  | 60000 | 120000 | GPS:Center of Mars:1031072.50:131072.50:1631072.50:#FFF10000: | 1031072.5 | 131072.5 | 1631072.5
Moon | 0 | 120000 | -130000 | 131072 | 251072 | 1072 |  | 9500 | 19000 | GPS:Center of Moon:16384.50:136384.50:-113615.50:#FFF10000: | 16384.5 | 136384.5 | 113615.5
Titan | 20000 | 210000 | 5780000 | 151072 | 341072 | 5911072 |  | 9500 | 19000 | GPS:Center of Titan:36384.50:226384.50:5796384.50:#FFF10000: | 36384.5 | 226384.5 | 5796384.5
Triton | -350000 | -2500000 | 300000 | -218928 | -2368928 | 431072 |  | 40126.5 | 80253 | GPS:Center of Triton:-284463.50:-2434463.50:365536.50:#FFF10000: | -284463.5 | -2434463.5 | 365536.5
Europa | 900000 | 0 | 1600000 | 1031072 | 131072 | 1731072 |  | 9500 | 19000 | GPS:Center of Europa:916384.50:16384.50:1616384.50:#FFF10000: | 916384.5 | 16384.5 | 1616384.5
Pertam | -4000000 | -65000 | -800000 | -3868928 | 66072 | -668928 |  | 30066.5 | 60133 | GPS:Center of Pertam:-3967231.50:-32231.50:-767231.50:#FFF10000: |  |  | 


.
<br />
## <span id="SE-colors">Colors</span>

-   **Blocks:**

<div id="color-scheme"><ul>
<li id="background"><b>Dark Blue Custom:</b> RGB(3, 9, 15), HEX(#03090F);</li>
<li id="text"><b>Light Blue Custom:</b> RGB(180, 215, 255), HEX(#B4D7FF);</li>
<li id="highlight"><b>White Smoke:</b> RGB(245, 245, 245), HEX(#F5F5F5);</li>
<li id="medgray"><b>Medium Gray:</b> RGB(150, 150, 150), HEX(#969696);</li>
<li id="shadow"><b>Dark Gray:</b> RGB(38, 38, 38), HEX(#262626);</li>
<li id="accent"><b>Gold:</b> RGB(255, 215, 0), HEX(#FFD700);</li>
<li id="accent2"><b>Yellow-Orange:</b> RGB(255, 174, 66), HEX(#FFAE42);</li>
</ul></div>

-   **Other:**
    -   Light Blue (Lights): RGB(180,215,255)
    -   Dark Blue (Display BG): RGB(3,9,15)


.
<br />
---
## <span id="SE-autolcd">Common AutoLCD Commands</span>

```
Center - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Center P O W E R
Center - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Echo
PowerStored {G:Carrier Batteries} {Batteries Stored}
Echo
PowerIn {G:Carrier Batteries} {Batteries In}
Echo
PowerOut {G:Carrier Batteries} {Batteries Out}
```
```
Center - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Center T A N K S
Center - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Echo 
Tanks * Hydrogen
Echo
Tanks * Oxygen
```
```
Center - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Center C A R G O
Center - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -
Cargo {G:Cargo Containers}
Echo ---   ---   ---   ---   ---   ---   ---   ---   ---
InvListX * all
```

## <span id="SE-other">Other</span>


<br />

---
# <span id="SE-station-registry">Station Registry</span>

- Station name/number (As indicated on the remote control block)
- Station Type (See [naming convention][3-05])
- Location (GPS on the remote control block)

| Station Name | Station Type | GPS Location |
| --- | --- | --- |
| SpaceStation01 | 


.
<br />

# <span id="SE-ship-registry">Ship Registry</span>

- Ship name/number
- Location (ship name if assigned to a carrier)
- Ship type (blueprint name)

| Ship Name | Assigned Location | Ship Type |
| --- | --- | --- |
| **Utility Ships** |
| AT-001 | CVU-001 | M80 Tug |
| AT-002 | CVU-002 | M80 Tug |
| AT-003 | AKL-001 | M80 Tug |
| AT-004 | AKL-001 | M80 Tug |
| LCU-001 | Earth-like Orbit | M80 Heavy Lander |
| **Cargo Ships** |
| AKL-001 | Earth-like Orbit | M80 Super Heavy Freighter |
| AKM-001 | Earth-like Orbit | M80 Heavy Freighter |
| AKS-001 | Earth-like Orbit | M80 Light Freighter |
| **Mining Carriers** |
| CVU-001 | Earth-like Orbit | M80 Mining Carrier |
| CVU-002 | Earth-like Orbit | M80 Mining Carrier |
| **Mining Ships** *(cockpit)* |
| MSH-001 | CVU-001 | M80 Hydro Mining Ship |
| MSH-002 | CVU-001 | M80 Hydro Mining Ship |
| MSH-003 | CVU-001 | M80 Hydro Mining Ship |
| MSH-004 | CVU-001 | M80 Hydro Mining Ship |
| MSH-005 | CVU-001 | M80 Hydro Mining Ship |
| MSH-006 | CVU-001 | M80 Hydro Mining Ship |
| MSH-007 | CVU-001 | M80 Hydro Mining Ship |
| MSH-008 | CVU-001 | M80 Hydro Mining Ship |
| MSH-009 | CVU-002 | M80 Hydro Mining Ship |
| MSH-010 | CVU-002 | M80 Hydro Mining Ship |
| MSH-011 | CVU-002 | M80 Hydro Mining Ship |
| MSH-012 | CVU-002 | M80 Hydro Mining Ship |
| MSH-013 | CVU-002 | M80 Hydro Mining Ship |
| MSH-014 | CVU-002 | M80 Hydro Mining Ship |
| MSH-015 | CVU-002 | M80 Hydro Mining Ship |
| MSH-016 | CVU-002 | M80 Hydro Mining Ship |
| MSI-001 | AKL-001 | M80 Ion Mining Ship |
| MSI-002 | AKL-001 | M80 Ion Mining Ship |
| **Mining Drones** *(no cockpit)* |
| --- | --- | --- |


## <span id="SE-naming-convention">Naming Convention</span>
**Stations**
-   PD: Production Depot
-   RC: Refueling Center
-   RP: Respawn Point
-   SY: Shipyard

**Ships**
-   ARS: Rescue and Salvage Ship
-   AKS: Cargo Ship, Small
-   AKM: Cargo Ship, Medium
-   AKL: Cargo Ship, Large
-   AP: Transport
-   AR: Repair Ship (welder)
-   ATF: Fleet Tug
-   ATR: Rescue Tug
-   ATY: Yard Tug
-   CVU: Carrier Utility
-   LCU: Landing Craft Utility
-   MSH: Mining Ship, Hydrogen
-   MSI: Mining Ship, Ion
-   MDH: Mining Drone, Hydrogen
-   MDI: Mining Drone, Ion


## <span id="SE-fleet-blueprints">Fleet Blueprints</span>

-   M80 Yard Tug \[ATY-###]
-   ***M80 Fleet Tug \[ATF-###] (not exists)***
-   M80 Super Heavy Freighter \[AKL-###]
-   M80 Heavy Freighter \[AKM-###]
-   ***M80 Light Freighter \[AKS-###] (not exists)***
-   M80 Mining Carrier \[CVU-###]
-   M80 Hydro Mining Ship \[MSH-###]
-   M80 Ion Mining Ship \[MSI-###]
-   ***M80 Hydro Mining Drone \[MDH-###] (not exists)***
-   ***M80 Ion Mining Drone \[MDI-###] (not exists)***



.

<br />

<!-- reference links -->
[3-01]: #SE-todo
[3-02]: #SE-networkedgrids
[3-03]: #SE-laserantennae
[3-04]: #SE-coords
[3-05]: #SE-naming-convention
[3-06]: #SE-colors
[3-07]: #SE-autolcd
[3-08]: #SE-other
[3-09]: #SE-ship-registry
[3-10]: #SE-fleet-blueprints
[3-11]: #SE-station-registry
<!-- end reference links -->