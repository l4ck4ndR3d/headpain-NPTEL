# Logistics & Supply Chain Management — Exam Notes (Decade 6: Lectures 51–60)

**Course:** NPTEL Online Certification — Logistics & Supply Chain Management
**Instructor:** Dr. Vikas Thakur, Assistant Professor, Department of Humanities & Social Sciences, IIT Kharagpur

> These notes are compiled strictly from the professor's lectures (Lec51–Lec60). All definitions, figures, and examples are the ones used by the professor in the sessions.

---

## Lecture 51 — Assignment Problem Programming

### 51.1 Concept and Context
- The **assignment problem** is taken from **Operations Research** and is a **special case of the transportation problem**: instead of deciding which factory ships to which market, we assign **tasks to people/resources/machines** (or **markets to factories**) so that the overall scenario is optimized.
- **Objective:** minimize the total cost, or if a **profit function** is used, maximize profit.
- Solved using the **Hungarian method**.
- Why needed: resources are **limited** in capacity (manpower, machines, factories). We assign **workers to machines**, **markets to factories** (from where material is transported), and **salesmen to sales areas**.
- Assignment is not only about the job requirement but also about the **resource side** — you must know the **skills and talent** of available manpower to match job requirements.
- If there are **n jobs** and **n persons**, the number of tasks must equal the number of allocation points.
- **Basic assumption:** the **per-unit cost** of assigning each job to each resource is known. Only one assignment is done — **one person is assigned only one job**; two jobs cannot go to one person (same for machines).

### 51.2 Matrix Representation
- **Resources on rows** (man m1, m2 … mn / machines) and **tasks/jobs on columns** (job 1, 2 … n).
- **c_ij** = cost of assigning resource i to task j; e.g. **c_11** = cost of assigning job 1 to man/machine 1.
- Decision variable **x_ij** = **1** if assigned, else **0**; objective function = **Σ c_ij x_ij** (minimize), or **p_ij** (profit, maximize).
- Only one assignment in one row and one column → the sum of each row and each column is always **1**.
- **Balanced problem** = **square matrix** (3 machines, 3 jobs). **Unbalanced problem** = rows ≠ columns; convert by adding a **dummy row or dummy column**.
- **Maximization → minimization:** subtract all cell values from the **largest value** in the matrix, or multiply all cell values by **−1**; then follow the same algorithm.

### 51.3 Hungarian Method — Steps
1. **Develop the cost table** (fill all assignment cost cells).
2. If not balanced, **add a dummy row/column** with cost values **0 0 0**.
3. Find the **opportunity cost table**: subtract the **row minimum** from all values in each row, then the **column minimum** from each column → at least one **0** in every row and column.
4. **Make assignments:** examine rows successively — if a row has exactly **one 0**, circle it, assign that cell, and **strike off** other 0s in that row/column; if more than one 0, leave the row. Then do the same column-wise.
5. **Optimality:** if the number of allocations = **order of matrix** (each row and column gets a single allotment), it is the **optimal solution**.
6. If allocations < order of matrix, **revise the opportunity cost table** and iterate.

### 51.4 Revising a Non-Optimal Solution
- **Mark** each row that has **no assignment**; examine marked rows and **tick columns** containing assigned zeros; tick the rows containing those assigned zeros in the marked columns; repeat until no more rows/columns can be marked.
- Draw the **minimum number of straight lines** through each **marked column** and each **unmarked row** so that **all zeros are covered**.
- Among cells **not covered by any line**, choose the **smallest element**; **subtract** it from all uncovered cells; **add** it at the **intersection of two lines**; cells covered by one line remain unchanged.
- Re-do the assignment; keep iterating until number of allocations = order of matrix.

### 51.5 Worked Examples
- **Programmers example:** three programs A, B, C to three programmers. Cost if A → person 1 = **₹120**; B → programmer = **₹100**; C → programmer 2 = **₹110**. Row minima 80, 80, 110; after the opportunity cost table, assignment = **C → person 1, B → person 2, A → person 3** (costs 80 + 90 + 110). Allocations 3 = order 3 → **optimal**.
- **Unbalanced example:** **5 machines, 4 jobs** → add **one dummy job** with costs **0 0 0**. Row minima 10, 1, 6, and 0 (dummy). First assignment gives only **4 allocations < order 5** → not optimal; draw **4 minimum lines** covering all zeros, subtract minimum from uncovered cells, add at the **3 intersections**; iterate to **5 allocations** = order 5.
- If the matrix holds **cost** we minimize cost; if it holds **distance** (market to factory) we minimize distance; if two cells have the **same minimum cost** (₹15 and ₹15) any assignment is acceptable — this is a special case of the transportation problem.

### 51.6 Advantages
- **Efficiency**, **minimization of cost** (transportation cost, labour cost, time) and **maximization of benefits**.
- **Dynamic optimization** — works in a dynamic environment; as real-world scenarios change you update constraints and resource capacities, so today's optimal may change tomorrow.
- **Reduction of waste** (extra time, labour, resources = waste), **enhanced productivity** (minimum time, manpower, material).
- **Clarity** — clear objective function **x_ij c_ij** with precise criterion in terms of constraints/evaluation.
- **Quantifiable matrix**, no subjectivity; **integration with constraints**; **easiness** (binary decision 1/0, no intermediate value).
- **Tabular representation**, **scalability** (small or large scale), **accessibility** (decision-making software → information-based decisions).
- **Flexibility** (alternative assignments when costs are equal), **tailored solution**, **iterative improvement**, **scenario analysis**, **sensitivity of the solution**.
- **Real-time applications** — configure constraints with real-time IoT/sensor data (workforce management), **optimal routing and scheduling**.

### 51.7 Assumptions / Limitations
- **Deterministic demand and supply** — hard to predict exactly how many jobs are required in reality.
- **Homogeneous task and resources** — not true; doing the same job by machine vs manpower differs.
- **Fixed assignment cost** — cost may fall (technology upgrade) or rise (raw material cost).
- **No intermediate stops or transshipments** — only direct assignment (factory 1 → market 10).
- **Linear relationship** — basic LP assumption; non-linear cases need non-linear programming.
- **Capacity constraints** must be known.
- **Single-period planning** — the current best solution, not a long-term one.
- **Non-negative variables only** (minus 10 manpower cannot exist).
- **Fixed origins and destinations** — but customer/market locations also change, so dynamism must be considered.

---

## Lecture 52 — Inventory Management

### 52.1 Definition of Inventory
- **Inventory** = all the items, goods, merchandise and material a business unit keeps with itself so that later it can sell them and earn profit.
- This is **not complete** — equipment is never sold, but the **raw material and spare parts used to maintain that equipment are also inventory**.
- Inventory is an **asset** — tangible or intangible — used to generate revenue and deliver value through products/services.
- In a manufacturing unit with **more than 500 stages**, when the factory closes/turns off a shift, every stage leaves some **semi-finished product** — that is also inventory.

### 52.2 Three Types and the Services Difference
- Three types managed in any manufacturing unit: **raw material**, **semi-finished goods (WIP)**, **finished goods**.
- Services **cannot make inventory** — a barber cannot store a haircut; there may be **no customer for 2 hours then 10 people in 10 minutes**. Hence in **manufacturing** we talk of **inventory management**, and in **services** we talk of **queue management** (banks, post offices).
- Services still keep inventory of **supporting products** (equipment, oils, combs, shampoos, hair dryer, massager).

### 52.3 Inventory Terms
- **Bin card** — a card/document updating the inventory of a product **within a particular bin** (e.g., on the production floor), not the whole factory.
- **Buffer stock** — stock equivalent to consumption during the **standard replenishment period**, so you are not **stock-out** and machines/people do not sit idle.
- **Committed inventory** — inventory committed/booked for a specific model/order. **Maruti Swift and Desire** use a similar tire size: 100 Desire cars need **500 tires**, 200 Swift need **1000 tires**; tires booked for that specific order.
- **Demand signal** — any demand from the market/dispatch house to move stock to the market/warehouse, which reaches the production floor.
- **Inventory ledger** — all transactions (incoming/outgoing) recorded as in accounting.
- **Lead time** — time between placing the order and receiving it; e.g., a vendor takes a **minimum 2 days** to replenish — this helps calculate safety/buffer stock.
- **Minimum stock** — the minimum quantity always available to avoid shortage = **buffer stock + safety stock**; the terms are used interchangeably (some industries treat them separately).
- **Inventory on hand** — items in stock. **Overstock** — too much inventory is dangerous (carrying cost). **Physical inventory** — checking physical stock against digital records/ledger.
- **Reordering cycle** — period between two successive regular orders. **Safety stock** — extra stock to mitigate stock-out risk from uncertainties/delays.
- **Stock card** — overall stock of a single product within the factory (bin, semi-finished, store). **Stock keeping unit (SKU)** — a unique code/nomenclature designating a single line item of a larger consignment. **Stock out** — the whole production line stops.
- **Vendor managed inventory** — the vendor takes responsibility to manage inventory at the production end; you pay them to manage and provide raw material, and they ensure no stock-out.

### 52.4 Inventory Types
- **Raw material** — items maintained in the plant, later transferred to work in progress (WIP) then finished goods. Limited lifetime → **first-come-first-serve** sequencing (move oldest first, generate capital, start customer use); shelf life (chemical industry); electrical/home appliances kept **6 months–1 year** and switched on later can get damaged.
- **Work in progress (WIP)** — semi-finished products that cannot be sold but are inventory. **Work in process** is used in manufacturing (how quickly raw material converts into semi-finished); **work in progress** is used in project management (construction, tracked with a **Gantt chart** — completing only part of an activity means lagging; ahead of schedule means extra resources deployed — both are problems).
- **Finished goods** — ready to move to market (packaging done, quality ensured); move quickly to get money — stakeholders are waiting for their margin. A **finished product for one industry is raw material for another**: for Maruti Suzuki the car is finished, but for **JK Tire / MRF / Bridgestone** the tire is their end product.
- **MRO (Maintenance, Repairing and Operating) inventory** — cleaning products, spare parts, equipment, office supplies, lab equipment, table/chair/fan/AC/printer/desktop; **never sold** but required to run operations.
- **Buffer stock** — inventory is depleted at a constant rate (practically not constant — output decreases toward lunch/tiredness); the reorder point depends on lead time and how much buffer/safety/minimum stock to keep.
- **Cycle inventory** — goods/supplies/raw material kept on hand to meet the minimum production requirement; e.g., keep **10,000 units** because another 10,000 needs **2 days** to arrive.
- **Decoupling inventory** — kept at each workstation (machines A, B, C, D, E) so if B fails, C does not sit idle.
- **Transit inventory** — inventory travelling on road/ship/air/train (e.g., **10 days** of inventory); it is not at the vendor, manufacturer, warehouse or DC, so it is **not available for selling**. **FOB (freight on board)** — once loaded on the container the ownership/responsibility goes to the **buyer**; even then, buyer cannot consume it while it travels (e.g., **5 days**).

### 52.5 Inventory Planning Process
1. **Data analysis** — figure out trends, change in demand pattern, what/when/why customers buy (in a multi-brand store, why one product is picked over another); **big data analytics** from many touch points/sensors. Stages: **what happened → why it happened → what will happen (predictive) → how to control it before it happens**.
2. **Supplier planning** — suppliers play a huge role; **vendor rating** (price, quality, delivery schedule; promised **5 days ± 1 day**); the manufacturer is responsible for improving vendors; close collaboration makes planning efficient.
3. **Safety stock calculation** — **maximum daily sales (idle situation) × maximum lead time (worst situation, e.g., 15 days in the last 10 years)** minus average daily sales × average lead time.
4. **Storage space analysis** — how much warehouse capacity exists; short-term measures, change layout for better space utilization, extend the warehouse capacity, or go for a **second/third warehouse** (new location).
5. **Inventory and forecast monitoring** — an evergreen process; **accuracy and speed** of data both matter (speed matters — share information quickly, like share markets).
6. **Optimization of inventory level** — plan inventory against warehouse capacity; a larger capacity does not mean it should always be full; avoid tying up extra capital (e.g., **₹10 crore** inventory always idle → move it to **₹2 crore**).
- Keep inventory because **supply chain disruptions** happen (weather, disaster, transportation issues, labour issues, strikes) at the vendor end, during transportation, or after receipt (lot rejected on quality), and for **sudden demand spikes**.
- **Limited cycle counts** — an annual cycle count shuts operations for at least a day; a more manageable approach is **frequent counts on select inventory**.
- **Multi-channel warehousing (omni-channel)** — orders come through different channels; maintain inventory across many warehouses and channelize stock from another warehouse if one is out of stock (two-way traffic, multiple routes).

---

## Lecture 53 — Inventory Management (Contd...)

### 53.1 Just-in-Time (JIT)
- Japanese organizations are leaders; **Toyota Motor** and the **Toyota Production System**; JIT tried somewhere in the **60s and 70s** to **increase efficiency and decrease waste**.
- Purchase/supply material **only when it is required**; no need to keep inventory (unlike **Big Bazaar / Vishal Mega Mart** one-stop stores which must keep inventory). In production houses, **zero inventory** can be defined for some **large-value items**.
- Zero inventory → **no waste** (handling/shifting damages inventory that waits for the process).
- Works when **PPC (production planning and control)** works closely with marketing/sales and trend analysis/data analytics to configure the **demand function accurately**.
- Benefits: **no money tied up**, reduced waste, **no storage requirement**, no insurance cost; **risky** — an unexpected demand spike means you cannot manage and may be **stock-out**.
- Examples: **Toyota** (reduce waste/increase efficiency; TPS is a benchmark), **Dell Computers** (build-to-order — customization only after the order; now changing model), **Harley-Davidson** (JIT to reduce inventory cost and improve product quality).
- Advantages: no inventory no cost, improved cash flow, supplier relationship (suppliers must be **physically very close**), efficiency/productivity, quality products.
- Challenges: maintaining zero inventory; **supplier dependency** (JIT is supplier-driven; supplier role **70% or more**); demand fluctuation/unpredicted demand; **high initial investment** (vendors set up units within the premises; process changes).

### 53.2 MRP (Material Requirement Planning)
- Uses different **software**; **Enterprise Resource Planning (ERP)** and **SAP solutions**.
- Used when there are **many components in huge quantity**; keeps track of every unit (production line → semi-finished → packaging → forward supply chain).
- Works when **PPC raises the bill of material (BOM)** to the store department; weekly/3-day/half-wise schedules.
- Example: **sky manufacturer** using MRP (plastic, fiberglass, wood, aluminum stock); depends heavily on sales forecast.
- Examples: **Toyota** (lean manufacturing), **Intel** (semiconductor — complex supply chain, huge plant investment), **Boeing** (thousands of parts sourced globally).
- Advantages: better control/optimal inventory level, minimize stock-out/excess, production planning (clear schedules, BOM on time), cost saving, supplier collaboration; human intervention minimized, **automated planning**.
- Challenges: **data accuracy**, **speed of data**, complexity, **flexibility** (MRP struggles with sudden change — it works because the production plan is fixed), **integration** (ERP must integrate with supply chain/warehouse/transportation software).

### 53.3 EOQ (Economic Order Quantity)
- Makes the trade-off between **holding cost** and **ordering/setup cost**. **Total cost = holding cost + setup/ordering cost**; where the total cost is minimum is the **EOQ**.
- Larger orders help negotiate price, but holding cost rises; larger orders reduce ordering cost but increase storage cost.
- Graphical: **holding cost** rises proportionally (linear — an assumption; practically per-unit cost may fall with larger space); **ordering cost** falls as order quantity rises; the **equilibrium point** where holding = ordering cost gives the minimum total cost.
- **Formula:** EOQ = **√(2 × setup/order cost × demand / holding cost)**, derived by equating holding cost = ordering cost.
- Examples: **Walmart** (largest retail giant), **Tesco** (grocery), **Samsung**, **Toyota** (manufacturing/automotive/electronics); **healthcare** (medicines, medical equipment/devices — limited life, obsoletion); **food and beverages** (**McDonald's, Starbucks, Nestle**).
- Advantages: cost minimization, efficient inventory management, simplified ordering process (repetitive routine orders; vendors aware of quantities), improved cash flow.
- Challenges: **constant demand** assumption; **fixed cost** assumption (₹10 for one order vs ₹100 for 10 is not possible); **no shortage/stock-out/back-order** assumption.

### 53.4 DSI (Days Sales of Inventory)
- The **number of days** taken to convert inventory into sales. Also called **average age of inventory, days inventory outstanding, days in inventory, days sales in inventory**.
- **Lower DSI is preferred** = quickly depleting inventory; calculated using **average inventory maintained / cost of goods sold per year**.
- Examples: **Pfizer** (pharmaceutical), **Ford Motor** (automotive — vehicles, parts, components, spare parts), **Nestle** (food and beverage).
- Advantages: optimum inventory level (balance holding vs demand), forecasting and planning (sale trends, adjust production schedules, improve demand forecasting), improved financial health.
- Challenges: industry variability, **seasonality effect** (peak/slowdown), **accounting practices** (different Cost of Goods Sold methods).

### 53.5 Zero Inventory Model
- Based on the principle of **just-in-time**; implemented by **Toyota**; possible with **zero failures** (practically impossible — at logistics, storage and raw material vendor ends) and **zero lead time** (no concept of lead time).
- Benefits: cost reduced (no carrying/holding/damage/waste/insurance cost), streamlined processes (standardized), **working capital minimum/zero**, **risk mitigation** (less inventory — e.g., **BS3/BS4 engines were banned**, bikes sold at almost **half price**), customer focus (customized product, loyal customers).
- How it works: **demand-driven production** (no forecasting, no speculative process), **pull system not push**, **small batch size**, continuous improvement, huge supplier role.
- Challenges: **market volatility**, high **supplier dependence**, need for highly efficient/reliable logistics, coordination across purchasing/production/sales, **contingency planning**, advanced systems/software, accurate real-time data.
- Examples: custom-made orders (**Raymond store** keeps the cloth piece, tailors after taking measurements); **Amazon** middlemen — not purely zero inventory (**inventory-led model** in its distribution center + zero inventory where sellers directly keep inventory).

### 53.6 Vendor Managed Inventory (VMI)
- Vendor manages inventory at the manufacturer end; the manufacturer outsources many components/raw material; the vendor is responsible for managing it.
- **Optimized performance along the supply chain** — the supplier has clear information and sole responsibility for smooth supply, with no stock-out.
- **Improved service level / long-term relationship** (as long as **Maruti Suzuki** survives, **JK Tyre / MRF** survive by selling tires).
- For the manufacturer: no point of stock-out (someone else's responsibility), **no misunderstanding in communication** (the manufacturer does not place the order — the supplier figures out how much/when is required), enhanced service level, work eliminated from the manufacturer side (purchase department).

### 53.7 ABC Analysis
- Divides the overall inventory (e.g., **1000 components**) into three categories **A, B, C**; uses the **Pareto principle (80-20 rule)**.
- **A**: minimum in numbers, **value maximum**. **B**: moderate quantity, moderate value. **C**: huge in numbers, contributing very little value.
- Example: **A** = 20% of items contributing ~**70%** of value (₹70 of every ₹100 spent); **B** = ~30% volume contributing ~**25%** (can be 30/20); **C** = large numbers contributing only ~**5%** (can be 10%). Percentages change industry to industry.

### 53.8 Inventory vs Queue Management
- Production/manufacturing → **inventory management**; services → **queue management**.
- Services cannot be inventoried for later use; the product industry can make inventory and sell later.
- Differences: physical/tangible products vs intangible services/experience; revenue model = selling products vs providing services; the **customer is part of the production process** in services (barber, hospital, doctor consultancy) but not in the production industry; service delivery is manufacturing at the same time consumption happens; **no physical storage** in services; after-sales services are required in products but not in services (record experiences/feedback/inputs).
- **Queuing theory** manages long queues/channels — open **temporary service channels**; allocate a channel elsewhere when the queue is short.

---

## Lecture 54 — Supply Chain Digitalization: 21st Century Supply Chain

### 54.1 Definition and Purpose
- **Supply chain digitalization** = implementing advanced digital products and services into different aspects of the supply chain to **streamline operations, improve management and increase visibility** — so we can be more productive, efficient and **error free**.
- **Digitized data management** is the first important thing and a challenge — a **parallel digital world** representing all physical aspects; huge data is generated, must be processed timely, and decisions made from it.
- Example (inventory management software): surfing/shopping online — even a search, ad click and order is shared with the distribution channel, manufacturing unit, raw material suppliers, warehousing team and transportation team for **quick decisions on real-time information**. Tracking sales records/customer information helps **demand forecast** and plan the whole supply chain.

### 54.2 Evolution
- Earlier heavily **manual/documentation-based**: demand at country level collected area-wise by sales managers → district → state → country; **information gets amplified** (recorded **10**, placed **12** with distributor, distributor **15**) — the **bullwhip effect** — due to **limited visibility**.
- **Advent of computerization in the late 20th century**; first software; matured **ERP/SAP solutions** keep all data records.
- ERP lets you view **10 different plants/supply chains from one place**: lots received, items in a lot, rejected items sent back, vendors paid, purchase orders placed, manpower — all digital and real-time; find bottlenecks, low performance, breakdowns.
- But ERP **lacked real-time visibility and agility** (plan for tomorrow made this evening; a night disruption/market shift is not captured).
- **E-commerce market:** an ad click on social media is recorded by stakeholders; if a customer does not purchase, that is recorded too (e.g., wants delivery in **2 hours** but policy is tomorrow → top management informed to change policy).
- **Warehouse:** one interactive screen locates an item among **10,000 items** → minimize manpower.
- **Hospital:** the doctor enters a prescription on one system; the back-end warehouse packs and delivers the packet to the doctor's table within seconds (vs a pharmacy with a long queue and **10 people**).

### 54.3 Key Components
- **Data analytics and big data** — touch points (store, billing counter, distribution network, manufacturing, raw material suppliers, competitors); why customers shift brands.
- **Internet of Things (IoT)** — sensors, RFID tags, smart devices for real-time information. **Smart kitchen example:** the refrigerator automatically orders butter/juice when stock falls below the safety level (brand and quantity fixed).
- **Cloud computing** — scalability, flexibility, accessibility; real-time collaboration/information sharing (transportation capacity, warehousing capacity, raw material shipping).
- **Blockchain technology** — secure, transparent, decentralized data storage, immutable records, trust.
- **Digital twins** — digital representation of physical assets, processes or systems.
- **Robotic process automation** — repetitive routine activities done by robots, error-free; in R&D human intervention is needed. If a machine produces errors it keeps producing errors (stop production), while humans may produce a reject then OK material.
- **Supply chain visibility platform** — real-time data insights (where the raw material lot is, production status, dispatch, customer receipt); a collaborative platform.
- **Cyber security** — encryption, authentication, access control, continuous monitoring; quick backup if something goes wrong.
- **Supply chain network optimization** — design/configuration (warehouse location considering demand, supply, local conditions, space, economic, social, sustainability); **GPS** for the best route.
- **Predictive maintenance** — IoT in a **smart factory**; observe machine behavior to predict when it goes out of parameters (wear and tear) and plan maintenance; track equipment functionality.
- **Supplier collaboration platform** — communication/collaboration/information sharing; customer engagement (**Zomato** — restaurant approval, preparing, courier picked, rain-delay intimation).
- **Sustainability and environmental management** — fewer resources, less degradation, lower per-unit cost; share carbon footprint information with customers; recyclable packaging.
- **Supply chain resilience and risk management** — predict a disaster/political scenario; diversify material flow through another channel if one vendor strikes.
- **Regulatory compliance and governance** — digital records ready; no separate team needed to prepare documents.
- **Continuous improvement and innovation** — AI, ML, IoT, big data, predictive analytics used daily to innovate/renovate.

### 54.4 Implementation (Five Steps)
1. **Define the vision** — aligned with the organization's overall objectives.
2. **Assess the resources/existing legacy system** — manage the workforce (convince, educate and train them for new technical skills).
3. **Collect data and analysis** — define performance parameters after implementation.
4. **Unified data and processes** — complete end-to-end visibility; a unified platform (transportation, warehouse, assignment, what/where/how to manufacture, outsourcing, sequencing, scheduling); **automated planning**; quickly share demand decline with vendors.
5. **Align people with the process** — train them for new technology; use data/analytics for informed decisions.

### 54.5 Benefits
- **Better financial management** — inventory example: earlier **₹10 crore** inventory, now **₹5 crore**; keep inventory for **6–7 days** if it can be replenished within **5 days**.
- **Minimized lead time** — information shared as the customer places the order; no physical document handover.
- Improved decision-making (real-time data), increased automation, organization flexibility, support specialization/minimize process cost, accelerate innovation, **end-to-end customer engagement**.

### 54.6 Factors Forcing Digitalization
- **Government policies** — funding/tax rebates/regulatory framework to push technology so more industrial hubs, productivity, employment and GDP/national income.
- **Technological advancement**; **globalization and complexity**; **market demand and competition** (competitors provide digital records — e.g., **Flipkart/Amazon** keep bills digitally for a **5-year warranty** claim).
- IoT data model predicts predictive maintenance within **5 days**; productive global competitors have lower cost/price and higher margins.

### 54.7 Challenges
- **Information system and data** — some fake/random information; ensure meaningful conclusions.
- **Team training** — shortage of talent for warehouse management/transportation/distribution (not only in India but everywhere).
- **Change management** — human tendency to resist change.

### 54.8 Digitalization in Healthcare
- **47%** wish to know more about their doctor (the doctor knows the patient's history but patients never know the doctor's treated cases/results/side effects); **38%** would like to check a hospital and its medical facilities before going (blood group availability, equipment, labs, doctors); **77%** prefer online medical appointment.
- **COVID-19 → telemedicine** (for communicable diseases), with online medicine delivery to the doorstep.
- Data records/private documents must not be shared; **big data analytics** from medical devices, smart watches, wrist bands, oximeters (blood pressure, oxygen, temperature, sweating, steps).

### 54.9 Dell Case
- Earlier a **direct-to-customer** model for PC sales (requirements/config delivered in **1–2 days**); realized it wanted **build-to-order + build-to-stock** (keep some products ready for urgency).
- **Transformed in 2017** — digital supply chain to enhance **transparency, predictive analytics and automation**; interconnected digital business ecosystem; three transformational levels: **actors, processes and technology**.
- Motto: make the right commitment, ensure parts supply, keep the customer informed, manage the supplier ecosystem, drive operational efficiency.
- **Size and scale:** **25+ manufacturing locations, 2000 service centres, 50 distribution centres, 3 units shipped per second, 770 power distribution centres, 392,000 Dell and EMC SKUs, 34,000 ocean containers, 220,000 orders per day**.
- Conclusion: greater visibility, better decision-making, less inventory, greater flexibility and risk preparedness; invest in integrated IT systems that analyze big data and system-based algorithms.

---

## Lecture 55 — Smart Supply Chains

### 55.1 Evolution
- Smart supply chains evolved due to the **increasing complexity and interconnectedness** of the global supply network; after globalization there are no boundaries — **n stakeholders** from anywhere in the world must be connected on a **common platform**.
- History: scientific management and assembly line by **Frederick Taylor** and **Henry Ford** — optimizing production processes and improving inventory → **zero inventory / just-in-time**; many organizations still struggle to maintain JIT/zero inventory because the future is uncertain (safety stock).
- Globalization expanded supply chains — outsource/buy/sell anywhere; access to bigger/new markets but **huge setup cost**; huge big data; integrate with the factory (**smart industry**); a user interface for customers to order from anywhere; the desired level of automation.
- Challenges: **coordination, visibility, risk management** (overseas vendors, shutdown, **Russia-Ukraine war**, geopolitical scenario, disaster).
- **ERP** integrates inventory management, procurement, production planning and employee records. Smart technology → **real-time visibility, predictive analytics for demand forecasting**, optimize inventory, enhance collaboration.
- Smart supply chains are characterized by their ability to **leverage data-driven insights, automation and connectivity** to improve **agility, efficiency and resilience**.
- Sustainability integration — track carbon footprint, **green sourcing**, green packaging, green manufacturing; **Industry 4.0** (cyber-physical systems, cloud computing, AI).
- **Restaurant example:** online ordering is cheaper for the restaurant (no one-hour sitting, no AC/staff/space; 24-hour shifts; more customers within the same capacity) → margin/efficiency shared among customer, delivery partner and restaurant.

### 55.2 Smart Drivers
- Six drivers — **facilities, information, transportation, sourcing, pricing, inventory** — all become smart:
  - **Smart facilities** — automated warehouses, automated records shared with manufacturing immediately; **smart factories** (real-time information, automated production lines, robots, predictive maintenance).
  - **Smart information** — real-time.
  - **Smart transportation** — GPS, routes with minimum fuel/time considering weather and traffic.
  - **Smart sourcing** — smart contracts with vendors.
  - **Smart pricing** — benefiting the manufacturer, customer and stakeholders.
  - **Smart inventory** — real-time info minimizes inventory cost; a central location/hub to channelize inventory.
- These drivers generate **big data** (data streams/digital aspect); IoT + big data → smart supply chain, with decisions based on data from all six drivers.

### 55.3 Hierarchical Model (Zhang, 2023)
- **Level 3:** smart supply chain management; the **base (level 0)** is all the technologies discussed.
- **Smart unit flow** — material, information and finance flow smartly (a smart contract executes payment on lot acceptance).
- **Smart drivers, smart decisions** (real-time data from touch points), **smart function** (visibility, real-time optimization).
- **Level 2:** smart supply chain network — **interconnected, intelligent, innovative, self-organizing and self-optimizing** (the system takes decisions, e.g., predicts a **95% chance of rain, 50 mm**, and automatically re-routes so supply is not interrupted).
- Leads to a **responsive, efficient, resilient, agile, flexible and sustainable** supply chain: economy (efficient/less cost), environment (less resources depleted), society (value delivered to customers).

### 55.4 Traditional vs Smart Supply Chain
- **Transparency:** traditional — physical documents; even a service feedback form may not reach Maruti Suzuki's decision-makers; smart — information shared through all stakeholders.
- **Data collection:** traditional — bullwhip effect (region → district → state → country → world); smart — quick data sharing the moment a touch point generates data.
- **Responsiveness:** traditional — low (react after six months); smart — high.
- **Traceability:** traditional — low (e.g., **6–8 months** waiting for a model, unknown status); smart — highest level.
- **Adaptability:** traditional — reactive; smart — predictive/planned in advance.
- **Feedback:** traditional — may be stuck where the form is filled; smart — reaches the concerned person.

### 55.5 Key Components
- **Sustainable practices** — optimize energy, reduce waste, minimize environmental impact; greener raw material; information on packaging.
- **Agile and resilient supply chain** — predict in advance; ensure smooth supply even if a disruption occurs.
- **Responsiveness** — respond to customer requirements, changing market conditions and disruptions.
- **Efficiency** — same output with reduced input, or more output at the same input; target ~**95%** efficiency.
- **Flexibility** — anticipate and respond to changes in demand, market dynamics and operating conditions.
- **Real-time visibility** — IoT sensors/devices track the movement of goods and find bottlenecks in the factory.
- **Predictive analytics** — big data analytics and AI algorithms on IoT devices, production systems and external factors (weather, market trends).
- **Automated processes** — routine repetitive processes handled by robots.
- **Dynamic optimization** — reconfigure functions as forecasting/demand changes; machines decide based on market conditions; a collaborative ecosystem platform.

### 55.6 Resilience, Efficiency and Sustainability
- **Resilience** — supply chains vulnerable to disruptions; **panic buying** during shutdown (demand not actually higher, but people unsure of future supply); how far the supply chain is OK and how quickly it bounces back; embrace **IoT, AI, blockchain** for real-time tracking, proactive risk management, seamless coordination; cyber attacks; speed, reliability and agility.
- **Efficiency** — with the same/lesser input produce more; minimize expenses, waste, effort, raw material and rejection; efficiency = actual output / expected output (~**95%**).
- Cost reduction (less resources, no wastage), resource optimization, faster response time, improved customer service, risk mitigation, environmental sustainability.
- **Sustainability** — **closed-loop supply chain** (upstream/downstream); **economic, environmental and social** dimensions; economic value creation, minimize resource consumption, collection/sorting/recycling of waste; addressing **profit, people and planet**.

### 55.7 Implementation Examples
- **IoT-based sustainable smart supply chain** — customer approaches a touch point; sensor nodes generate data shared with manufacturer, transportation, packaging, supplier, warehouse; cloud computing; information-based decisions.
- **Blockchain-based sustainable supply chain** — smart contract executes on material receipt; a purchase order is raised when inventory falls below safety stock; consensus, cyber security, immutable, decentralization; ensures **transparency, traceability, trust, responsiveness and accountability**; closed-loop reuse of raw material.
- **Cloud and AI-based sustainable smart supply chain** — data from every stage goes to the cloud; **descriptive, predictive and prescriptive** analytics (what happened, why, what can happen in the future, how to control); decisions for raw material suppliers, manufacturer, customers, closed loop and disposal/recycling.
- **Smart grid power distribution** — sources like thermal (~20%), wind (~35%), and a small share (2–3%) from others; see utilization from each source and design strategies to get more energy from the wind generator.

---

## Lecture 56 — Robust and Resilient Supply Chain Design

### 56.1 Supply Chain Challenges
- The whole world is **one market and interconnected** — anything happening anywhere impacts the rest.
- Examples: **2008 recession** (started from the bankruptcy of **Lehman Brothers**), **COVID-19** (started in China), **Russia-Ukraine war**, recent political scenario in **Bangladesh** (clothing industries get maximum inputs from Bangladesh), **Sri Lanka** — strategic cheaper locations.
- Challenges are **cyclic in nature and forever**; supply chains are vulnerable → design a **robust and resilient** supply chain to minimize impact.

### 56.2 Risk — Mitigation vs Management
- **Risk mitigation** = reactive (something is happening and you respond); **risk management** = better prediction/anticipation (predictive analytics → manage in advance). Move from mitigation to management.
- Supply chain risk: **operational risk** (production/suppliers/vendors/manufacturing down → interrupted supply) and **financial risk** (bad debts, extra charges, inventory tied up, not enough capital to survive).
- Steps: **identify** how things happen and how they can impact → **assess the amount of impact** → come up with **mitigating strategies**.

### 56.3 Effective Risk Management Strategies
- **Build redundancy** — enough alternatives. Molding machine breakdown → alternative/spare parts/extra capacity machine. Transportation network: if road is obstructed by a natural disaster → **air/train** connectivity.
- **Diversify suppliers** (nearby/overseas); if something goes wrong in the northern region, the **southern supply chain** can supply raw material.
- **Contingent plans** (situational planning) for anything that goes wrong.

### 56.4 Supply Chain Vulnerability
- How **susceptible** the supply chain is to internal/external disruptions; impacts the three flows (**material, information, money**).
- Sources: **natural disaster** (cloud bursting, flood, earthquake), **political** (Bangladesh, Sri Lanka, Pakistan), **economic downturns** (COVID-19 — automobile sales went down, income stopped), **unexpected demand shift** (customers shift to a brand with a better strategy).

### 56.5 Robustness
- How long the supply chain can **withstand** disruptions (internal/external) while still providing raw material/finished product.
- Characteristics: **flexibility** (managing capacities for extra demand or a downturn), **adaptability** (how quickly you adapt to disruptions), **agility** (how quickly the supply chain responds).

### 56.6 Resilience
- How you **manage during** a disruption and how quickly you **bounce back**.
- A disaster (earthquake/flood) disconnects the main supply chain (roads, train, air), with no IT infrastructure/electricity — these concepts are most relevant for **disaster management/disaster relief operations** (medical supply first, then food packets, then clothing, then rescue).
- Build **adaptive capacity** (produce more/less/something else) and **foster collaboration and transparency** throughout the network.
- **Avoid the bullwhip effect:** today fluctuations are observed at regional level then consolidated district → state → regional → country → world; instead use a **one-stop solution** — anything at any point shared transparently and quickly.
- Sharing example: vendor A's machine failure → all stakeholders know the implication (interrupted supply of that component) → go for an alternative vendor/material.
- **Dell example:** customized products plus **make-to-stock** for standardized items; design, price and procure when the customer places the order; raw materials fly from **Asian countries**; record customer information; external threats/legislative and customer changes. Risk management process: define the disruption level → assess impact → mitigating strategies (not one-day/one-stop).

### 56.7 Risk Types
- **External supply chain risk** — social, political, technical, ethical, legal environment; cultural shift, technological breakthrough, political instability.
- **Demand risk** — forecast error, COVID-19 shutdown (sudden drop), **panic buying** (spike though actual demand is not increasing).
- **Supply risk** — posed by forward/backward supply chain (overseas/China/Bangladesh suppliers).
- **Environmental risks** — social/economic/political/governmental/environmental/sustainability.
- **Business risk** — business acquired (cultural shift), business failure, joint ventures.
- **Internal supply chain risk** — absenteeism (outsource manpower), disaster/fire outbreak; **manufacturing risk** (production down — machine breakdown, high absenteeism, interrupted raw material); **business risk** (disruption to standard personnel management reporting, joint venture, selling shares); **planning and control risk** (based on forecasting).
- **Mitigation and contingency risk** — plans not going as per the disaster.
- **Vulnerability = risk + exposure.** External risk: demand from the outside environment; uncertainty (customer ready/not ready to wait → short lead time); margins, markdowns, environmental challenges, security (cyber attack, **IPR leakage**). Internal: production process, purchasing, accounting (bad debts → liquidity ratio, cash for day-to-day obligations).

### 56.8 Risk Management Strategies
- **PPRR risk management model** — **Prevention, Preparedness, Response, Recovery**: prevent the disruption → if not, prepare contingent plans → respond quickly to the abnormal situation → recover to normal.
- **Manage environmental risk:** during COVID-19, suppliers in China; workforce shortage in warehousing/transportation/logistics; **multi-sourcing model**. **Breweries started producing sanitiser**; **Ford started manufacturing ventilators** (utilize existing capacity/manpower, contribute to society). **Risk assessment software** (predictive maintenance, predict future risk/disaster).
- Key strategies: **diversify suppliers**, source closer (**nearshoring vs earlier offshoring** — set up vendors nearby for JIT/zero or near-zero inventory), **regular stress tests**, **build inventory buffers**, use technology.
- **Carrier partner selection:** ~**60% road**, ~**1% air**, **5–6% train**, rest waterways. Air is most efficient for delivery/lead time; ship for cost/sustainability. Evaluate the carrier: transit time per mile, number of stops and average stop time, average loading time, route optimization, maintenance schedule (planned → alternatives).
- **Logistics contingency plan** (plan A fails → plan B), **internal risk awareness training** (mock drills), common supply chain risk, **continuous monitoring** of risk (scale operations accordingly), use data to **model key risk event scenarios** (predictive analytics — molding machine maintenance planning), **consolidate data for easy access** (customer buying patterns from organized/unorganized retail and online apps).

### 56.9 Temple of Supply Chain Resilience
- **Foundation:** supply chain strategy aligned with competitive strategy (if responsive, delivery speed is the priority, not cost).
- **Floor:** product design (if the raw material/component shape is difficult, quality/delivery/raw material issues arise).
- **Four pillars:** **agility, collaboration with partners, supply chain risk management** (predict in advance), **supply chain design** (multi-modal structure, warehouse, internal supply chain).
- **Roof:** the resilient supply chain structure.
- Steps: find multiple suppliers; build resilient inventory management (minimum inventory may go obsolete/be destroyed; JIT/nearshoring); harness advanced technology; strong relationships with stakeholders; map risk in advance (predictive analytics); strengthen the transportation/logistics network (route optimization for all modes); sustainability measures.
- **Drivers of potential vulnerability:** planning and supplier network (forecasting error disturbs vendor/storage/manufacturing/distribution), transportation and logistics (road obstructed → **drone** for emergency/medical supplies), financial resiliency (flexibility to invest extra), product complexity (simple product design and manufacturing line, minimum error-prone), organizational maturity.
- **Supply chain vulnerability drivers (supply side):** quality interrupted, diverse delivery risk (delay), supplier dependency, operational risk (machine failure/strike/disaster), demand side risk (fluctuation/spike/surge), environmental risk.

### 56.10 Robust Supply Chain — Key Aspects
- **Redundancy** (alternatives — supplies, production, warehouse, transportation), **flexibility**, **resilience**, **visibility** (visible to all stakeholders), **collaboration** (a game of collaboration — first supplier to end customer), **risk management**, **technology** (data analytics, predictive maintenance, predict weather/traffic/accident → alternate route; real-time informed decisions).
- Sequence: plan demand → plan with suppliers → maintain inventory → logistics/transportation → information system integrates all stakeholders.

### 56.11 JD.com Case
- Initially a **self-operated mode** — purchased all products and sold online, directly connecting; responsible for inventory management, distribution, delivery and after-sales; any delay/customer issue was their responsibility.
- Now changed — some affiliated JD stores are handled by independent merchants; still **60% share** is JD.com directly interacting with the customer.
- Traditional supply chain: brand manufacturer → general agents → distributors → retailers → carry-forward agent → wholesaler → distributors (a huge chain). **JD.com simplified** — only JD.com between customer and manufacturer; sourcing directly from manufacturer/factories/vendors/sub-assemblies; maintains inventory and channels it.
- Plus points: minimum disruption impact, high collaboration, effective information sharing (no delayed/manipulated/amplified multi-stage information), high agility, intelligent platform to predict disasters, minimum human intervention (automated planning; demand function configured/shared with vendors → JD plans inventories).
- **Nissan case:** after an earthquake in Japan, returned to normal production lines within **18–20 days** — a huge success in supply chain resilience/robustness.

---

## Lecture 57 — 21st Century Supply Chain

### 57.1 Characteristics and Driving Forces
- The 21st-century supply chain is characterized by **continuous transformation**; driving forces: **technological advancement, globalization and evolving customer preferences**.
- **Technological advancement** — software to predict disasters (heavy rain/flood/earthquake), market fluctuations, downturns/recessions, political instability, social/cultural change (using past records).
- **Globalization** — cannot operate in isolation; crude oil/petrol/diesel price inflation affects every industry.
- **Evolving customer preferences** — today **2% extra** delights, tomorrow 2% merely satisfies, then they want 3%, 5%, 7%; a competitive environment demands a supply chain based on **real-time data and analytics**.
- **Interconnectedness** is positive (share information, align decision-making — cost efficiency shared with raw material suppliers/distribution) and negative (anything wrong at one point disrupts the whole chain; increasingly complex supply chains; **automated decision-making** needed).

### 57.2 Key Aspects
- **Digitalization and automation** — a digital twin/replicating the physical in a digital platform; records must be shared at the same time they are recorded (automated); AI, ML, big data analytics, IoT; a virtual world of physical equipment/resources/markets.
- **Supply chain visibility and transparency** — explore alternatives when a route is interrupted (know how many hours it will take); share where the threat/cyber attack happened; **blockchain-embedded supply chain** (records immutable, cannot be destroyed).
- **Globalization and outsourcing** — offshoring reasons (cheaper product/labour, raw material availability, latest technology); now **nearshoring** (vendors near the manufacturing unit for JIT, zero inventory and customization).
- **Supply chain resiliency** — earlier recession cycles were **8–10 years**, now frequent (**2008 recession, 2018/COVID-19, Russia-Ukraine war, Sri Lanka, Bangladesh, Iran war**); fuel import interruptions/increasing prices; **redundancy/alternatives** (cyber attack → keep records somewhere else).

### 57.3 Sustainability and CSR
- Earlier a **climate-change debate**; government regulations (banning **BS4 engines**, updated versions; in polluted cities like **Delhi/Calcutta**, heavy vehicles older than **15 years** are not allowed).
- **Customer awareness** is forcing major brands — **Myntra** moved from poly bag/plastic packaging to paper packaging; European example: end-mile delivery by bicycle/electric vehicle → customers more delighted, placing more orders.
- Customers demand complete information about **carbon footprint** (at packaging, manufacturing, transportation — every stage).
- **Customer centricity and omni-channel logistics** — customers want speed, convenience and personalization; quick delivery despite extra fuel/energy/resources; repeated delivery attempts consume resources.
- **Omni-channel** — traditional brick-and-mortar, e-commerce, air tickets (Indigo/Air India website, **MakeMyTrip, Goibibo, IRCTC, ixigo**); limited capacity; a strong information system to configure.

### 57.4 Supply Chain Trends in 2024
- **Integral visibility, sustainable brands, regionalized/near-shoring supply chains, RPA adoption (robotic process automation), AI-driven decision-making**.
- Visibility is a **must have**, not nice to have; a **unified data platform**; data analytics; IoT network shared with stakeholders; the **entire supply chain responds** (not just the manufacturer/transporter/warehouse/vendor).
- **Competitiveness** — this era's game is based on information; "it is better to be **first** than to be **better**."
- **Sustainability as a key brand differentiator** (Myntra paper packaging; European bicycle delivery as a USP).
- **Circular economy models** — **Life Cycle Assessment (LCA)** software; information on packaging about environment depleted at each stage; per unit of electricity → environment depleted; rating agencies/consumer requests — **environmental, social and governance (ESG)**; electric cars, green business, green packaging; electric bikes selling in huge numbers.

### 57.5 Circular vs Linear Economy
- **Linear economy:** raw material enters → manufacturing → distribution → consumption → byproduct (waste); not a long-term solution.
- **Circular economy:** byproducts are reused/reutilized/remanufactured in the same industry or in other industries (industry 1, 2, 3, 4) after end use.

### 57.6 Regional Supply Chains
- Regional supply chains meet disasters better; **nearshoring**, **multi-node networks**, **localized production**, **multi-sourcing** (many suppliers, not just 1–2) for smooth supply.
- Coming back to regional models — earlier the **barter** system (produce in Kharagpur/West Bengal and consume there only); implement zero inventory/JIT models.
- Cannot deny global supply chain benefits (quality, technology, raw material supply, price) → make the **trade-off**.

### 57.7 Supply Chain Risk Management Steps (Overview)
- Establish proper **governance**; identify **critical suppliers** — **A/B/C model**: **C-type ~70–80%** of components contributing only **5–10%** value → can maintain long-term inventory (outsource offshore for location/technology/price/quality advantage); **20–25%** small number of items contributing huge value (~**80%** of cost) → keep very near (hard to hold inventory).
- Adopt **robotic and autonomous systems**; warehouse management software, warehouse robots (place on shelves, identify/retrieve, pick/pack/ship).
- **Next-generation AI (2024)** — **generative AI** generates/replicates data for the future and predicts future maintenance, absenteeism, raw material supply disruption and external environmental forces; **route optimization** (based on the last 10 routes, disruptions/traffic jams → best route or mode for economic/environmental/sustainability benefit).
- **Significant benefits of AI:** predictive maintenance → no breakdown, cut machine **downtime by 35–45%**, fewer rejections, improved production quality/quantity, increased productivity.
- **McKinsey report:** digital AI-driven forecasting **reduces error by 50%**.

### 57.8 Logistics and E-commerce
- Logistics is the **backbone of any trade/product manufacturing**; implement technologies in the logistics framework — technological integration, **automated route planning**, AI, data analytics to streamline operations, reduce errors and increase efficiency.
- **E-commerce boom** — half-hour/one-day/two-day delivery; end-mile delivery by **drones and autonomous vehicles**.

### 57.9 Challenges and Solutions
- **Challenges:** disruptions (internal/external environment), sustainability (measures changing frequently), labour-intensive jobs replaced by robots but **qualified professionals** needed to run robots/technology/software.
- **Solution** to major problems: data sharing/transparency/visibility, demand fluctuation/predictive analytics → **blockchain technology**; a **collaborative platform/unified data** for one planning; **ESG supply chain dynamics**.
- **ESG** — environmental (energy efficiency, greenhouse gas emission, deforestation — Myntra paper packaging but collaborated with an **NGO** for more plantation), social (quality of life, opportunities), governance (cyber security, government reports/disclosure).
- **Web-based supply chain management** — an internet-based platform (order, distribute, track; **Amazon, Flipkart, eBay, Myntra**).
- Benefits: enhanced collaboration (JD.com manufacturer-to-customer), improved visibility (track order anytime), cost saving (intermediaries removed), scale up/down, enhanced customer services (customized product), data-driven insights (AI/generative AI).

### 57.10 Indian Supply Chain
- One of the **largest globally** (population-wise); huge market potential; but struggling — **competitiveness gap ~180 billion US dollars**; India spends ~**12–13% (14%)** of GDP vs **8%** in developed nations.
- **CII supply chain leadership conclave, September 2020** set the agenda for **Vision 2030**; also a conclave on supply chain transformation for efficiency and capability.
- Indian supply chain focus (Vision 2030): logistics-cost optimization, mix-model (60% road), digitalizing records, omni-channel approach, green supply chains.
- Industry growing at **10.5% annual CAGR**; but unbalanced logistics model mix, high indirect cost, poor infrastructure (road; train only **15–20 km/h** vs possible **60–70 km/h** due to traffic). COVID-19 exposed the supply chain; huge demand for online grocery.
- **Barriers:** unbalanced modal mix (**64% by road**; rail/water/air underutilized — air ~**1%**, water ~**5%**; transportation ~**40%** share), high indirect cost, poor infrastructure, limited technology adoption (high initial investment; MSMEs cannot afford), **fragmented/not-regulated trucking network** (container capacity underutilized on return trips, e.g., Kharagpur → Calcutta).
- Work on intermodal transportation or improve connectivity infrastructure. 21st-century supply chains must emphasize **innovation, collaboration and sustainability**.
- **Five major digital components:** insight-driven enterprise, digital customer engagement, digital-enabled workforce, digital service optimization, digital ecosystem.
- Holistic supply chain perspective; the **margin/profit is for all players/stakeholders** and is shared among them.

---

## Lecture 58 — Sustainable Supply Chain

### 58.1 Introduction
- Increasing **customer awareness** plus pressure from **regulatory authorities/environmental agencies** are forcing sustainable supply chains.
- Focus: the **environmental and human aspect**; minimize environmental/social impact across extracting raw material, transporting it, manufacturing, warehousing, distribution and reaching the end customer; plus the **economic parameter** (the third pillar).
- Goal: minimize environmental harm; **energy usage, water consumption**, and minimize byproducts.
- **Nike** — minimum footprint: **100% recyclable energy**, solar lights, turbine lights, **100% recyclable packaging**, and recycling after the product's end life.

### 58.2 Role of Sustainability
- In the 21st century we are more concerned because we have degraded/depleted the environment; resources are falling short and must be available for the next generation.
- The health and survival of every supply chain and individual depends on the health of the surrounding world.
- **United Nations (Led commission):** "development that meets the need of the present **without compromising the ability of the future generation** to meet their own needs."
- **UN framework:** **economic, environmental and social** sustainability. Economic sustainability is equally (maybe more) important — only if surviving economically can we think of the others.
- Large countries (**Brazil, China, India**) are growing → faster resource extraction; the environment/natural resources cannot sustain this for long.
- Under economic consideration: reduce risk and improve financial performance; a **continuous cycle of finance** (backward → forward supply chain; pay vendor/supplier/manufacturer/distribution/warehouse/transport) and a reverse flow ensures **ROI**.
- **Attracting customers who value sustainability** — studies show customers are ready to pay **2–10% more** if brands promise sustainability/minimum carbon footprint; a marketing strategy — record the carbon footprint on packaging (production and doorstep delivery); customers ready to wait if it is not an emergency (delivery by cycle).

### 58.3 Examples
- **Unilever** — helping emerging economies (**Brazil, India**) fight poverty, water scarcity and climate change; Brazil tomato growers converted to **drip irrigation** to save water; almost **half of its sales and majority of growth** came from emerging economies.
- **Walmart** — many initiatives to be sustainable; **100% recyclable energy** for facilities/warehouses; efficient light bulbs; **skylights** for natural light; reducing packaging (with over-packaging only **80 instead of 100 products** fit in a container → cut transportation cost).

### 58.4 Triple Bottom Line
- Coined by **Johan (Elkington)**; aims to instill transparency in supply chain performance — throughout the complete supply chain (storing/cooling, transporting, disposing of packaging, converting raw material) how much energy/environment is used.
- **Life Cycle Assessment (LCA) software** records energy use and environment depletion at different stages; e.g., energy from **hydro vs thermal** power station (thermal burns coal); hydro also depletes soil fertility; the software calculates the impact on the environment, society and economic cost.
- Strengthening local activities and competitive advantage (nearshoring saves energy/resources).
- Mitigate environmental degradation — e.g., **SAIL (Steel Authority of India Limited)** continuously degrades the environment (high temperature to melt steel, coal as primary fuel, 24×7); it compensates through **CSR** (health care/hospitals, education, employment, infrastructure, electricity, roads, water supply).
- **Social measures:** health/well-being/quality of life, supportive work environment, **gender equality**, ethical business practices, **human and labour rights**.
- **Environmental measures:** identify/prioritize green practices within manufacturing **and at the supplier end** (e.g., EV end-mile delivery, but electricity from a thermal power station equally affects the environment).
- **Economic measures:** financial flow through the supply chain (circulate ₹10 again and again for more returns); expenditure on the environment; the upfront cost is high → single-use plastic is still cheap; returns via brand awareness (**Myntra** paper packaging "100% recyclable").
- Nurturing business integrity across **people, profit and planet**.

### 58.5 Key Advantages
- Reducing **carbon footprint and energy expenses** (minimize resource use).
- Enhancing **brand image and productivity**; initial investment high but many have implemented — **Starbucks** dedicated customer cup (bring your own cup) eliminates use-and-throw culture, saving up to **50%**.
- Paving the path for future growth and financial security; a green brand image attracts **investors** (green shares in the Indian stock market).
- Five frequently cited business activities that benefit: **supply chain operation** (emission targets with suppliers), **branding** (customers pay 2–10% more), **compliance** (sustainability metrics meet regulations), **investor relations** (positive impact on stock price), **corporate culture** (theme into HR practices, mission/vision statement).

### 58.6 Key Metrics for Sustainability
- **Carbon footprint** — total greenhouse gas emission at different stages; identify high-footprint stages.
- **Energy consumption** — track energy at each stage; if transportation consumes the maximum, find an alternative fuel.
- **Water use** — reduce water consumption.
- **Waste generation** — minimize; if not possible, use the byproduct as raw material/input to another organization. **Sugar industry example:** sugarcane husk thrown/burned openly creates pollution; instead burn it in a furnace → energy/electricity; pass the black smoke through **water** to retain harmful elements; the water can be used as fertilizer or given deep burial.
- **Supplier diversity** — based on location, size, quality and ownership.
- **Ethical sourcing** — vendors that ensure good labour practices and sustainability.
- **Supplier compliance** — ask for a sustainability report with every lot (carbon footprint of the raw material) and add it to your metric.
- **Product life cycle analysis** — introduction, growth, maturity, decline; record environment depletion.
- **Transportation efficiency** — intermodal transportation; **ship** has the minimum environmental impact (if infrastructure is available).
- **Social impact** — protect workers' interests; no **forceful labour, no child labour**.

### 58.7 Six Drivers for Sustainability
- **Facilities** — Walmart efficient light bulbs, skylights; manufacturing/warehousing cooling and lighting systems → minimum consumption, recyclable energy.
- **Inventory** — inventory is kept because demand is uncertain; latest software/predictive analytics to predict demand 100% → minimize inventory.
- **Transportation** — the mode carrying maximum weight with minimum time and minimum carbon footprint.
- **Sourcing** — **Starbucks** collaborates with socially/environmentally responsible suppliers.
- **Information** — if you do not measure carbon footprint throughout all stages you cannot control it; **reporting and measurement are the two basic steps**.
- **Pricing** — customers are ready to pay extra if initiatives are positive.

### 58.8 Seven Ways to Improve Sustainability
1. **Find the current pain points** — calculate the **product carbon footprint (PCF)** at each stage; identify the stages contributing the maximum.
2. **Optimize transportation** — nearshoring, maximum capacity utilization, electrical vehicles; a US study shows **29%** — only the transportation part — contributes to pollution/carbon footprint.
3. **Collaborate with sustainable partners** — socially/environmentally/ethically strong; **GRI 408/409** norms (child labour practices); **ISO 14001** certified; request vendors to submit **ESG reports, carbon footprint, PCF verified**.
4. **Minimum inventory** — heating/cooling/lighting facilities are not required (except milk products, where the refrigerator runs morning to evening).
5. **Reuse waste or byproduct as raw material** — in your company or another.
6. **Use environmentally friendly packaging material** — only **1% of plastics are biodegradable**; shift to another material.
7. **Nudge regulators and consumers** — green/hybrid/electric car companies; tax difference (petrol version ~**27%**, electrical ~**10%**); a car is used for a minimum of **15 years**. Starbucks reduced plastic consumption by **50%**.

### 58.9 Challenges
- **Cost** — the initial investment is big; smaller companies cannot afford it; government agencies should support them.
- **Investment in sustainable practices for the long term** — not quick ROI.
- **Impossible/hard for a few companies** (steel industry burning coal, extracting ore).
- **Complexity in transitioning** — no clear norms; regulations keep changing.
- **Resistance to change** (human tendency).
- **Lack of customer interest** — if you replace packaging and ask the customer to pay extra, the initial phase is a struggle.

### 58.10 Trends and Survey
- **Circular economy** — anything entering the circle should not leave as waste; after end of use, divert it to another industry as raw material or recycle it in the same industry.
- **Data-driven supply chain** — cloud-based systems, IoT devices; how much waste, where, and how to channelize it; municipal waste quantity is uncertain.
- **Survey (case study):** many executives have long-term vision but face **upfront cost and lack of a clear business case** to support sustainability expenditure; **8 of 10** executives are increasing effort but struggle with ROI.
- Five suggested actions: organizational commitment, improve visibility/traceability, expand ROI measurement (market share, brand awareness, sales growth), leverage tax incentives and grants, public-facing sustainability goals.
- **55%** of supply chain executives expect better management of operational risk within the next **1–3 years**; more than **20%** have already seen reductions.
- Why companies go for sustainability: **61%** to save cost/reduce resource consumption; **51%** compliance with the regulatory authority; **40%** pressure from partners/suppliers to highlight the product as sustainable.

---

## Lecture 59 — Emergency Supply Chain

### 59.1 Definition and Context
- A **complex emergency** (as defined by the **Joint Logistics Enterprise**) is a wide array of international conflict (cross-border), humanitarian and domestic disaster relief scenarios — combinations of warfare, food insecurity, pandemics or social conflict.
- Scenarios are characterized by: **displaced people** (COVID-19 — people moved from big cities back to villages, carrying the virus to rural areas), **large-scale damage**, **hindrance of intervention/prevention due to political scenario** (e.g., Bangladesh), security/infrastructure constraints, and threat of loss of life.
- Assistance is required at a very large scale; here the recipient is not a "customer" but the **affected people**.

### 59.2 Emergency Supply Chain
- A **specialized logistics framework** established to address **urgent and unforeseen situations**.
- Difference from a normal supply chain: normal disruptions can be analyzed up to some extent with predictive analytics/preparedness; in an emergency we **cannot predict the scale**, the number of people affected, the area affected, or the after-demand (which is for **segregated products**).
- Requires **very rapid mobilization of resources**, **coordination of stakeholders** (military, government, NGOs, individuals) and **deployment of essential goods and services** to affected areas.
- **Primary objective:** reach the affected people in a timely and effective way to minimize the disruption impact and save lives.
- Includes huge inventory of necessary items, **alternative transportation routes**, alternative facilities, and temporary warehouses and distribution centers.
- Not a one-time event — sequence events (aftershocks); the distribution channel set up is disrupted again.
- Two basic domains: **military operations**, and **support to non-government and disaster relief organizations**.

### 59.3 The Disaster Response Cycle
- Disaster → respond quickly → **search and rescue** (find people still alive) → **need assessment** (may cover 10 km without finding anyone, then one group waiting; requirements uncertain) → **medical supply immediately** (medicines, life support systems) → **resource mobilization** → **relief operation**.
- **Recovery** (after 4–5 days) → rebuild and reconstruct → set up channels; the **communication channel is most important** (no electricity/internet/telecom; use bluetooth/wifi devices that need no connectivity, or wearable wristbands to track life).
- Communicate information to all stakeholders (government, NGOs, industries, individuals); identify the number of people, medical supplies required, serious cases needing **air ambulance**; set up **helipads** to shift people to safe locations.
- **Mitigation** — lessons learned; predict/prepare; set up temporary locations; monitor the event and forecast supplies; compute the **lead time** for each activity; if lead time is high, **stockpile inventory**; **contingency planning** (e.g., second floods); **logistics capacity assessment**.
- **Waste is very high** in emergency supply chains — unsure how much supply is needed; emotional decisions → some products over-supplied, some never reaching. **UNICEF** example (emergency/humanitarian supply chain operations) and **drone/AI-enabled** relief.

### 59.4 Prioritization
- Normal situation (Maslow): **food, water, warmth** first; then safety/security; then society/community well-being; then self-esteem/self-actualization.
- Emergency: first **air** (e.g., a child falling in a bore well — ensure air supply), then **heat**, then **water and food supply**, then **medical supply** (recover/maintain health).

### 59.5 Why a Separate Framework
- **Disruption vs emergency:** disruptions (labour strike, unavailability of raw material, an accident on the road, a shipment problem, quality issues) keep the **same supply chain identity and same stakeholders** — strengthen vendors, adopt new technology, strengthen packaging.
- The **emergency supply chain** is initiated once the emergency has happened — **responsive/reactive**; how quickly can emergency supplies be provided. There is **no time for planning/coordination/collaboration/transparency/forecasting/data analytics** (little information).
- Set up the supply chain along the way — realize how many people/area are affected, for how long, and how many facilities/warehouses/distribution centers are needed; military units and disaster relief organizations arrive quickly.
- The supply chain manager decides the **new location, distribution routes and alternative transportation modes** (drones, helicopters, helipads, air ambulance).

### 59.6 Objectives — Conventional vs Emergency
- **Conventional:** right product, right quantity, right price, right time, right location; cost efficient; top-level service and doorstep delivery; ship back if the customer says no; sustainable packaging.
- **Emergency:** no service level, cost efficiency or demand certainty; **at any cost** ready to ship material.
- **Success = achieving results quickly** — how many lives saved, not cost saved; even if one individual is left behind, rescue by helicopter regardless of cost; faster shipping methods; **no economies of scale** (less-than-truck-load shipments), and over-supply is waste.
- **Implied demand uncertainty** is most suitable to define this supply chain.

### 59.7 Uniqueness of Emergency Logistics (Four Aspects)
1. **Urgent relief situations** — diverse and immediate services essential (medical supply from the pharmaceutical industry, food supply, water, electricity, communication, medical equipment, doctors, air ambulance); timely availability defines the **survival rate**.
2. **Accurate real-time information** — many software/touch points exist, but infrastructure vanishes in a flood/earthquake; how to collect information quickly is a challenge.
3. **Prioritized service efficiency over profit**.
4. **Collaboration** among government, public organizations, firms and individuals. **Uttarakhand flood (2013/14)** — relief operation lasted more than a month; if every day only bread packets, people cannot survive 30 days on the same bread; similar medical supplies but situations differ. Need a **unified system** — one ensures the complete medical supply chain, one food, one water, one air-ambulance/transportation.

### 59.8 Solution
- **Early preparation and precautionary measures** (natural disasters predictable up to some extent; man-made/war e.g., **Ukraine-Russia, Israel-Iran** — stockpile inventory for **6 months/1 year** so the military can survive; not only ammunition but medical and food supplies).
- A well-established emergency supply chain system based on **transparent communication** reduces time, energy and financial investment; without collaboration/streamlined communication, resources are wasted.
- Software development; if the IT infrastructure is damaged, set up another support system; combine/channelize financial support from different organizations; strengthen communication among aid enterprises, NGOs, individuals, industries and governments (upstream/downstream) → smooth supply, **no panic buying/extra stockpiling**.
- **Collaborative mechanism** — a **message-based system or electronic procurement hubs**; quick **walkie-talkie/bluetooth** devices connecting nearby.

### 59.9 Humanitarian Supply Chain
- Defined as **buying and delivering requested supplies and services at the places and time they are needed**.
- Basic survival needs: food, water, shelter; the humanitarian supply chain targets **immediate needs** — medical assistance, transportation, evacuation and water/food/medicine supplies.
- Two angles: **technical perspective** (planning, information gathering, warehousing, **pre-positioning**, transportation, distribution — a temporary supply chain) and **strategic decisions** (from where to outsource/buy, inter-organization cooperation, **public-private partnership**).
- It is the **lifeline in any crisis**.

### 59.10 Crisis Examples
- **2015 Nepal earthquake** — air and unconventional methods; **air ambulance** as the main transportation to supply medical supplies and food packets; the same helicopter transported people to relief camps, and later transported construction material to rebuild communities.
- **2017 Hurricane Maria, Puerto Rico** — ensured the **power grid and communication first** (medical equipment works on electricity); then restoring infrastructure, then permanent healthcare facilities, schools and livelihood (5–10 years/one decade).
- **Ebola outbreak, West Africa** — sudden surge in demand for medical supplies; the medical supply chain was **overburdened**.
- **Rohingya refugee crisis, Bangladesh** — limited access to the affected population; used **mobile medical supplies/mobile healthcare facilities** instead of a big facility.
- **2010 Haiti earthquake** — coordinated supply chain, **pre-positioned supplies**, collaboration with local stakeholders.
- **Zaatari refugee camp, Jordan** — collaboration with local authorities and innovative solutions; **nearshoring** (buying overseas/long distance is slow); nearby vendors pack food; **foreign field hospitals**.
- **COVID-19** — testing centers overnight, foreign field hospitals, many vaccination centers; record who took the first dose and ensure the **second dose of the same vaccine**; yet there was wastage of critical life-saving drugs.

### 59.11 Challenges
- **Never sure about demand** (how much area affected, population, how many survived) — Ebola outbreak surge; overburden.
- **Limited access to the affected population** (rural areas, cloud bursting) → **airdrops/mobile distribution** (Rohingya refugee crisis).
- **Domestic barriers and delays** (political/regulatory norms; cross-border supplies are time taking).
- **Many organizations involved** — **inefficient collaboration** is the main reason; **fraud** (supplies shown as done but affected people not getting them) — centralize and use a **blockchain-enabled supply chain** for transparency/visibility.
- **Cost inefficiencies**, waste generation, **lack of trust** between organizations (does donated money reach the affected people).

### 59.12 General Steps (Humanitarian Supply Chain)
1. **Need assessment** — size, quantity required, people/area affected.
2. **Planning** — from where to source, transportation mode, delivery schedule.
3. **Sourcing** — best option is to **outsource to local players** for immediate supply.
4. **Procurement** — little negotiation on cost, but **quality and testing** matter (food supply should not deteriorate health).
5. **Transportation** — road/air connectivity gone; helicopters carry limited supply.
6. **Temporary warehouses** — distribute through local partners/community organizations.
7. **Monitoring and evaluation** — minimize wastage and improve next time.
- **Information/communication flow** is the most important.

### 59.13 Relief Items and Network Approach
- **Humanitarian cargo/relief items:** medical supplies, housing and shelter, **WASH** items, sanitary pads, dangerous items, organization support, food quantities, **ready-to-use foods**, fortified foods (enhance nutrition).
- **Network approach (diagram):** set up supply chains/major houses up to a point; place distribution centers/local distribution centers near the disaster area to meet local demand; if only part of the area is affected next time, the existing supply chain still works efficiently.
- **Australia flooding** — thousands flood-affected, shortage of fresh food; supermarkets introduced **buying limits**, out of stock; not new (COVID-19 too); agencies warned that climate change, drought, fires and heat waves will make this frequent; government depending on the main food industry; the highway was blocked.
- **Resilient food supply chain** — **regenerative** products that maintain soil/fertilizers; **decentralize** food supply chains; local and regional supply chain partners; **diversify** food supply items; **equitable access to food**; **circular food economy** (close-loop supply chain).

---

## Lecture 60 — Assets Management in Supply Chain

### 60.1 Introduction / Definition
- Managing the assets used for the long/short term to ensure **100% availability** and efficient utilization throughout the supply chain — at the vendor, transportation, manufacturing, distribution and customer inventories.
- Broadly **tangible** and **intangible** assets:
  - **Tangible:** manufacturing facilities, warehouses, automated tugs/trolley systems, transportation vehicles, inventory.
  - **Intangible:** warehouse management software, information flowing through the supply chain, **IPR**, R&D, innovation, brand value, customer/supplier relationships.
- Assets enable the efficient flow of **goods, services and information**; in the reverse supply chain the three flows are **bidirectional** (goods return, money refunded).
- **Asset** = that portion of a company's assets directly/predominantly attributable to the operation, supply, manufacture and distribution of the product — **excludes** company cash, cash equivalents and liquid investments in share/other markets.
- Objective: **developing, operating, maintaining and selling assets cost effectively**; maintains the **resiliency and viability** of the supply chain.

### 60.2 Tracking and Maintenance
- Track records — e.g., a camera bought: after how many hours the lens must be changed, the camera repaired → no sudden breakdown.
- Machines bought at different/same times — know when to maintain and how long maintenance takes.
- Warehouse operations/freight carriers — a **post-trip inspection** reveals brake issues → the vehicle goes out of the supply chain; know the time required; regular **planned maintenance** gives alternatives; focus on **scheduled maintenance** for machines, vehicles, physical assets **and manpower** (casual/earned/medical leaves; alternatives; **500 stages → 500 minimum workers**).
- **Comprehensive work orders** — how much work, resources, time, equipment and manpower; track/inventory data historically.
- **Employee and vendor scheduling** — circulate the comprehensive work order to vendors so they know the lots to supply throughout the year (± variation).
- **Institutional knowledge** for new team members — efficient onboarding adds to **intangible assets**.
- Effective asset management supports **uptime** and the team's ability to maintain revenue streams; transparency through technology to track what/where and to regain the original position.

### 60.3 Asset Management Functions
- **Cost control** — scheduled maintenance planning (out of **10 machines, 2** go for routine maintenance → run an extra shift); if **2 more** break down suddenly, delivery cannot be maintained, less-than-truck-load during transportation, orders are lost (inventory not replenished), inventory piles up in manufacturing → cost increases.
- **Revenue management — supply chain finance (a new trend):** vendors supply material and are paid per quality/quantity, typically within **60/90 days**; small players cannot survive 3 months → a **financing institution** provides finance the **same day** the material is delivered; the manufacturer pays the financing institution; the bank takes small interest (**1–2%**); ensures a sustainable flow of finance and maintains revenue at both vendor and manufacturer ends.
- **KPIs, scheduling and work order management** — a comprehensive work order; plan/design the supply chain → procurement → construction of facilities → maintain facilities/equipment → **disposal** after end life.

### 60.4 Asset vs Inventory Management
- **Inventory management** — records routine incoming/outgoing raw material/semi-finished/finished goods.
- **Asset management** — long-term assets kept to produce products; maintained till the end of the life cycle (unless the manufacturing unit is sold); replenishes goods and parts to sell to the customer; regular inspection, cleaning, repair and replacement; spare parts replaced frequently.
- Customers return items to inventory only if dissatisfied; here **users borrow items and return them to the asset pool** (a camera borrowed and returned).
- Minimum contact with each item vs **determines which assets provide value and which are liabilities** (if an asset becomes a liability, replace it — the car example: fuel efficiency gone down, frequent repairs; in Operations Research this is the **replacement problem** — consider scrap value, maintenance value and cost of new equipment; replace when the cost is maximum).

### 60.5 Types of Assets
- **Short-term** (moving in the market) and **long-term** (kept longer).
- Raw material, WIP, finished goods; **packaging material** (with every product) and the **equipment/tools** to convert raw material (lathe machine for turning, molding machine for plastic products).
- **Transportation vehicles** (trucks, ships, airplanes, automated vehicles); **warehouse infrastructure** — tangible (cooling facility, lighting facility, automated tugs, trolleys, tractors, robots) and intangible (warehouse management software for order management/tracking/picking/packing/shipping).
- **Information technology assets** (software, hardware, technological infrastructure for transparency/visibility — blockchain, IoT sensors).
- **Intellectual property** (patents, trademarks, copyrights, secret recipe) and **human resources** (the logistics industry is struggling for talented/skilled human resource due to automated warehouses/transportation management systems).

### 60.6 Asset Management KPIs
- **Mean time between failures (MTBF)** — anticipate future breakdowns; (asset in-use time − unplanned downtime due to breakdown) / total number of breakdowns.
- **Mean time to repair (MTTR)** — total maintenance time / total number of repairs.
- **Overall equipment effectiveness (OEE)** — availability × performance × quality (e.g., a molding machine running 24×7; how many hours it was unavailable; actual cycle time; rejected vs quality products).
- **Asset utilization rate** — utilization up to full potential.
- **Return on assets** — total income / total assets.
- **Maintenance cost**, **downtime**, **asset availability** (% of time available for routine operation), **asset life cycle cost** (cradle-to-grave), **asset performance ratio** (actual/expected), **work order completion rate** (within the time frame), **asset condition index** (how frequently maintenance is needed → deteriorating → replace).

### 60.7 Benefits, Risks and Technology
- **Benefits of end-to-end asset tracking:** cost-effective monitoring (expected **2 hours** delivery took **4 hours** because the carrier truck could not go above **30 km/h**), real-time visibility (take better decisions next time; **Ola/Uber** revised-time messages and alternative search), **sustainability optimization** (predictive maintenance → longer contribution, minimum carbon footprint, fuel efficiency), enhanced control.
- **Risks:** non-optimal efficiency (loss), risk of disruption (transportation/warehousing damage), **asset loss prevention** (theft, unauthorized use — Amazon account details), competitive advantage (if you don't, your competitor will).
- **Technologies:** **RFID** (location, moving or not), **GPS** (track the truck, driver resting/rash driving/wear and tear), **barcode scanning** (Big Bazaar/malls — billing value, inventory left, manufacture time, operator), **IoT sensors** (location, temperature, humidity, vibration — extreme conditions → wear and tear → charge extra), **near field communication** (wireless short range), **Bluetooth** (shorter distance, within the house — pallet, tractor, equipment), **real-time location system** (RFID/GPS/WiFi within a particular area), **cloud-based asset tracking software** (four-wheelers with a chip/GPS, better route), **blockchain** (transparency/visibility of transactions and truck movement), **AI and machine learning** (predictive analytics and predictive maintenance), **mobile apps** (where is my train), **drones** (aerial surveys), **cameras** (find the asset), **edge computing** (device near the data source), **augmented reality** (digital info onto the physical environment), **voice recognition** (Siri, Alexa), **thermal imaging** (emergency supply chain, heat signatures from the body), **ultrasound tracking** (sound waves, indoor assets), **smart packaging** (RFID tags, dynamic chips — customer taken/used the product, packaging destroyed), **telematics** (integrated GPS, cellular and onboard diagnostics), **telemedicine** (wearable devices, smart watches — location in the plant).

### 60.8 Best Practices
- **Comprehensive asset inventory**; centralized record; **standardize the tracking process** for consistency/accuracy.
- **Centralized asset database** (know how many resources moved out and came back).
- **Regular audits** (physical inventory vs records).
- **Asset maintenance protocols** (routine protocols, prevent breakdowns).
- **Real-time monitoring** (immediate visibility into asset location, status and performance).
- **Preventive maintenance schedule** (estimate breakdowns, reduce maintenance time).
- **Asset life cycle management** (stages, depletion, spare parts to upgrade/change/replace).
- **Vendor management** (assets with vendors/suppliers for timely delivery).
- **Employee training** (use data to decide when to replace equipment/assets).
- **Data analytics and reporting** (regularly/routinely for informed decisions; 100% productivity is not possible → aim to make assets available 100% of the time).

### 60.9 Future Trends and Microsoft Case
- **Future trends:** IoT for tracking (real-time monitoring of location, condition, performance), **predictive maintenance**, **blockchain** (immutable records of asset transactions/ownership changes), **AI and optimization** (patterns of asset deterioration, algorithms for when to maintain), **autonomous vehicles and drones** (locate assets), **augmented reality for maintenance** (remote access, digital overlays of manuals/diagnostic tools), **digital twin** (parallel digital world, modeling/optimizing), **sustainable asset management** (eco-friendly utilization), **cloud-based asset management system** (records, maintenance schedules, anytime access), robots and automation, multi-tier supply chain visibility/end-to-end traceability.
- **Microsoft** supply chain (enterprise asset management; **Dynamics 365** solutions, ERP): **Dynamics 365 Finance** (financial management for middle/big companies — revenue recognition, credit management, treasury, organization administration, accounts receivable, tax, payroll, expenses, fixed assets, liquidity ratio, cost management); **Dynamics 365 Supply Chain Management** (asset management, master planning, sourcing, procurement, service management, after-sales services, feedback, fleet management, vendor management, transportation management, production management).
- **Maintenance strategies** (increasing uptime/revenue/profitability): **reactive maintenance** (breakdown then react — minimum uptime/revenue), **scheduled/preventive maintenance** (adds a little), **condition-based maintenance** (only when the condition demands, address that point only), **predictive maintenance** (predict the breakdown before it happens → maximum uptime), **cognitive maintenance** (intelligent operation, learning, interacting with machines → maximum benefit/uptime).

### 60.10 Conclusion
- Effective asset management throughout the supply chain is very important; the flows of **information, finance and product** can be ensured only when the assets are in place (automated warehouses, working robots, transportation management system, proper routing, cost efficiency/effectiveness, quality to the end customer; predictive analytics to manage risk).
- Closing remarks — the course covered various aspects of logistics and supply chain management over **12 weeks**; feedback is important for designing the course better; best wishes for the exam.

---

## Quick-Revision Cheat Sheet

| Lecture | Core Topic | Key Takeaways |
|---|---|---|
| 51 | Assignment Problem Programming | Special case of transportation problem; assign n tasks to n resources; Hungarian method; **c_ij** cost, **x_ij** = 1/0, objective Σ c_ij x_ij; balanced = square matrix (else dummy row/column of 0); opportunity cost table (row min then column min); assignments optimum when allocations = order of matrix; else minimum lines covering zeros, subtract min from uncovered, add at intersections; maximization → subtract from largest or × −1; programmers example (₹120/100/110 → C→p1, B→p2, A→p3), 5 machines/4 jobs → dummy job, 4 lines, 3 intersections; advantages (dynamic optimization, no subjectivity, binary decision, real-time IoT); assumptions (deterministic demand, homogeneous tasks, fixed cost, no transshipment, linear, single-period, non-negative, fixed origins) |
| 52 | Inventory Management | Inventory = items/goods/material kept to sell later (+ equipment/spares/MRO); 3 types (raw material, WIP, finished); services use queue management (barber); terms (bin card, buffer/safety/minimum stock, committed inventory — Swift/Desire tires 500/1000, demand signal, ledger, lead time 2 days, stock card, SKU, stock-out, VMI); types (WIP vs work-in-progress Gantt, transit inventory FOB, decoupling at machines A–E, cycle inventory 10,000 units/2 days); planning process (data analysis big-data stages, supplier/vendor rating 5±1 day, safety stock max sales × max lead time − avg sales × avg lead time, storage space, accuracy+speed, optimize ₹10cr → ₹2cr); limited cycle counts; multi-channel/omni-channel warehousing |
| 53 | Inventory Management (Contd...) | JIT (Toyota/TPS 60s–70s, Dell build-to-order, Harley-Davidson; supplier role 70%+; high initial investment); MRP (ERP/SAP, BOM by PPC, sky manufacturer, Toyota/Intel/Boeing, challenges data accuracy/speed/flexibility/integration); EOQ (holding = ordering cost, √(2DS/H), Walmart/Tesco/Samsung/Toyota, McDonald's/Starbucks/Nestle; challenges constant demand/fixed cost/no shortage); DSI (days to convert inventory, lower better, Pfizer/Ford/Nestle; seasonality/accounting); zero inventory (Toyota; BS3/BS4 bikes sold half price; pull not push; Raymond; Amazon inventory-led + zero); VMI (Maruti → JK Tyre/MRF); ABC analysis (A 20% items ~70% value, B 30/~25, C large/~5%); inventory vs queue management (customer part of process in services) |
| 54 | Supply Chain Digitalization | Replace manual with digital; digitized data management; evolution manual → ERP/SAP (view 10 plants; lacked real-time visibility/agility) → e-commerce (bullwhip 10→12→15); components (big data/analytics, IoT smart refrigerator, cloud, blockchain, digital twins, RPA, visibility platform, cyber security, network optimization GPS, predictive maintenance, supplier collaboration/Zomato, sustainability, resilience, compliance, innovation); five implementation steps; benefits (₹10cr → ₹5cr inventory; 5-day replenish → 6–7 days stock); forcing factors (government/tax, technology, globalization, competition, McKinsey-type); challenges (fake data, talent shortage, change management); healthcare (47% know doctor, 38% check hospital, 77% online appointment, telemedicine); Dell case (2017 transformation; 25+ plants, 2000 service centres, 50 DCs, 3 units/sec, 770 PDCs, 392,000 SKUs, 34,000 containers, 220,000 orders/day) |
| 55 | Smart Supply Chains | Evolved with complexity/interconnectedness; Taylor/Ford → JIT/zero inventory; driving forces (technology, globalization, ERP integration, Industry 4.0); six **smart drivers** (facilities, information, transportation, sourcing, pricing, inventory); hierarchical model (Zhang 2023) — level 0 technologies → smart unit flow (material/information/finance, smart contracts) → smart supply chain network (interconnected, intelligent, innovative, self-organizing/optimizing — 95% rain/50 mm auto re-route); traditional vs smart (transparency, bullwhip data collection, responsiveness, traceability 6–8 months, adaptability); key components (sustainability, agile/resilient, responsiveness, efficiency ~95%, flexibility, real-time visibility, predictive analytics, automation, dynamic optimization); resilience (panic buying, cyber attacks); sustainability (closed loop, profit-people-planet); implementation examples (IoT/blockchain/cloud+AI, smart grid thermal 20%/wind 35%) |
| 56 | Robust and Resilient SC Design | Challenges (Lehman Brothers 2008, COVID-19 China, Russia-Ukraine, Bangladesh, Sri Lanka); risk mitigation (reactive) vs management (predictive); operational + financial risk; redundancy, supplier diversification, contingent plans; vulnerability (natural/political/economic — COVID/demand shift); robustness (withstand strength = flexibility, adaptability, agility); resilience (bounce back; disaster relief — medical then food then clothing); PPRR (Prevention, Preparedness, Response, Recovery); COVID responses (breweries → sanitiser, Ford → ventilators, multi-sourcing); nearshoring; carriers 60% road/1% air/5–6% train; temple of resilience (strategy foundation, product design floor, 4 pillars — agility, collaboration, risk management, design; roof); JD.com case (self-operated → 60% direct, minimal intermediaries, high collaboration, automated planning); Nissan 18–20 days after Japan earthquake |
| 57 | 21st Century Supply Chain | Continuous transformation driven by technology, globalization, evolving customer preferences (2%→3%→5%); interconnectedness positive/negative; key aspects (digitalization/automation, visibility/transparency, blockchain, globalization/nearshoring, resiliency — recessions now frequent); sustainability & CSR (Delhi 15-year vehicles, BS4 ban, Myntra paper packaging, Europe cycle delivery, carbon-footprint info); customer centricity/omni-channel (MakeMyTrip, IRCTC, ixigo); 2024 trends (visibility must-have, sustainable brands, regionalized supply chains, RPA, AI decisions); circular vs linear economy (LCA software, ESG); regional supply chains; risk steps (A/B/C model — C ~70–80% items 5–10% value, 20–25% items ~80% cost; generative AI; downtime cut 35–45%; AI forecasting error −50% per McKinsey); India (competitiveness gap $180 bn, 12–13% GDP vs 8%, Vision 2030 CII Sep 2020, 64% road, 10.5% CAGR, train 15–20 km/h, fragmented trucking); five digital components; innovation/collaboration/sustainability |
| 58 | Sustainable Supply Chain | Customer awareness + regulators; environmental + human + economic; UN definition (meet present without compromising future); triple bottom line (Johan/Elkington; people, profit, planet; LCA software; SAIL CSR; social — gender equality/labour rights; 2–10% more willingness to pay); Unilever (Brazil drip irrigation, half sales from emerging economies); Walmart (100% recyclable energy, skylights, 80 vs 100 per container); key metrics (carbon footprint, energy, water, waste — sugarcane husk→furnace electricity, supplier diversity, ethical sourcing, supplier compliance, PCF, ship, social impact); six drivers; seven ways (pain points/PCF, optimize transport 29%, sustainable partners GRI 408/409 + ISO 14001 + ESG reports, minimum inventory, reuse byproduct, eco packaging 1% biodegradable, nudge regulators — petrol 27% vs electric 10% tax; Starbucks −50% plastic); challenges (cost, ROI, steel industry, changing norms, resistance, customer interest); trends (circular economy, data-driven); survey (upfront cost, 8/10 increasing effort, 61% save cost, 51% compliance, 40% partner pressure) |
| 59 | Emergency Supply Chain | Complex emergency (Joint Logistics Enterprise — war, food insecurity, pandemics, social conflict; displaced people/COVID reverse migration, political hindrance, infrastructure/security constraints); specialized framework, rapid mobilization, coordination (military/government/NGOs/individuals); disaster cycle (search & rescue → need assessment → medical supply → resource mobilization → relief → recovery → rebuild; communication channel first); prioritization air → heat → water/food → medical; disruption vs emergency (identity same vs reactive); success = lives saved not cost; implied demand uncertainty; four aspects (urgent diverse services, real-time info, efficiency over profit, collaboration); solutions (early prep/stockpile 6 months–1 year; transparent communication; blockchain/message-based systems); humanitarian supply chain (need assessment → planning → local sourcing → procurement quality/testing → transportation → temporary warehouses → monitoring); relief items (WASH, ready-to-use/fortified foods); cases (Nepal 2015 air ambulance, Hurricane Maria 2017 power first, Ebola overburden, Rohingya mobile units, Haiti 2010 pre-positioned, Zaatari nearshoring, COVID same-vaccine second dose); challenges (demand uncertainty, limited access, barriers/delays, fraud, trust); Australia flood + resilient food supply chain (regenerative, decentralized, diversified, equitable, circular) |
| 60 | Assets Management in Supply Chain | Tangible (facilities, warehouses, vehicles, inventory, automated tugs) vs intangible (WMS software, information, IPR, R&D, brand, relationships); asset = portion attributable to operation/supply/manufacture/distribution (excludes cash/liquid investments); cost control (10 machines, 2 routine + 2 breakdown → LTL, lost orders); supply chain finance (60/90 days, same-day finance, 1–2% interest); asset vs inventory (borrow/return to pool; value vs liability; OR replacement problem — scrap/maintenance/new cost); types (short/long term, packaging, IT, IP, HR); KPIs (MTBF, MTTR, OEE availability×performance×quality, utilization, ROA, life cycle cost, condition index); benefits (2 hr → 4 hr at 30 km/h, Ola/Uber, sustainability); risks (theft/unauthorized use, disruption); technologies (RFID, GPS, barcode, IoT sensors, NFC, Bluetooth, RTLS, cloud, blockchain, AI/ML, drones, edge computing, AR, voice, thermal imaging, ultrasound, smart packaging, telematics, telemedicine); best practices (centralized database, audits, preventive maintenance, life cycle mgmt, analytics); future trends (IoT, predictive maintenance, blockchain, AR, digital twin, cloud); Microsoft Dynamics 365 (Finance + Supply Chain Management); maintenance strategies (reactive → scheduled → condition-based → predictive → cognitive); conclusion — asset availability ensures product/information/finance flows |

---

*End of Decade 6 notes (Lectures 51–60).*
