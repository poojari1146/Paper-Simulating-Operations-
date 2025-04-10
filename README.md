🍛 Simulating Operations of a Troy Indian Fast-Food Restaurant<br>
| A discrete-event simulation project to optimize staff allocation, reduce wait times, and improve service efficiency at a high-traffic Indian fast-food restaurant in Troy, MI.

🏪 About the Restaurant<br>
The restaurant is a popular Indian fast-food establishment located in Troy, Michigan, serving a large dine-in and online customer base. It operates from 11:00 AM to 9:30 PM on weekdays and till 10:00 PM on weekends. Known for its wide variety of dishes, the restaurant faces long customer wait times during peak hours, especially on weekends.

🎯 Project Objective<br>
To simulate the real-world operations of the restaurant and:<br>
- Compare weekday and weekend performance
- Evaluate wait times, queue lengths, and resource utilization
- Experiment with staffing adjustments and operational changes
- Propose strategies to reduce congestion and improve customer experience

🧪 Simulation Scenarios Modeled<br>
Scenario 1: Baseline Comparison<br>
- Same staff configuration on weekdays and weekends
- Measured differences in customer wait times and staff utilization
Scenario 2: Dynamic Factors Introduced<br>
- Changes in online order share, order mix, operating hours, and customer arrival rates between weekday and weekend
Scenario 3: Operational Improvements Tested<br>
- Added extra staff at cash register and food counters
- Extended shop hours
- Observed impact on weekend congestion and service time

🛠 Data Collection & Assumptions<br>
- Sources: Observations, manager interviews, stopwatch timing
- Process times collected for cashier and food prep stations
- Order sizes categorized as: Small, Medium, Party
- Customer behavior modeled:
  - Balking: Customers leave if order line is too long
  - Reneging: Customers leave if dining area is full and wait exceeds 5 minutes
- Failures included: POS/credit system failure every 2 weeks

🧩 Model Structure (Built using Simio)<br>
 🧍 Entities<br>
- Dine-in and Online Customers (color-coded for clarity)
- Orders are treated as copies of customer entities with mapped preferences<br>
📈 Order Flow & Logic<br>
- Orders split by category: Chat/Sandwich, Roti/Dosa, Chinese
- Customers may order from 1, 2, or all 3 stations
- 25% orders come online, delayed strategically during busy dine-in periods
- Plating & packaging times depend on order size and type<br>
🔄 Key Features<br>
- Matching & combining logic to associate orders with the right customer
- Queue limits, balking/reneging logic
- Dining room capacity limited to 50
- Online wait logic delays execution if dine-in queue exceeds threshold

📊 Performance Metrics Captured<br>
- Average wait time per customer
- Queue lengths across stations
- Utilization of staff at cash counters and food stations
- Comparison of weekday vs weekend efficiency
- Impact of added resources in scenario 3

✅ Recommendations<br>
- Add extra staff at cash counter and busiest food stations on weekends
- Extend store hours slightly on weekends to ease congestion
- Introduce priority handling for online orders during peak times
- Digitize laundromat & back-end processes for better data insights
- Explore demand forecasting for inventory and staffing

🔮 Future Work<br>
- Model parking lot capacity and washroom availability
- Analyze customer churn due to overcrowding
- Integrate delivery service coordination
- Use historical data to add forecasting layers for better scheduling
- Under supervision of Prof. Edward Williams

🛠 Tools & Concepts Used<br>
- Simio (Discrete-event simulation)
- Queue modeling, service distributions
- Process logic, entity duplication, conditional flows
- Data collection through observation and validation



