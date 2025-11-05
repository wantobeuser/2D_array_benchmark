# Benchmark Description
To emulate a practical HBM4 routing environment, we developed a new bus routing benchmark by extending the ICCAD 2018 benchmark[1]. We provide a set of 18 routing benchmarks designed to evaluate bus routing under different I/O port configurations:

### 1D_placed_designs (Total 9 comparisons)
  - bus_design_XX
      - bus_XX_def.tar.gz
      - bus_XX.png
  - 9 benchmarks with conventional boundary I/O ports

### 2D_placed_designs (Total 9 benchmarks)
  - bus_design_XX
      - bus_XX_def.tar.gz
      - bus_XX.png
  - 9 benchmarks with 2D-array I/O port structures
        
These benchmarks are derived from the original bus and blockage patterns and extended to introduce a 2D port placement scheme. All benchmark layouts were implemented using a commercial Place-and-Route (P&R) tool. The 2D I/O benchmarks were constructed through custom DEF generation.

## Bus Configuration
Each benchmark includes combinations of four bus widths:
- 8-bit, 16-bit, 32-bit, and 64-bit
- The number of buses is varied to represent different routing congestion scenarios.

## Port Placement Structure
- Boundary I/O Benchmarks: All input/output ports are placed along the die boundary.
- 2D Port Benchmarks:
  - Input ports remain on the die boundary.
  - Output ports are placed inside the die as 2D-array ports, modeled after TSV-based connections.
  - Each 2D port uses a 5 × 5 µm² metal pad on the M5 layer, matching top BEOL via dimensions and routing track pitch.

## Routing and Blockage Configuration
- Routing uses four metal layers (M3–M6).
- Ports are located on M5.
- Routing blockages are inserted on M3 and M4 to represent already-utilized routing resources from logic placement, effectively constraining available routing space for buses.

# Reference
[1] A. Liao, H. Chang, O. Chi, and J. Wang. (2018). ”ICCAD 2018 CAD Contest Obstacle-Aware On-Track Bus Routing” [Online]. Available: http://iccad-contest.org/2018/Problem B/2018ICCADContest ProblemB.pdf
