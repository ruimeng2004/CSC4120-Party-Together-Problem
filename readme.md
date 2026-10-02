# CSC4120 Project — Party Together Problem

This repository contains my complete implementation of the **Party Together Problem (PTP)** project for **CSC4120, Fall 2025**.

The project finds a driving route and pickup locations for a group of friends, balancing driving cost and walking distance. The car starts and ends at location `0`, and each friend is picked up at their home or a neighboring location.

## Implementation

- **Metric TSP:** An exact Held–Karp dynamic programming solver.
- **Home Pickup (PHP):** A solver that reduces home pickup to Metric TSP and expands the result into a route on the original graph.
- **Party Together (PTP):** A local-search heuristic with pickup assignment and feasibility repair.
- **Interactive CLI:** Input validation, solver execution, solution checking, and cost evaluation.

The repository also includes sample inputs, saved outputs, a notebook, and my [project report](report.pdf). The original [project specification](proj_description%202025b.pdf) is included for reference.

## Setup and Usage

Install the dependencies and start the client from the repository root:

```bash
python3 -m pip install networkx matplotlib
python3 main.py
```

Available commands:

| Command | Description |
| --- | --- |
| `ls_input` | List available input files. |
| `ck_input` | Validate student-created inputs. |
| `test_php` / `test_ptp` | Run a solver on selected inputs. |
| `test_php_all` / `test_ptp_all` | Run a solver on all inputs. |
| `--help` | Show help. |
| `exit` | Quit the client. |

When prompted, enter input filenames such as `1.in 2.in`. PTP solutions are saved to `outputs/`.
