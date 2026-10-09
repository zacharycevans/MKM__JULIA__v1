## Example: Acetic Acid Decomposition on Pd(111)

The `sample` directory contains an example simulation of acetic acid decomposition on a Pd(111) catalyst surface.

This example uses **coverage-independent reaction energetics and rate constants**. Although the full modeling framework supports coverage-dependent energetics and interpolation, those capabilities are not exercised in this particular example.

### Example Configuration

The simulation is defined in `AcOH_Decomp_01.xml`, which specifies the chemical species, surface configurations, reaction network, simulation conditions, and numerical options.

The example investigates reaction kinetics under low-pressure conditions, with an acetic acid partial pressure of 1 mbar.

### Included Results

The example includes numerical outputs for:

- Species fractions and their evolution over time
- Species production and consumption rates
- Reaction-pair rates
- Degrees of rate control (DRC)
- Degrees of selectivity control (DSC), comparing CO₂ and CO
- Simulation diagnostics and execution logs

These results illustrate the framework's capabilities for analyzing catalytic reaction networks and identifying kinetically influential processes.

### Scope

This example demonstrates the coverage-independent microkinetic modeling and sensitivity-analysis capabilities of the software. It should not be interpreted as a demonstration or validation of the coverage-dependent interpolation functionality.
