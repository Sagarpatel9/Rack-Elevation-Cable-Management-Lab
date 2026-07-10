# Rack & cable labeling scheme

This doc defines the naming convention used across Rack-01, based on the
structured-cabling administration approach in TIA/EIA-606, applied to the
physical layout designed in TIA-942.

## Why label at all

An unlabeled rack is unmaintainable even if it's wired perfectly. A
structured label lets anyone standing anywhere in the data center, holding
a loose cable, immediately identify which rack, which panel, and which
port it belongs to — without a spreadsheet or a walk-around.

## Device naming

Every device follows the pattern:

```
R{rack}-{role}-{group}-{index}
```

| Example | Breakdown |
|---|---|
| `R01-PP-Copper-A` | Rack 01, Patch Panel, Copper group, panel A |
| `R01-PP-Fiber-A` | Rack 01, Patch Panel, Fiber group, panel A |
| `R01-SW01` | Rack 01, Switch, unit 01 |
| `R01-CM-01` | Rack 01, Cable Manager, unit 01 |
| `R01-SRV-APP-01` | Rack 01, Server, App role, unit 01 |
| `R01-SRV-DB-01` | Rack 01, Server, DB role, unit 01 |
| `R01-SRV-05` | Rack 01, Server, generic/unnumbered role, unit 05 |

## Port naming

Every patch panel port follows the pattern:

```
R{rack}-{panel}-P{port}
```

Example: `R01-PPA-P01` reads as **Rack 01, Patch Panel A, Port 1** —
readable cold, with no lookup required.

## Cable labels (both ends)

Every physical cable is labeled at both ends, showing both endpoints:

```
R01-PPA-P01 <-> R01-SW01-P01
```

Labeling both ends serves as a built-in verification check — if a cable's
two physical ends ever disagree with what's recorded in NetBox, that's an
immediate signal something was mis-cabled or mis-documented.

## Cable type conventions

| Type | Used for |
|---|---|
| Cat6a | All server-to-switch links, the DB replication jumper, and the copper uplink |
| Single-mode fiber (SMF) | The fiber uplink from the switch to the building network |

## Applying this scheme in NetBox

NetBox's Cables feature stores both endpoints natively (Device + Interface/
Port on each side), so the "both ends visible" requirement above is
enforced structurally rather than by convention alone — clicking any port
shows a full cable trace to the other end.
