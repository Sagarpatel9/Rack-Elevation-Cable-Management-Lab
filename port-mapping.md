# Port mapping

The same data as [`port-mapping.xlsx`](./port-mapping.xlsx), in markdown
so it renders directly on GitHub without needing a download. The xlsx
remains the source file; this is a browsable copy.

## Cable connections

| Cable ID | Rack | A-Side Device | A-Side Port/Interface | B-Side Device | B-Side Port/Interface | Cable Type | Connection Purpose | Status |
|---|---|---|---|---|---|---|---|---|
| 137 | R01 | R01-SRV-APP-01 | Gig-E 1 | R01-SW01 | ge-0/0/0 | Cat6a | Server -> switch (data) | Connected |
| 138 | R01 | R01-SRV-APP-02 | Gig-E 1 | R01-SW01 | ge-0/0/1 | Cat6a | Server -> switch (data) | Connected |
| 139 | R01 | R01-SRV-DB-01 | Gig-E 1 | R01-SW01 | ge-0/0/2 | Cat6a | Server -> switch (data) | Connected |
| 140 | R01 | R01-SRV-DB-02 | Gig-E 1 | R01-SW01 | ge-0/0/3 | Cat6a | Server -> switch (data) | Connected |
| 141 | R01 | R01-SRV-APP-03 | Gig-E 1 | R01-SW01 | ge-0/0/4 | Cat6a | Server -> switch (data) | Connected |
| 142 | R01 | R01-SRV-APP-04 | Gig-E 1 | R01-SW01 | ge-0/0/5 | Cat6a | Server -> switch (data) | Connected |
| 143 | R01 | R01-SRV-05 | Gig-E 1 | R01-SW01 | ge-0/0/6 | Cat6a | Server -> switch (data) | Connected |
| 144 | R01 | R01-SRV-06 | Gig-E 1 | R01-SW01 | ge-0/0/7 | Cat6a | Server -> switch (data) | Connected |
| 145 | R01 | R01-SRV-07 | Gig-E 1 | R01-SW01 | ge-0/0/8 | Cat6a | Server -> switch (data) | Connected |
| 146 | R01 | R01-SRV-DB-01 | Gig-E 2 | R01-SRV-DB-02 | Gig-E 2 | Cat6a | DB replication jumper (direct, bypasses switch) | Connected |
| 147 | R01 | R01-SW01 | ge-0/0/9 | R01-PP-Copper-A | Port 01 | Cat6a | Switch uplink -> copper patch panel (building network) | Connected |
| 148 | R01 | R01-SW01 | ge-0/0/10 | R01-PP-Fiber-A | Port 01 | SMF (planned) | Switch uplink -> fiber patch panel (building network) | Connected |

## Unused capacity

| Category | Total | Used | Free | Notes |
|---|---|---|---|---|
| Rack U-space | 42 | 26 | 16 | U19-U1 reserved for growth |
| Switch ports (ge-0/0/x) | 48 | 11 | 37 | 9 servers + 2 uplinks used |
| Copper patch panel ports | 48 | 1 | 47 | Only Port 01 used (uplink) |
| Fiber patch panel ports | 24 | 1 | 23 | Only Port 01 used (uplink) |
