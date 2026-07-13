# CS303 — Digital Logic System Design

Term project: a **lab timer** built at the gate level — no HDL, no microcontroller, just
combinational logic and flip-flops wired by hand.

## The circuit

`Term Project/labtimer.dig` is the design. It's a synchronous sequential circuit built from
roughly:

| Component | Count |
|---|---|
| AND gates | 96 |
| Multiplexers | 64 |
| OR gates | 41 |
| D flip-flops | 21 |
| NOT / NOR / XOR | 24 |

The 21 D flip-flops hold the timer's state (count registers plus the control FSM); the
multiplexer bank handles load/count/hold selection, and the gate network implements the
next-state and output logic.

`Term Project/testbench.dig` drives the design and checks its behavior.

## Running it

These are [**Digital**](https://github.com/hneemann/Digital) circuit files — a free
gate-level simulator. Install it, then open `Term Project/labtimer.dig` and hit run, or open
`testbench.dig` to execute the test vectors against the design.

## Spec

The assignment brief is included: `Term Project/CS303_term_project_2025.pdf`.
