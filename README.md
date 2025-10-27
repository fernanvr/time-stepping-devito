# Multi-Stage Time Stepping with Devito

This repository contains a Jupyter notebook implementing a multi-stage Runge-Kutta-like time integration scheme for solving PDE systems using [Devito](https://www.devitoproject.org/).

## Overview

The notebook demonstrates a **Multi-Stage Minimum Failure Example (MFE) Time Stepping Simulation** that implements high-order time integration methods for partial differential equations.

### Key Features

- **Multi-stage Runge-Kutta time integration** for PDE systems
- **Source term handling** with Taylor series expansion
- **Strong Stability Preserving Runge-Kutta (SSPRK)** coefficients
- **Devito-based finite difference implementation**
- **2D wave equation** example with multiple source terms

## Mathematical Foundation

The method formulates PDE systems as first-order in time:

```
∂U/∂t = HU + f(x,t)
```

where the solution is approximated using matrix exponentials and multi-stage Runge-Kutta methods following the approach from:

1. Al-Mohy AH, Higham NJ (2010) - Matrix exponential algorithms
2. Gottlieb S, Gottlieb LAJ (2003) - Strong stability preserving Runge-Kutta methods

## Files

- `MFE_time_size.ipynb` - Main Jupyter notebook with complete implementation

## Requirements

- Python 3.7+
- NumPy
- SymPy
- [Devito](https://github.com/devitocodes/devito)

## Installation

1. Install Devito following the [official installation guide](https://www.devitoproject.org/devito/download.html)
2. Clone this repository:
   ```bash
   git clone https://github.com/fernanvr/time-stepping-devito.git
   cd time-stepping-devito
   ```
3. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook MFE_time_size.ipynb
   ```

## Usage

The notebook is self-contained and includes:

1. **Environmental setup** - Grid and variable configuration
2. **PDE system definition** - Wave equation with source terms
3. **Source derivatives computation** - Symbolic differentiation
4. **Operator construction** - Multi-stage method implementation
5. **Simulation execution** - Running the Devito operator

Simply run all cells in sequence to execute the complete simulation.

## Methodology

The implementation follows these key steps:

1. Formulate the PDE system as first-order in time
2. Expand source terms using Taylor series
3. Apply multi-stage Runge-Kutta integration
4. Use Devito for efficient finite difference computation

## Results

The simulation produces time-evolved wavefields demonstrating the effectiveness of the multi-stage time integration approach for wave propagation problems.

## License

This project is open source. Please cite the relevant papers when using this code in academic work.

## Author

Fernando V. R. - [GitHub](https://github.com/fernanvr)

## References

- Al-Mohy AH, Higham NJ (2010) A new scaling and squaring algorithm for the matrix exponential. SIAM Journal on Matrix Analysis and Applications 31(3):970–989
- Gottlieb S, Gottlieb LAJ (2003) Strong stability preserving properties of runge–kutta time discretization methods for linear constant coefficient operators. Journal of Scientific Computing 18(1):83–109