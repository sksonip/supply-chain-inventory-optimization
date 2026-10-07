# Supply Chain Inventory Optimization

**Status: project proposal. Implementation is not available in this repository.**

This repository outlines an inventory-policy experiment. It currently contains documentation, a dependency list, and a license; it does not contain a working optimization engine, reinforcement-learning agent, simulation, or dashboard.

## Proposed scope

Start with a reproducible comparison of EOQ/reorder-point and (s, S) policies on clearly labelled synthetic demand. Define demand variability, lead time, holding/ordering/shortage costs, and the service-level target before considering an RL extension.

## Evidence required before reporting results

- Runnable simulation and documented input assumptions.
- A baseline policy and independent evaluation scenarios.
- Cost breakdown, fill rate, stockout frequency, and uncertainty across seeds.
- Saved outputs and exact commands to reproduce the comparison.

No cost savings, service-level improvement, or stockout reduction has been validated here. Earlier numerical claims and examples referencing absent implementation files have been removed.

## License

Repository materials are provided under the [MIT License](LICENSE).

Maintained by [Satish Kumar Soni](https://github.com/sksonip).
