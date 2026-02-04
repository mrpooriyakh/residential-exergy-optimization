# Exergoeconomic Optimization of Hybrid Renewable Residential Energy Systems

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Julia](https://img.shields.io/badge/Julia-1.10-blue.svg)](https://julialang.org/)

Unified framework integrating second-law thermodynamics with techno-economic modeling for optimal design of residential hybrid renewable energy systems.

## 📄 Paper

**Title:** A Unified Exergy-Economic Framework for Optimal Design of Hybrid Renewable Residential Energy Systems

**Authors:** Pooriya Khodaparast, Seyed Emad Hosseini, Kimia Rasouli-keshvar, Mahan Ahmadi, Dr. Saeed Talebi

**Institution:** Amirkabir University of Technology, Department of Energy Engineering and Physics

## 🎯 Key Features

- **Second-law thermodynamic analysis** revealing 95% exergy waste in conventional grid-only systems
- **Multi-scenario optimization**: BAU (subsidized), EMIS (emission-constrained), COST (market pricing)
- **Component-level exergy destruction** tracking across all technologies
- **Comprehensive system integration**: PV, wind, battery, PCM storage, heat pumps, grid, furnace
- **8760-hour optimization** with hourly resolution
- **Julia/JuMP implementation** using HiGHS MILP solver

## 📊 Key Results

| Scenario | PV Capacity | Battery | Emissions | Cost | Exergy Efficiency |
|----------|-------------|---------|-----------|------|-------------------|
| BAU | 0 kW | 0 kWh | +5,294 kg | $584 | 4.95% |
| EMIS | 4.8 kW | 1.3 kWh | +950 kg | $2,033 | 5.44% |
| COST | 7.2 kW | 10.1 kWh | -2,035 kg | $5,588 | 5.78% |

## 🚀 Quick Start

### Prerequisites
- Julia 1.10+
- JuMP.jl
- HiGHS.jl
- XLSX.jl
- DataFrames.jl

### Installation
```julia
using Pkg
Pkg.add(["JuMP", "HiGHS", "XLSX", "DataFrames"])
```

### Running Optimization
```julia
include("optimization_model.jl")
# Results exported to optimization_results_YYYY-MM-DD_HHMMSS.xlsx
```

## 📁 Repository Structure
```
├── optimization_model.ipynb    # Main optimization framework
├── heat_pump.ipynb            # Heat pump component model
├── solar_pv.ipynb             # Photovoltaic model
├── battery_storage.ipynb      # Battery storage model
├── pcm_storage.ipynb          # PCM thermal storage model
├── gas_furnace.ipynb          # Natural gas furnace model
├── wind_turbine.ipynb         # Wind turbine model
├── solar_thermal.ipynb        # Solar thermal collector model
├── grid_electricity.ipynb     # Grid electricity model
├── data/                      # Input data (weather, demand)
├── results/                   # Optimization results
└── paper/                     # LaTeX source for paper
```

## 📈 Main Contributions

1. **Unified exergoeconomic framework** integrating all major residential energy technologies
2. **Second-law analysis** revealing hidden inefficiencies (71% energy vs. 5% exergy efficiency)
3. **Policy insights**: Pricing reform more effective than emission mandates for voluntary decarbonization
4. **Marginal abatement cost analysis**: $676-1,405/tonne CO₂ under different scenarios

## 🔬 Methodology

- **Optimization:** Mixed-Integer Linear Programming (MILP)
- **Solver:** HiGHS
- **Horizon:** 8760 hours (1-year, hourly resolution)
- **Location:** Tehran, Iran (TMY weather data)
- **Building:** 183 m² apartment, mid-floor


## 📜 License

This project is licensed under the MIT License - see LICENSE file for details.

## 🙏 Acknowledgments

- Amirkabir University of Technology, Department of Energy Engineering and Physics
