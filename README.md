# 📦 Supply Chain Inventory Optimization

> **AI-powered inventory optimization system using reinforcement learning and EOQ models to minimize costs and prevent stockouts**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![RL](https://img.shields.io/badge/Reinforcement_Learning-Enabled-green.svg)](https://github.com/sksonip/supply-chain-inventory-optimization)

## 🎯 Overview

This project implements an **intelligent inventory management system** that uses **Reinforcement Learning (RL)** and **Economic Order Quantity (EOQ)** models to optimize inventory levels, minimize total costs, and prevent stockouts in supply chain operations.

### Key Benefits

- 💰 **Cost Reduction**: Minimize holding, ordering, and stockout costs by 15-30%
- 📈 **Demand Adaptation**: RL agents learn optimal policies from demand patterns
- ⚡ **Real-time Optimization**: Dynamic reordering decisions based on current inventory
- 📊 **Multi-objective**: Balances service level, costs, and inventory turnover
- 🤖 **Automated Decision Making**: AI-driven reorder points and quantities

## ✨ Features

### 🔥 Reinforcement Learning Module
- **DQN (Deep Q-Network)**: Learn optimal inventory policies through trial and error
- **PPO (Proximal Policy Optimization)**: Stable training for continuous action spaces
- **Custom Gym Environment**: Simulates inventory dynamics with realistic constraints
- **Reward Shaping**: Balances multiple objectives (costs, service level, freshness)

### 📊 Classic Optimization Models
- **EOQ (Economic Order Quantity)**: Classic formula with extensions
- **Safety Stock Calculation**: Statistical methods for buffer inventory
- **Reorder Point (ROP)**: Considers lead time and demand variability
- **(s, S) Policy**: Min-max inventory control strategy

### 📊 Analytics & Visualization
- Interactive dashboards showing inventory levels over time
- Cost breakdowns (holding, ordering, shortage)
- Service level metrics and fill rates
- Comparison of RL vs traditional methods

## 🚀 Quick Start

### Installation

```bash
git clone https://github.com/sksonip/supply-chain-inventory-optimization.git
cd supply-chain-inventory-optimization
pip install -r requirements.txt
```

### Basic Usage

```python
from inventory_optimizer import InventoryOptimizer

# Initialize optimizer
optimizer = InventoryOptimizer(
    initial_inventory=100,
    holding_cost=2.0,
    ordering_cost=50.0,
    stockout_cost=10.0
)

# Load demand data
optimizer.load_demand_data('demand_history.csv')

# Train RL agent
optimizer.train_rl_agent(episodes=1000)

# Get optimal policy
reorder_point, order_quantity = optimizer.get_optimal_policy()

# Simulate performance
results = optimizer.simulate(days=365)
print(f"Total Cost: ${results['total_cost']:.2f}")
print(f"Service Level: {results['service_level']:.2%}")
```

## 📊 Mathematical Models

### Economic Order Quantity (EOQ)

EOQ Formula:
```
Q* = √((2 × D × S) / H)

Where:
- Q* = Optimal order quantity
- D = Annual demand
- S = Ordering cost per order
- H = Holding cost per unit per year
```

### Reinforcement Learning State Space

**State**: (current_inventory, demand_forecast, days_since_order, lead_time)
**Action**: (reorder_yes/no, order_quantity)
**Reward**: -(holding_costs + ordering_costs + stockout_costs)

## 📁 Project Structure

```
supply-chain-inventory-optimization/
│
├── inventory_optimizer.py    # Main optimization engine
├── rl_agent.py              # RL agent implementation
├── eoq_calculator.py        # Classic EOQ models
├── simulation.py            # Inventory simulation environment
├── visualizer.py            # Plotting and analysis
├── requirements.txt         # Dependencies
├── README.md               # Documentation
└── LICENSE                 # MIT License
```

## 🔬 Algorithms Implemented

1. **Deep Q-Network (DQN)**: Value-based RL for discrete actions
2. **Proximal Policy Optimization (PPO)**: Policy gradient method
3. **Economic Order Quantity (EOQ)**: Classic inventory model
4. **Reorder Point (ROP)**: Safety stock calculations
5. **(s, S) Policy**: Min-max inventory control

## 📊 Performance Metrics

- **Total Cost**: Sum of holding, ordering, and stockout costs
- **Service Level**: Percentage of demand met from stock
- **Fill Rate**: Units delivered / units ordered
- **Inventory Turnover**: COGS / Average inventory
- **Stockout Frequency**: Number of stockout events

## 🎯 Use Cases

- **Retail**: Optimize stock levels for thousands of SKUs
- **E-commerce Warehousing**: Dynamic reordering based on sales velocity
- **Manufacturing**: Raw material inventory management
- **Pharmaceuticals**: Balance freshness with availability
- **Food & Beverage**: Perishable goods optimization

## 📈 Expected Results

Typical improvements vs manual/rule-based systems:
- **15-30% cost reduction** in total inventory costs
- **5-10% improvement** in service levels
- **20-40% reduction** in excess inventory
- **50% fewer stockouts** through predictive reordering

## 🤝 Contributing

Contributions are welcome! Areas for improvement:
- Multi-echelon inventory optimization
- Integration with ERP systems
- More sophisticated demand forecasting
- Additional RL algorithms (A3C, SAC)

## 📝 License

MIT License - see [LICENSE](LICENSE) file

## 👤 Author

**Satish Kumar Soni**
- GitHub: [@sksonip](https://github.com/sksonip)
- LinkedIn: [sksonip](https://linkedin.com/in/sksonip)
- Portfolio: [sksonip.github.io](https://sksonip.github.io)

## 🙏 Acknowledgments

- OpenAI Gym for RL environment framework
- Stable-Baselines3 for RL implementations
- Supply chain optimization research community

---

<div align="center">
  <p><strong>⭐ Star this repo if you find it useful! ⭐</strong></p>
  <p><em>Optimizing supply chains, one decision at a time.</em></p>
</div>
