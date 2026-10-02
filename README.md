# EV Battery Thermal Degradation Model 🔋

A computational simulation predicting the thermal response of a lithium-ion battery cell during a 60-second high-load acceleration run.

### ⚙️ Physical Foundation: Lumped Capacitance Model
This Python script utilizes a lumped capacitance heat transfer model to simulate battery thermals. It calculates the net temperature increase by evaluating the heat generated via internal electrical resistance against the heat removed by an active cooling system.

**The core governing logic:**
`Net Heat = (Current² × Resistance) - Cooling Rate`
`Δ Temperature = Net Heat / (Mass × Specific Heat)`

### 🧪 Simulation Parameters
* **Initial Temperature:** 25.0 °C
* **Current Draw:** 150.0 A (Hard acceleration)
* **Internal Resistance:** 0.005 Ω
* **Cell Mass:** 1.2 kg
* **Specific Heat Capacity:** 850 J/(kg·°C)
* **Active Cooling Rate:** 5.0 J/s
* **Critical Safety Threshold:** 60.0 °C

### 📊 Results
The model loops through a 60-second timeline, outputting temperature increments every 10 seconds. 
* **Final Computed Temperature:** 31.32 °C 
* **Status:** Safe (Under the 60.0 °C degradation threshold).

---
*Built as a foundational project bridging mechanical thermodynamics with Python computational logic for modern electromobility applications.*
