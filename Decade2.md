# Logistics & Supply Chain Management — Exam Notes (Decade 2: Lectures 11–20)

**Course:** NPTEL Online Certification — Logistics & Supply Chain Management
**Instructor:** Dr. Vikas Thakur, Assistant Professor, Department of Humanities & Social Sciences, IIT Kharagpur

> These notes are compiled strictly from the professor's lectures (Lec11–Lec20). All definitions, figures, and examples are the ones used by the professor in the sessions.

---

## Lecture 11 — Tools for Improving Logistics Efficiency (Contd.)

### 11.1 The 7 QC Tools (K. Ishikawa)
- Given by **Professor K. Ishikawa**; used as a **sequence** starting from diagnosing a problem to reaching and implementing the solution, and then tracking performance.
- The seven tools: **cause-effect diagram, flow chart, check sheets, Pareto charts, histograms, control charts, scatter diagram.**
- Recap of the previous tool (**PDCA / Deming wheel**): define a process → process gives output → compare with standards → if deviation, take corrective & preventive action (change process, raw material, output, or technology); if no deviation, continue.
- The professor notes quality tools are often used by **production-line workers** — "in the manufacturing industry major problems are solved by those illiterate people working on the production line" because they repeat the same action (e.g., producing **10,000 units/day**, doing the operation 10,000 times). Quality tools cannot be used overnight; a team must be prepared to collect data, analyze, and prioritize solutions in phases.

### 11.2 Tool 1 — Flow Chart
- A flow chart gives a **quick understanding/visibility** of a process (better than reading long paragraphs). Different **shapes** represent different stages (start, decision, end highlighted differently).
- **Electronic-gadget manufacturer example:** assembly starts at step one (component checking), then several **assembly stages**, then a decision point — is a quality check needed or is it error-free/100% inspection? If needed, go for a **check sheet**, take samples, and check for defects. If a defect is found, re-check whether the **component is faulty** or something is wrong with the **assembly line**; if not required, continue to **final product testing** (another decision point), then final assembly → production complete.
- A flow chart can also be drawn for the **complete logistics network**: first supplier → transportation → manufacturing facility → stock/carry-forward agents, wholesalers, distributors, retailers → end customer.
- **Inference:** flow charts **reveal bottlenecks and inefficiencies**.
- **Bottleneck example:** five assembly stages with times **5 s, 6 s, 4 s, 8 s, 6 s**. The **8-second stage is the bottleneck** (almost double the next). If the stage before it processes **two products** in that time but this stage passes only **one**, only **50% of semi-finished products** pass; the rest become **pending stock** at that stage. Solutions: think of **parallel stages/workstations** (temporarily assign another workstation) or **additional training** or **change of technology** so all stages are uniformly designed (around **4–4.5 s**) and no stage has pending work.
- Flow chart also helps **quality**: if a particular critical stage (e.g., packaging) is where most complaints come from, increase inspection there. **Misconception:** quality does not mean checking — the target should be that **quality is built into the design** of the product, packaging, process, and warehouse (e.g., the system should automatically give an **alarm** when only a few days/weeks are left so the stock is rotated first).

### 11.3 Tool 2 — Check Sheet
- Dr. Ishikawa's concept for **collecting data** — a way of recording where faults happen. Daily-life example: the **feedback form** given on a train or flight to rate staff behaviour, cleanliness, and service.
- Records number of occurrences by defect and day; e.g., **Monday: bottle broken = 2, cap loose = 0 (`-`), missing label; Tuesday: cap loose = 2**.
- Helps identify the **operator, location, date, section** where the problem consistently occurs. Reasons may be: on **weekends** defects are more (people rush to leave the workstation for weekend plans); **Monday** more complaints (difficulty concentrating after enjoying the weekend).
- **Electronic-components manufacturing case:** track **date of production, type of defect** (soldering issue, component misaligned, damaged/faulty component, faulty packaging/process), and **location of defect** (A/B/D shift, workstation 5th/10th/12th).
- **Actions:** identify the root cause; define specific quality check sheets for those stages; **targeted training** for the particular operator; and note that the **machine** can also be at fault (continuous working causes **wear and tear**, even in a fully automated/robot warehouse).
- Result: improvement in quality → sustainable environment of quality management.

### 11.4 Tool 3 — Histogram
- **Pictorial representation** of the **frequency** of faults (fault 1, fault 2, fault 3…), giving a **quick view** and enabling **month-wise comparison** (January, February, March).
- **Restaurant chain case:** to enhance food quality and customer satisfaction, they collected **delivery-time data** — how many deliveries in **10–15 min, 15–20 min, 20–25 min**. A **normal distribution curve** can be drawn; maximum time falls in one/two bins. This shows where to speed up (e.g., keep **half-cooked items** ready for continuous-demand products).
- Enables **real-time performance monitoring** by tracking delivery times; reduces the peak (e.g., 25–30 min) and makes service **consistent** — consistency matters because a customer who gets **5 min** service one day and **25 min** the next day is highly dissatisfied; if the store consistently takes **15–20 min**, the customer is mentally prepared.
- Defects can also be shown by **shift (1, 2, 3)**; e.g., reasonably **shift 1 defects are very high** and shift 2 increasing. Defect types: **wrong color, does not light up when turned on, did not turn on, too small/size not fitting, wrong label, wrong size information**.

### 11.5 Tool 4 — Pareto Chart (80-20 Rule)
- **Pareto principle (80-20 rule):** **80% of problems come from 20% of the reasons.**
- Professor's life analogy: a few big decisions (education line → career, own venture vs. service, life partner, post-retirement plan) — these **20% decisions** carry **80% weightage**.
- **Inventory example:** **20% of items/components carry the maximum price/cost**, the other **80% of items contribute only 20%** — this is the **ABC analysis** of inventory to be covered later.
- A Pareto chart **arranges the histogram bars** so the biggest problems are on the left; you prioritize the 20% of problems that 80% of customers face.
- Used to prioritize issues: are they mostly related to **packaging, transportation, outdated inventory (warehouse management)**?
- **Electronic gadgets case (scratched screen, battery issues, missing components):** combining **three** issues (**scratched screen, battery issues, missing components**) gives about **80%** of the problems — solve these 20% and 80% of the problem is solved. Then do **root-cause analysis** to find where scratches happen (storage, packaging, cleaning, or installation at site).

### 11.6 Tool 5 — Fishbone / Cause-Effect Diagram (Root-Cause Analysis)
- Also called the **cause-effect diagram** (Ishikawa); shaped like a fish — the **head is the problem**, branches are categories.
- **Packaging problem example:** problem may be due to **manpower on the workstation, technology, equipment used to pack, poor working conditions, fault in raw material**, and other issues.
- Then drill into sub-causes: for **manpower** → did not undergo proper training, unhappy with work environment, disturbed personal life, wrong skills for the job, salary, health issues. For **training** → why was that person placed there; who is at fault (HR team, placement team, induction people). If HR is at fault → HR needs to change the policy.
- Uses a **brainstorming session** with **5-Why analysis** (or 3-Why/7-Why): keep asking "why this happened" until the **root cause** is reached.
- Then take **corrective action** — additional staff, optimize workflow, or special training. When the root cause is found, the **employee feels motivated and connected** to the organization; overall performance improves and the original problem (customer satisfaction) is resolved → **customer loyalty**.

### 11.7 Tool 6 — Scatter Diagram
- Used to **track the effect of a solution** on results (independent variable on X-axis, dependent variable on Y-axis).
- **Example — compensation vs. results:** if compensation is increased from point A to point B, does the number of complaints **decrease** (negative correlation) and does productivity **increase** (positive correlation)? If the points are **staggered**, there is **no relationship** (increasing compensation does not motivate the employee and performance does not improve).
- **Training example:** number of **training programs** vs. **job performance** shows an increasing trend → suggests training programs increase overall performance. Regular checks can track and improve performance.

### 11.8 Tool 7 — Control Chart
- Statistically controls quality; given by **Professor Shewhart**. The process varies around a **mean (middle line)** with an **upper control limit (UCL)** and a **lower control limit (LCL)**.
- As long as the process is **within the range**, it is "controlled." If it goes **beyond the range**, stop and take corrective action.
- Range is often set at **±3 sigma**. Used to distinguish **assignable (special) cause** from **common cause** of variation:
  - **Common cause** — small natural variation (environmental conditions, human intervention, wear and tear even in automation); cannot be removed.
  - **Special cause** — a big problem; requires corrective action.
- Implementing control charts **reduces variation** in the quality of products delivered.
- **Summary of the 7 tools sequence:** flow chart (big picture), check sheets (data collection), histogram/Pareto (data analysis, quick view + prioritization), fishbone (problem identification), scatter (results of a solution), control chart (keep within range), Pareto (prioritize the solution when multiple solutions exist).

### 11.9 Quality Circle
- A **voluntary, not very formal** group, usually **8–10 people**, who discuss an issue (e.g., packaging).
- Members come **voluntarily** from different departments linked to the problem: one/two from **production, quality, R&D, maintenance, training & development**, and **accounting** (accounting checks cost feasibility).
- They meet **regularly**, do brainstorming, find solutions, and suggest them to **higher/top management**.
- Roles:
  - **Top management** — support the QC, sanction the budget to implement solutions, provide awards/rewards so members stay motivated to keep meeting as informal teams.
  - **Steering committee** (senior people) — evaluate whether a QC is really required for that problem, whether objectives are within broader organization guidelines, and whether out-of-the-box suggestions are acceptable given **cost, ethical, and legal constraints**.
  - **Coordinator** — coordinates between the quality circle and higher management; keeps track of activities.
  - **Facilitator** — a senior officer of the department; arranges training programs, sets up links between QC and management, ensures a participative culture.
  - **Leader** — leads the team, defines the problem and its aspects, elaborates with the team, and consolidates suggestions/feedback (with cross-questioning to validate the solution).

### 11.10 5S Philosophy (Japanese)
- **Seiri, Seiton, Seiso, Seiketsu, Shitsuke** — a housekeeping approach to manage inventory properly in the warehouse and sustain it.
  1. **Seiri (Sort)** — sort material: by pin code, by product, by product requirement; cold-storage products in their area, delicate items handled/stored properly.
  2. **Seiton (Set in order)** — arrange items by size, use, or product nature; design shelf space.
  3. **Seiso (Shine)** — maintain cleanliness of the workplace for smooth functioning and reduced accidents.
  4. **Seiketsu (Standardize)** — standardize the process so it can be done repeatedly (not one day set in order and the next day back to the old way).
  5. **Shitsuke (Sustain)** — once standardized, sustain it forever.

### 11.11 Benchmarking
- Decide your **KPIs**, then find the KPI of the **best player** in the market and identify the **gaps**; the concept of **house of quality** and the **balanced scorecard** approach (designed with respect to supply chain/logistics management) help here.
- House of quality identifies the **present situation** vs. the **best-player benchmark** to find gaps and **best practices/opportunities** (why delivery is delayed, why wrong products ship frequently, why there is always a shortage of inventory, why defective products reach the customer → something wrong with the courier partner).
- **Six steps of benchmarking:**
  1. **Define the objective** — the area to improve (e.g., let us first improve transportation, since transportation contributes **60–70%** of cost).
  2. **Identify the KPIs.**
  3. **Gather data** — our transportation KPIs vs. the industry leader's (e.g., if comparing delivery, compare with **DHL**).
  4. **Select the partner** — exchange information with courier/logistics/transportation partners on where to improve.
  5. **Analyze and compare** data to see if significant improvement occurred.
  6. **Identify the opportunity** — e.g., addressed 30%, still go further; the next step may improve another 50% and cut complaints by another 50%.

### 11.12 Conclusion
- Goal = **customer focus** — deliver the best quality product and best experience; set KPIs in order and "shine" them every day. Requires an environment of **continuous improvement** (PDCA continuous), **employee empowerment**, and **QC circles**; supplier role is important to control quality at the supplier end. Product design and process should meet customer expectation and be **defect-free**.

---

## Lecture 12 — Reverse Logistics

### 12.1 Introduction — Why Reverse Logistics
- Return rate is very high — around **25–30% in some cases**, often more.
- Reverse logistics is a **parallel system**: initially products flow from raw-material suppliers to the end consumer (forward); now the **reverse flow** is equally important and must be **equally efficient**.
- **Challenge:** you cannot charge anyone for managing the reverse supply chain — it is **additional cost**. But it can be a very efficient **source of income** if you efficiently **recycle/remanufacture** unused or used products.
- Other terms used: **retro logistics, reverse supply chain, reverse logistics flow, reverse flow, backward supply chain, return management, after-market logistics, after-market supply chain**.
- **Distinction:** logistics (forward/reverse) takes care only of **transportation, warehousing, distribution**; **supply chain** (forward/reverse) includes **all activities** — raw-material extraction, packaging, manufacturing, assembly lines, final packaging, marketing, order recording, selling, distribution.

### 12.2 Product Returns — Types
- Reverse logistics = the flow in the **opposite direction**, handling **waste and returns**. It is **not only waste** — it can be a **fresh/unused product** (e.g., ordering from Amazon/Flipkart/eBay and simply not liking it → shipped back to the seller).
- **Three ways products come back from the customer:**
  1. **Customer returns** — customer did not like the product. Value is fully there but **packaging is destroyed** (e.g., **shirt** — steel pins, plastic pins, card papers used; customer damages packaging while trying it, so **100% packaging recovery cannot be ensured**).
  2. **Under warranty/guarantee** — service partner/employee visits on-site and replaces components **free of cost** (coming from the forward network) or the product is shipped back to the manufacturer.
  3. **End of life** — product fully consumed (e.g., **home appliances**: average age is **12–15 years**, can extend to **18–20** with care or fall to **8–10** without care).
- **Secondary market concept:** refurbished/reworked/repaired/second-copy products sold at a **reduced price** in a **secondary market** (not the primary market).

### 12.3 End-of-Life and Modular Design
- **Home appliances example:** the outer container, plastic and steel components have **minimum wear and tear** and can last **30–40–50 years**, but the overall life is **12–15 years** because the **motor and electronic components** have limited life.
- **Modular design** solution: replace only the limited-life parts. E.g., in a **TV**, if the **sound panel** is faulty, take it out and fix another sound panel; in an **AC**, if the **outside motor** fails or the inner **circuit board** fails, replace just that board; wherever the problem is (inner or outer unit), replace the module.
- **Economic/marketing angle:** you cannot claim an AC lasts 100 years — service partners and the marketing strategy need repeat sales. But if we are **environment/sustainability-conscious**, we extend the end of life.

### 12.4 Aquaguard AMC and Service-over-Product
- **Aquaguard** does not sell products — it sells **services**: the **AMC (Annual Maintenance Contract)**. If anything goes wrong with the purifier, it is **replaced free of cost** as long as you are under AMC. It is not truly free — you already purchased the AMC.
- The idea: talk about the **end life of the customer**, not the product — "as long as you are there you will use Aquaguard."
- **AC proposal example:** if an AC company fixes the unit as per room size/cooling requirement and takes full responsibility to maintain it as long as you take their services (and takes it out when you stop), it is a **win-win** — the manufacturer is motivated to use **more sustainable technology/raw material** (better plastic and steel that can be reused again and again).

### 12.5 Definitions
- "Going the wrong way on a one-way street."
- **Carter and Elram:** the **return upstream movement** of goods or material resulting from **reuse, recycling, or final disposal**.
- Under the umbrella of **product recovery management**.
- **Council of Logistics Management:** planning, implementing, and controlling — in an efficient and cost-effective way — the flow of raw material, in-process inventory, finished goods, and related information from the **point of consumption to the point of origin** (reverse).
- **Disposal debate:** nothing is "totally waste." Even a car used 20–25 years — the steel cannot make another car, but can be **melted** into **steel rods/sheets** used for **roofing** (where safety parameters matter less). After recycling, material not useful in the same industry can be a **raw material for another industry**.
- **Reverse flow network:** collect waste (byproducts, rejected material, warranty, end-of-life, fresh returns) → store in a warehouse → **refurbishment center** recover value (clean, iron, re-apply components, new primary packaging, new secondary packaging, labeling, billing info) → quickly available in the distribution network for **reselling**.

### 12.6 Reverse vs. Forward Logistics
- **Forward:** raw material → manufacturer → distribution chain → retail industry → customer picks up.
- **Reverse:** **collection centers** → **consolidation center** → sorting → treatment.
- **Why consolidation/sorting is needed:** e.g., 100 items sold and **30 return**, a small amount. When collecting returns from **customer 1, 2, 3, 4** (grocery item, shirt, shoe, grocery), **mixed-up items** come in — so **consolidation and sorting centers** sort **industry-wise** and then try to recover value. Reverse supply chain is **not as easy to set up** as forward because returns come from **different industries and different customers**.

### 12.7 Reverse vs. Green vs. Sustainability
- **Reverse logistics** — product returns, marketing returns, country returns.
- **Green logistics** — taking care of the **environment** while distributing: end-mile delivery by **electric bikes/cycles**, **customer pickup locations**, alternate resources (not petrol/diesel), **recyclable packaging**, minimizing packaging size.
- **Sustainability** — takes care of **environment + social + economic** aspects.
- Reverse logistics **adds to** green logistics and sustainability, but must be **efficient**.
- **3 R's:** reuse, reduce, recycle — e.g., if you purchase Aquaguard services, you won't throw it out after 10–15 years as long as they maintain it (you keep paying AMC).

### 12.8 Why Reverse Logistics is Important (Factors)
1. **Government policies and legislation**
   - **Netherlands:** it is the manufacturer's responsibility to **take back** the product (e.g., the **car industry** must take the car back after usage and ensure material recovery — cannot throw it into the environment).
   - **Germany:** the **packaging ordinance** requires collection of **all sales packaging material**.
   - Some countries make it **mandatory** for suppliers to carry packaging back to the warehouse, and packaging should be **100% recyclable/reusable**.
2. **Economic consideration** — the claim that it needs initial investment that distracts from the main product is a **misconception**. If outsourcing, the third party charges money anyway — so set up your own network and extract maximum value. In many countries there is a **very relaxed tax structure** for recovering value from scrap. **Waste handling and disposal costs are also increasing.**
   - **ACC cement example:** ACC developed a reverse logistics network in the local community, collecting the community's **waste as part of CSR**, **burning it to produce energy** to run their plants — reducing energy consumption and taking care of the environment.
3. **Environmental consideration** — government/regulatory bodies push organizations to control **carbon emission**; can be used as a **marketing tool** ("green product, green supplier, green manufacturer"); shift towards **buying services instead of products** (Aquaguard; AC).
4. **Effective waste management** — electronic industry is becoming **use-and-throw**; flat TVs/mobile screens **cannot be repaired** (complex integrated circuits with millions/trillions of components on a tiny chip) → **modular design** (picture control panel, sound control panel, quality control panel, signal receiving/transmitting modules).
   - **80% of mobiles are replaced every 2 years** — where there are **100 crore** mobile users, **80 crore** come back after 2 years as waste.
   - **Sources of e-waste:** municipality collection points, electronic industry waste, retailers, and the **informal recycling sector** in India/developing nations.
   - **Challenge:** dangerous waste (radioactive, infectious) — e.g., hospital syringe plastic recycled without chemical disinfection.

### 12.9 Conclusion
- Reverse logistics is a parallel, equally important system. Managing returns is a big challenge (no one to charge) but also an **opportunity** (source of income). Leads towards **green logistics and sustainability** dimensions. Continued in the next session.

---

## Lecture 13 — Reverse Logistics (Contd.)

### 13.1 Key Aspects
- **Product returns** — due to **defects, damages, overstock** (retail partner overstocking), or **customer dissatisfaction**.
- Inspect returns:
  - **Unused product** → check whether new packaging is required (cleaning, ironing depending on product).
  - **Used product under warranty** → inspect how much value is left.
  - **End of life** → identify components that can be refurbished/reused/recycled; roughly **15–20%** cannot be used anywhere → **disposal** (if the ultimate option).
- **Incinerating waste** — use the energy generated to convert into **electricity** or another form. Fundamental concept: **energy cannot be created or destroyed**, so why waste it?
- **Remanufacturing/refurbishment** — take out parts, use them in another product, or repair/clean/reassemble.
- **Recycling** — shred packaging material; melt plastic into **plastic grains** and reshape into an on/off switch, mobile casing, remote-control casing, electrical components.
- **Final disposal** — for hazardous/infectious items, careful handling, disinfection; follow guidelines.
- **Warranty and service management** — repair/replace components; manage the replaced/used/destroyed components.
- **Asset recovery and remarketing**:
  - Shoe material may not make another shoe but can be used elsewhere (road metalling, compost, fertilizer from kitchen waste).
  - Sell in the **secondary market** at reduced cost, not the same market.

### 13.2 Supply Chain Optimization (Reverse)
- Optimize the reverse flow just like the forward flow.
- **Traceability** — software can quickly analyze how much value is left in a particular waste.
- **Collection center efficiency** and **consolidation** — if only 20% items return, how do you ensure economies of scale? **Combine/collaborate** with another partner to utilize the full container capacity for transport back to the seller.
- **Warehouse optimization** — minimize inventory, rotate stock quickly back to the market.

### 13.3 House of Reverse Logistics — Structure
- First clarify the **reason**: regulatory pressure, social/corporate responsibility, environmental concern, customer awareness.
- **Input** — used part/material collected from customers → **forecast** properly to design the distribution-network/consolidation-center capacity.
- **Process** — **disassembly** (very important — find components with value left), inventory management, supply chain, repair, refurbishment, manufacturing, recycling.
- **Structure** — set up location and inspection/consolidation center; integrate manufacturing units who recover value and reassemble.
- **Output** — price the remanufactured product and set up customer relationships.

### 13.4 Customer Perception Challenge
- Customer welcomes **recyclable packaging** (packaging has no use after transport).
- But a **shirt made of recycled material** may make the customer hesitant — "if I am paying for a new shirt why should I wear the old one?" Technical reality (recycling into new fabric) exists, but the **perception** that it is used/repaired/remanufactured is a challenge for the marketing team to overcome.
- Sometimes sell these products at **lower cost in the secondary market**, presenting the fresh products (coming directly from ore → "fresh steel") as quality-assured.

### 13.5 Steps in Reverse Logistics
1. **Gate keeping** — return of goods received and checked; customer communicates with the company whether the return is **authorized**. If no → compensate directly; if yes → **verification** (customer hasn't damaged it, packaging present, seal not broken; checks depend on the product). If no again → send back to customer (not accepted); if yes → return accepted; identify whose fault (courier partner/manufacturer) → **compensation** (new product or money back). Collect the old destroyed product.
2. **Collection** — whose responsibility: company directly, third party, or the customer (some companies offer a **coupon/discount on next purchase** if you deposit back). 
   - **Policy idea:** if the return rate is normally 25%, give customers with a return rate **below 5%** free delivery for the next 10 deliveries / 1 year / 6 months, or give **free Amazon Prime membership** (worth ~**₹1,500/year**) if they return less than 2% — reducing the 22–23% returns and maintaining seller relationships.
   - Then ship, re-check the product; **exchange** if damaged and not the customer's responsibility; transport to the nearest **service point/consolidation center**.
3. **Sorting** — sort returns onto different conveyor belts.
   - **Canon case study:** to collect used **cartridges**, Canon gives **prepaid shipping coupons** to customers (customer need not spend; customer feels encouraged). Customers return cartridges directly or through Canon's logistics/courier partners. Loyalty: 5%/10% off on the next cartridge if purchased from Canon. Done in **24 countries**.
   - Sorting example: a big packet may contain **t-shirts, undergarments, toys, appliances, books**; returns segregate industry-wise — clothes to the clothing treatment center, groceries to the grocery warehouse, books to the books warehouse. **Cold-storage/perishable items usually have no return policy.**
4. **Processing** — three stages; choose from a list of processing activities depending on the **age, condition, characteristics, nature** of the product. Even after remanufacturing/refurbishing/new packaging, if you cannot sell in the same market, it is an **economic burden** — need to handle the **three sustainability dimensions**.
5. **Treatment** — repack, repair, disassemble, reassemble, reconfigure, remanufacture, update, upgrade, recycle, or **donate** (if useful elsewhere), or sell in the **secondary market** at lower price.
6. **Disposal** — for hazardous material, chemical disinfection; **incineration** at **1000°C**, sometimes more than **1200°C**. Smoke passed through **water** so harmful elements don't go into the air; the ash (hazardous if the waste is hazardous) can be used as **fertilizer** or deep burial (landfill). Alternatives: **microwaving, autoclaving**.
- **Recovering energy:** use the heat energy where there is no alternative. **Hybrid engines example** — **Maruti Grand Vitara** hybrid engine promises ~**30 km/litre** (from ~15 km/l). Running on fuel (petrol/diesel), the **kinetic energy of moving wheels is converted to electrical energy** to charge the battery; below ~**60 km/h**, the battery runs the vehicle. No charging-station limitation (unlike EVs).

### 13.6 Factors for Successful Reverse Logistics
1. **Visibility/transparency** — track products, understand recoverable value, identify bottlenecks/delays and areas of improvement; tap all stakeholders (sometimes lacking proper collaboration with customers to collect the product after use).
2. **Efficient return management** — streamline workflow; clear return policies; quickly place the returned item back for resale.
3. **Product recovery and disposition** — maximize recovery (recycle whole product or use components); minimize disposal.
4. **Tracking feasibility and collaboration** — with suppliers, manufacturers, retailers, service providers. Example: if you claim to be a green manufacturer but the retailer refuses to accept returns (no space), your **strategic alliance is not good** — give the retailer enough reasons, maintain the industry relationship.
5. **Network design** — flow of return products/material **and information**; software can analyze end-product value and remaining life of components and share with supply chain partners → minimize lead time and processing/collection time; pick up quickly from the customer.
6. **Technology integration** — data analytics to predict demand for returns and end-of-life management; automated/robot-controlled warehouses; predictive analytics to maintain recycled-product inventory.
7. **Comply with regulatory requirements** — regulatory authorities appreciate when you take care of end-of-life, byproducts, and packaging.
8. **Customer experience and satisfaction** — e.g., a courier partner delivering the product can **collect the packaging** at the same time, enhancing the customer's involvement with the brand.
9. **Continuous improvement and innovation** — track performance matrices and stakeholder/customer feedback via transparent tracking technology.
10. **Sustainability and corporate responsibility** — take responsibility for byproducts and carbon emissions, not just the marketed product.

### 13.7 Performance Measures (Reverse Logistics)
- **Return rates** — high = products not meeting expectation; low = meeting expectation.
- **Return processing time** — how quickly returns are processed/repaired (shorter is better).
- **Recovery rate** — how quickly value is recovered and waste minimized. (Myth to change: "refurbished hardware was once defective.")
- **Regulatory compliance** — how often environmental norms are met; carbon footprint calculated and compared.
- **Disposition cost** — direct and indirect cost of disposing (transporting, storing, handling, burning, ash management, pollution).
- **Transportation cost** — carrying the product from end customer to fulfillment/warehouse/manufacturer, or shipping components back to vendors.
- **Inventory holding cost** — of inefficient products; sell quickly, reuse components, or give components to another industry as raw material (steel from cars/aeroplanes → steel rods/sheets).
- **Environment impact** — carbon emission, energy consumption, waste generated.
- **Continuous improvement** — tracking performance, innovative packaging technology, supplier collaboration, trained manpower, technology adoption (RFID, IoT, AI), risk management/contingency plans (product recalls), reverse supply chain integration, **circular economy** initiatives.

### 13.8 Case Studies
- **Amazon:** promises cost-free returns to build trust and attract traffic, but return volume increases. In **2021, $761 billion** of merchandise was returned to retailers — increasing **15–20% every year**. Amazon avoided more than **2 million tons** of packaging material since **2015**; reduced **41% per-shipment packaging weight**; avoided **37,150 metric tons of plastic** globally. **Product donation** — software identifies remaining value and donates via local community organizations to the needy.
  - **SIP (Ships In its own Packaging):** reduced **14 packaging components**, reduced volume by **69%** (so cost also reduced) — only primary packaging, no secondary packaging/labels needed.
- **IKEA:** minimizes waste, maximizes resource recovery, reduces carbon footprint. Collaborated with stakeholders and customers; **product returns management** gives **full refund** within a specific time; inspect, repair, and make available for the next life cycle. **Material recovery** of wood, metal, plastic. Ensures **durability, repairability, recyclability**; reduces waste going to **landfills** (landfill cost rising). Requires an efficient **collection/transportation network**.

### 13.9 Conclusion
- Reverse logistics is crucial because **customers are more aware** and **regulatory authorities force sustainability**. You must develop a **parallel distribution channel** to collect end-of-life, warranty, semi-used, and unused products back to manufacturing, sort, recover components, and sell (not in the same market — in the **secondary market at reduced cost**). Next: green logistics and lean logistics → ultimate **sustainability**.

---

## Lecture 14 — Green Logistics

### 14.1 Reverse vs. Green vs. Sustainability (Quick Review)
- **Reverse logistics** — efficiency/effectiveness of moving products from the **point of consumption** back to the manufacturing unit, refurbishment center, or raw-material supplier.
- **Green logistics** — takes care of the **environmental aspect**; efficiency/performance/effectiveness evaluated by **how much we deplete or support the environment** (indicator: **carbon footprint** of manufacturing, delivering, transporting).
- **Sustainability** — next version: **environment + economic + social** dimensions (leads to sustainable supply chain management).

### 14.2 Green Supply Chain Functions (In Sequence)
1. **Green raw material** — the first step/stakeholder is the raw-material supplier. Example: **electric vehicles** reduce pollution, but if the **electricity comes from burning coal**, it is equally damaging — so find energy sources from **renewables** with minimum impact.
2. **Green design** — in R&D, design the product for minimum impact: easy to repair, implements the **3 R's** (reduce, recycle, remanufacture).
3. **Green purchasing** — suppliers provide green supplies; use **alternative fuels** to minimize carbon footprint.
4. **Green production** — converting raw material into finished goods using **renewable energy**; eliminate wastage; minimize component use; increase product life; ensure quality (producing defects uses more resources than required).
5. **Green warehousing** — use **automation**, **solar energy**, efficient material handling.
6. **Green distribution** — end distribution by **electric vehicles, cycles, drones**; consider the share by road/ship/air/train and the carbon footprint (**ship** and **drones** can be more efficient).
7. **Green marketing** — record customer expectations/preferences and meet them in an environment-friendly way.

### 14.3 Green Transportation
- **High emission of CO₂ gases** — increased to **71% in 2016** and still increasing; projected to be **50% more**. Transportation is a big reason for greenhouse-gas emissions/climate change.
- **Delhi example:** during winters you **cannot breathe easily** → the Delhi government introduced the **Odd-Even formula**; restrictions on certain diesel engines; **BS4**-type technology limits; **trucks older than 15 years cannot enter** certain areas.
- Road delivers ~**60%** of products → huge source of pollution/carbon footprint.
- **Green procurement and logistics** — purchase products/services that are **less harmful**; it must start from procurement of raw material — tie up with suppliers.

### 14.4 Green Warehousing and the Inventory-Waste Link
- **Refrigerator example:** keeping **10 items vs. 20 items** in your fridge → energy consumption will be **higher (not exactly double, but higher)**. Cold storage always keeps much higher inventory.
- Why keep inventory? Because demand is uncertain — because **predictive analytics/forecasting** wasn't done and buying behavior/pattern isn't known. Meeting unexpected demand this way means you are **not a green distributor/supply chain**.
- Extra inventory can be **damaged or outdated** in the warehouse → wastage → adds to carbon footprint.

### 14.5 Green Design and Manufacturing
- Product design should be **eco-friendly**; minimize byproducts during manufacturing.
- Design for **easy repair** and **extended life** by replacing small components.
- **AC example:** **inverter technology** = more energy-efficient; using **aluminum winding / copper winding**; a **5-star** AC is more energy-efficient than a **3-star** one → reduces carbon footprint.

### 14.6 Definition and Scope of Green Logistics
- **Definition:** the practice of managing the **flow of goods and resources** in a manner that **minimizes the environmental impact**.
- Minimizing is not only about alternate fuel with less CO₂ — doing something right the **first time** avoids producing extra waste; producing **quality products** extends life and reduces service/change-over/replacement needs.
- Three major logistics functions covered: **transportation, warehousing, distribution**.
- Activities: **alternative fuels, optimizing transportation routes** (shortening a route by **10 km** saves that much energy), **energy-efficient vehicles** (very old vehicles consume more fuel), **reduce packaging** (multiple layers — plastic packaging, main carton, outer carton, then the e-commerce player's own packet/labeling — increase weight, size, and resources).

### 14.7 Green Logistics vs. Green Supply Chain
- **Green supply chain** — the entire process from raw-material suppliers to end customer, including manufacturers and the whole retail/distribution chain; all stakeholders made efficient, minimum wastage, renewable energy sources.
- **Green logistics** — focused specifically on **transportation, distribution, warehousing**.
  - **Green logistics activities:** routes to minimize fuel consumption; use **TMS/vehicle routing** software for minimum distance considering road condition/traffic (like **GPS** giving options); alternate fuels; efficient warehouse management (full capacity utilization); **sustainable/recyclable packaging**.
  - **Green supply chain activities:** sustainable sourcing, energy-efficient manufacturing, waste reduction, recycling initiatives, environment-friendly packaging.
- **Objective (green logistics):** minimize environmental impact throughout the supply chain but reduce **greenhouse gas emission, energy usage, and resource consumption** in the three areas (transportation, distribution, warehousing).

### 14.8 Waste-Collection Routing Example
- If a city has **more than 500 dustbins**, you cannot touch all daily. Travel **more frequently** (twice/thrice a day) to high-population/shop/industry areas. Ensure a visited dustbin is **near full** (picking a half-full bin wastes efficiency). Decide: "today I pick these **150 dustbins**" and design the **route to minimize distance** while addressing all points. Minimum distance + maximum locations + less fuel = low emission.
- **Sensor idea:** employ sensors to know the **level of the dustbin** and pick only when full; use software/operation-research optimization to find the optimal route.

### 14.9 Key Challenges for Implementing Green Logistics
1. **Raw material cost is increasing** — pushing suppliers to provide greener raw material cannot happen overnight; the grade/grading cannot change suddenly.
2. **COVID-19** — sourcing raw material was a big challenge (shutdown, manpower shortage, price hikes); such disruptions happen frequently.
3. **Transforming the existing system** — the old system took a decade to stabilize/standardize; making it obsolete for a green network is a big challenge.
4. **Technological advancement** — upgrade technology; combine **operation research** concepts for optimization (iterative approach → best optimal solution).
5. **Green transport technologies** — green vehicle routing reduces greenhouse-gas emission, air pollution, noise, and space (e.g., transporting **14–16 items** instead of 10 in the same space).
6. **Logistics solutions for carbon neutrality** — last-mile by electric vehicles/cycles; green packaging; green warehousing; motivate customers to deposit packaging back.
7. **Horizontal collaboration** — pooling resources. **Swiggy example:** the courier going from point A to B covering **15 km** could combine orders from **Zomato, Domino's**, etc. Pooling resources minimizes delivery cost vs. individual delivery networks.
8. **Logistics agglomeration** — consolidate shipments for economies of scale (use the full **10-ton** vehicle capacity instead of 8 tons; combine with others if short).
9. **Carbon management practices** — first **record and report** emissions, then **decarbonize step by step** (e.g., 40% from road transportation, 30% from packaging → address 70%; may hold 30–35% rather than 0).

### 14.10 KPIs for Green Logistics
- **Councils/standards:** **ISO 14000 series** (environmental practices); **United Nations** standards; **Global Logistics Emission Control Council** framework (measures to calculate emissions, set benchmarks).
- **First ensure the reverse supply chain is minimum** (rejections/returns minimize) — even then, ensure **recycling/refurbishment**, with **disposal as the last option** (it directly contributes to carbon footprint).
- **KPIs:**
  - **% of return products successfully recycled** (e.g., 30% → 50% → 70%).
  - **Time taken to process return products** — and **cost per unit** of recycling should be **less than a new product** (since it goes to the secondary market or is price-reduced after repair).
  - **% of raw materials sourced from recycled or renewable sources** (circular economy).
  - **Waste generated** — minimize; byproduct is harmful.
  - **Correlation between environmental and financial performance** — leading to sustainability (with the social dimension). Record **ROI and cost-benefit analysis**; fuel efficiency and route optimization increase financial performance.
  - **% reduction in waste per unit of output; recycling rate; energy efficiency ratio** (energy consumed vs. output).
  - **Overall transportation/vehicle utilization** — pool with competitors/players.

### 14.11 Carbon Footprint Calculation
- **Total carbon footprint** = sum of emissions from **transportation + warehousing + logistics activity**.
- Multiply the **emission factor** by the total material/energy used. **Emission factors:** electricity **0.85**, petrol **2.296**, diesel **2.653** (per unit). Diesel is highest → hence focus on **alternative fuels**; **electric vehicles are most efficient** (minimum emission factor).
- **Life Cycle Assessment (LCA) software** helps calculate energy consumed, environmental depletion, and cost at each stage (e.g., manufacturing one **water bottle** from raw material to end consumption, then recycling/disposal).
- **Harmonization** of emission calculation is needed because industries have different standards, procedures, and units → standardize to compare emissions and share data for transparency (so customers can choose).

### 14.12 Case Studies
- **DHL:** initiated sustainability practices in **2009**; the **GoGreen campaign** focuses on green/sustainable transportation. Claimed **CO₂ emission reduced by 50%** and **pollution emission reduced by 70%**. Initiated **clean delivery and pick-up** using **electric vehicles/bicycles**; trained suppliers (raw-material providers) and included customers in the GoGreen campaign to ensure complete waste collection.
- **Myntra (plastic-free packaging):** paper bag (100% recyclable); replaced **plastic bubble wrap** with **shredded secondary used carton boxes**; replaced **plastic cello tape** with **paper tape**; replaced the small polythene bag for the invoice with a **craft-paper pouch**; uses **RFID tags**. Collaborated with **Canopy** (non-profit) for packaging/recycling, and with the **cotton industry** for sustainable cotton farming (cotton instead of plastic bubble wrap). Warehouses moving towards **solar power**.

### 14.13 Future Perspective
- Advance vehicle technologies to minimize emissions; proper routing; use data analytics to compare with the best industry performance (Myntra still does not **recollect** the paper packets — how to do that at minimum cost).
- Scale of access to public transport and quality of roads will improve → minimum transportation time and fuel.
- Battery-operated vehicles are the best option but range is a question → use an **intermodal network** (sometimes diesel/petrol, sometimes ship, sometimes cycles/electric cycles).
- Research: add **methane** and other ingredients to improve fuel efficiency; **hybrid engines** in 4-wheelers store kinetic energy to charge batteries (significantly increased mileage).
- Tap suppliers and customers, train them, ensure complete collection → green and sustainable logistics throughout distribution, warehousing, and transportation.

---

## Lecture 15 — Lean Logistics

### 15.1 Basic Concept — Minimize Waste
- Lean logistics **minimizes waste** and **streamlines the flow of material**.
- Instead of storing inventory in a storage room, when you need **10 pieces**, 10 pieces come onto the production line, are processed one by one, and output emerges — avoiding **inventory, handling cost, damage during storage, and tied-up capital**.
- Any activity (in warehouse, transportation, or manufacturing) that does **not add value** to the end customer is **inefficient**. Example: storing a product for **10 hours** adds no customer value; the customer cares about getting the product, not how much inventory you keep — **same with packaging**: if the product is safe and quality standards are met, the customer hardly cares about single/double/multi-layer packaging.

### 15.2 Definitions
- Lean logistics focuses on **eliminating waste, improving efficiency, streamlining processes, creating constant flow, enhancing collaboration, and achieving quality**; collaboration among all stakeholders is essential.
- Another definition: **recognize and eliminate wasteful activities** from the supply chain to **increase product flow and speed**.

### 15.3 Container Capacity Example
- Using software/technology, ensure **full utilization of container capacity** and smooth movement of **pallets**; in a well-arranged lift system, one full container is loaded in **less than 2 minutes** (vs. many hours manually).
- Opportunity inside pallet boxes: reduce packaging, make it compact to save space. Instead of shipping **1,000 items**, ship **1,050** in the same container → **per-unit cost comes down**.
- Lean benefits: improved efficiency, reduced cost, faster customer delivery, higher margin (keep some as profit, share some with customers), increased overall profitability, and a more **agile, responsive, efficient** supply chain.

### 15.4 History
- The term **lean** was coined by **John Krafcik** in his **master's thesis in 1988** (implementing lean in manufacturing, warehousing, shipping, and other functions) — but only as a **theoretical concept** with instructions/steps.
- Lean manufacturing was **properly** used by **Toyota** — engineer **Taiichi Ohno** — well known for setting up new quality standards and lean manufacturing; eliminating waste, enhancing product safety, and improving the bottom line.

### 15.5 The Three M's (Japanese)
1. **Muda (waste)** — e.g., overflow of water; total capacity vs. utilized capacity (a room for **100 people** with AC cooling for 100 but only **10 sitting** → unutilized capacity/waste). Rest of the capacity is waste.
2. **Muri (overburden)** — the person takes more than his capacity.
3. **Mura (unevenness)** — not balanced/uneven.

### 15.6 The 7 Types of Waste (Muda) — "TIMWOOD"
1. **Transportation** — unnecessary movement during transportation is waste.
2. **Inventory** — raw material, WIP, finished goods held beyond need = complete waste (customer derives no value).
3. **Motion** — a worker moving zigzag between bins/workstations wastes time (poorly designed workstation).
4. **Waiting** — two workers at stages 1 and 2; while one processes (2 min), the other waits idle. In distribution, a **Zomato courier waiting outside the restaurant for 10–15 min** while food is prepared is waste — reduce it by keeping **half-cooked items** ready and using quick information sharing.
5. **Over-production** — producing something extra not required = waste. **Example:** producing more t-shirts when a customer can wear only **one t-shirt at a time**.
6. **Over-processing** — treating something at **150°C** when only **100°C** is needed; **baking bread at more than the required temperature** damages the product and wastes energy.
7. **Defects** — anything defective passing through the line is waste. Even if you say "we will repair/replace," as a customer paying for a new product I should not get a repaired one.
- Additional wastes: **unutilized talent** (talent is a resource); leaving the recording room with **AC and lights still on** (use sensor-based lights/AC); **byproducts**; idle worker drawing salary without being aligned to the organization's goal (a problem of **role/responsibility design**).

### 15.7 Applying Muda to Inventory, Warehousing, and Transport
- **Inventory** — minimize to meet demand only (JIT); avoid excess.
- **Warehousing** — full capacity utilization, minimum handling, proper **stock rotation** (no obsolete/expired stock), renewable/sustainable energy for lighting.
- **Trucks** — full capacity during routing; minimum distance; travel time is waste (this is why the professor records lectures and holds interactive sessions remotely instead of travelling to address audiences).
- **People waiting for their turn** and **unused skills of manpower** are waste.
- **Electric vehicles** help develop sustainable transportation solutions.

### 15.8 Muri (Overburden) — Causes
- Reasons for overburden: worked too much after not working earlier; fluctuating demand (a **barber** with no customer for 2 hours then 10 customers in 10 minutes).
- Examples that cause overburden: processes you are **not trained for**; **poorly laid-out workplace**; **unclear instructions**; **lack of proper tools/equipment**; **fluctuating demand (mura)**; **lack of proper maintenance**; **unreliable processes**; **poor communication**; wrong prediction of seasonal demand → extra/double shifts → **wear and tear and burnout**.
- In services these cannot be avoided; overburden leads to breakdowns and increased absenteeism.

### 15.9 Mura (Unevenness)
- Inconsistency — not working at all for a while, then working morning-to-evening for two days.
- Smooth out the production process; overburden makes you process quickly → **defective items/damaged products** → quality compromised.
- **Assignment example:** given 4 weeks to submit: week 1 just think about it; week 2 calculate days left; week 3 start the introduction; last week target **70–80%**. This **hockey-stick graph** is human tendency and applies to all stakeholders (raw-material suppliers behave the same way → raw material shortage in the last week). Hence **smooth out production**.

### 15.10 Principles of Lean Logistics
1. **Eliminate waste** (basic principle) — if you don't know how an activity adds value, it is waste.
2. **Improve efficiency** — eliminating waste reduces cycle time (e.g., minimum inventory/cross-docking saves warehousing time); one step relates to the next (improve suppliers → manufacturing smooth → distribution streamlined).
3. **Streamline processes** — remove unnecessary steps; improve **visibility** (analyze what everyone on the workstations is doing; cannot have one heavily loaded and another idle).
4. **Create constant flow** — all stages should have almost equal work; starts with the supplier → smooth manufacturing → smooth distribution → on-time delivery to the end customer.
5. **Enhance collaboration** — lean cannot be implemented within one organization/manufacturing unit alone.
6. **Achieving quality** — storing a product for **two months** vs. **ten days** degrades quality; moving it around to manage space damages quality. Ship quickly to generate revenue and maintain quality.

### 15.11 Performance Metrics for Lean Logistics
- **On-time delivery**; **lead time** (shorter = streamlined process); **inventory turnover** (minimum inventory = quick stock replacement).
- **Order accuracy** — accurate order at accurate time with accurate quality (a **complete order**).
- **Transaction cost per unit** — carrying **10 items** at cost ₹100 → ₹10/unit; carrying **20 items** → cost maybe ₹5–7/unit (ensure full capacity utilization).
- **Warehouse utilization** (space used); **cycle time** (start to end for any activity); **dock-to-stock time** (receiving stock to shelf-ready-for-sale).
- **Return rate** (high = not meeting expectation/defects → question on manufacturing, packaging, handling); **order fulfillment cycle**; **perfect order rate** (on-time + complete + intact product with quality); **back order rate** (demand not met due to insufficient inventory → deliver in a few hours/days later).
- **Supplier on-time delivery performance** (record it; give maximum orders to the 90–95% on-time supplier); **order lead time variability** (inconsistency = unreliable; if consistently late by a fixed margin, you can plan for it, but random 3–10 days cannot be planned).
- **Shipment damage rate during distribution**; **sustainability metrics** (carbon emission, energy, waste as byproduct).
- **Employee engagement and training** — motivated employees work properly.

### 15.12 Conclusion
- Concepts of lean logistics and the types of waste addressed; next session covers the **methodologies/frameworks** to overcome these wastes.

---

## Lecture 16 — Lean Logistics (Contd.)

### 16.1 Methodology 1 — Value Stream Mapping
- **Trace and map the whole process**, then identify all activities that **do not add value**; only after identifying them can waste and inefficiency be eliminated.
- Extra time means extra resources (manpower, energy, equipment) — **reducing even 2–3 seconds** adds up in the big picture.
- **Car industry example:** if a car comes out every **3–3.5 minutes**, saving **2–3 seconds** → after producing **100 cars**, you get **one extra car**. Small products coming continuously out of packaging: save even **microseconds** → increase overall efficiency.

### 16.2 Methodology 2 — Just-in-Time (JIT)
- Inventory was one of the 7 wastes. Maintain only a **minimum stock** to avoid stock-out; avoid excess inventory (no value addition, consumes resources, handling damages it, extra cost).
- JIT: when a product is required, ship directly from **raw-material suppliers to the production line** and from production to the customer.

### 16.3 Methodology 3 — Standardized Work Procedures
- When setting up a **new production line** for a new model, initially there is more **process rejection** because the process isn't standardized/streamlined, workers aren't trained, equipment isn't set, and the raw material/design parameters may change after the initial run.
- Goal: reach **standardization** — eliminates (reduces) **process variability**, reduces errors, improves efficiency.

### 16.4 Methodology 4 — Continuous Improvement Culture (Kaizen)
- Not a one-time fix — every day there is a new opportunity; product design can improve after **2–3 years**.
- **Product recalls example:** **Volkswagen, Maruti's Desire and Baleno, BMW**, and **Nokia** (battery issues). After commercialization, customers use products roughly, revealing new issues → may need to change raw material, design, technology, or train manpower. Every stakeholder/unit element has a role in improvement.

### 16.5 Methodology 5 — Supplier Collaboration
- For JIT and total quality management, suppliers play an important role. Share **demand forecast** and **production schedules**; the downstream team interacting with customers analyzes demand patterns — this information must be passed **immediately, without manipulation**, throughout the network.

### 16.6 Methodology 6 — DMAIC (Lean Six Sigma)
- **Six sigma** allows only **3.4 defects per million** opportunities; **DMAIC** is the methodology to implement six sigma and reduce errors/rejection.
- **Two types of rejection:**
  - **Zero-hour rejection** — responsibility of the **raw-material supplier** (material is wrong before you even use it on the line; no issue with your manufacturing unit).
  - **Process rejection** — responsibility of the **manufacturing unit** while converting raw material into finished goods (faulty technology, faulty method, untrained worker).
- **Calculation:** if 100 components make 50 products and 10 are damaged → only **45 finished products** → rejection rate. Target: **less than 2%** (some organizations **less than 0.5–1%**); anywhere between **2–3%** is considered fair enough but depends on industry.
- **100 AC example:** if every 100 ACs manufactured, **2–3 are defective**, imagine those defective ACs reaching the market → bad brand image in the long run.

### 16.7 Methodology 7 — Technology Integration
- **Transportation:** route optimization (reduce distance, pick better route considering environment/accidents/road condition/traffic) via **transportation management software** → less fuel → lower cost.
- **Warehouse:** full capacity utilization; if a part is vacant, go for **consolidation/horizontal integration** (store a competitor's product in your cold storage if required); **warehouse management software** ensures proper **stock rotation** so nothing goes outdated/expired; quickly identify and ship items.
- **Distribution network:** consolidate shipments (instead of 10 deliveries in a pin code, manage with 2 shipments).

### 16.8 Methodology 8 — Sustainable Packaging Practices
- Target **recyclable and biodegradable** packaging with minimum environmental impact; consider the footprint and how it will be recollected.
- **Right size of packaging** — reduce the extra layer for safety so that complete container space is utilized.

### 16.9 Methodology 9 — Other Technology-Based Solutions
- **Performance-based contracts / smart contracts**; continuously **evaluate vendors** (on-time delivery, order accuracy, **inventory accuracy** — records vs. physical; a fully automated warehouse has **no gap**).
- **Demand forecast and planning** — accurate prediction using predictive analytics, sales-team/customer interaction, historical data, market trends, and customer feedback. But emergencies can change demand: **COVID-19** — automobile/other production reduced (shutdown), but medical supplies and **masks, gloves, face shields, goggles, hand sanitizer** demand rose (common man started using them; even 4–5 years later they are still used).

### 16.10 Methodology 10 — Modular Transportation and Intermodal
- Standardize **container size** by considering packet size; fix the **product packaging size** to utilize **100% container capacity**; use **intermodal** transportation to minimize cost and be sustainable.
- Where infrastructure exists, use **ships**; for last-mile use **cycles or electric vehicles**. **Reverse logistics optimization** — make the reverse supply chain equally efficient (resale of unused, recycling, refurbishment) and map performance matrices. **Performance measurement and monitoring** — track KPIs throughout the distribution network to identify bottlenecks (like **kaizen**, small daily improvements; out of 100 opportunities, prioritize the first ten that can address 60–70% of the efficiency problem).

### 16.11 Value Stream Mapping — Details
- Identify **value-adding activities** (logistics — doorstep delivery experience; manufacturing — putting features in; sales team — recording needs; R&D — new features) and **non-value-adding (supporting) activities**.
- **Non-value-adding but required example:** **HR management** — compensation policies, health-care benefits, training & development; a customer doesn't derive direct value if their product is fine, but it is required to **retain employees**. **Auditing example:** as a customer buying a car, you only care that it has **five tyres** — whether your inventory lost/damaged tyres doesn't matter.
- **W. Edwards Deming (quality guru):** "If you do not describe what you are doing as a process, then you do not know what you are doing."
- **Zigzag motion example:** extra motion → extra handling → breakage → extra cost → inefficiency; implementing lean basics gives a **smooth, streamlined flow**.
- **Five steps of value stream mapping:**
  1. **Prepare the problem** — identify current state by analyzing current data.
  2. **Develop the future state** — where we want to be.
  3. **Develop the plan** accordingly.
  4. **Implement the plan**.
  5. **Track/align the plan** with the overall activity.
- **Scope:** define what you want to change (process, manpower, technology). If manpower isn't trained, arrange **training & development** (cannot hire and fire). Set logistics for the event (participants, stakeholders, location, materials, refreshment — this is like a workshop).
- **Gather data:** e.g., on-time delivery failure because the courier partner **did not pick on time** → focus on the **first courier partner** from seller to local warehouse (even if the downstream partner is on time, the initial delay has a **ripple effect**). Identify actual **lead time**, cycle time, defect rate.
- **On-time delivery case:** if total is 5 days, the courier partner gets only **12 hours** to pick from the seller; if it takes **more than 20 hours**, the target/future state is **12 hours** — communicate to the courier partner; change technology if information isn't shared quickly; provide training if required.
- **Worksheet example — wrong product shipped:** reason = wrong order recorded (the Zomato customer placed an order, information wasn't accurately shared with the restaurant, and the wrong item was communicated to the kitchen). **Action:** can we replace human intervention by having the order go directly from Zomato to the kitchen through the network? **Responsible:** technology/R&D people who develop the platform. Set a **due date**, implement, and record performance matrices.
- **Stapler example:** pick up paper (**1 s**), walk to stapler (**5 s**), staple (**2 s**), walk back to desk (**5 s**), put down paper (**1 s**) → **total 14 s**, **distance 40 feet**. **Value-added time** = pick up + staple + put down = only **4 s**. So **10 s are waste**, and no distance was required if the stapler/pen were on the desk. Value-added time was only **28%**; the other **72% was waste**.

### 16.12 Conclusion
- Continued discussion on methodologies to implement lean logistics; next session = **Toyota Production System** case study.

---

## Lecture 17 — Lean Logistics (Contd.)

### 17.1 DMAIC Approach (Detailed)
- Used to implement **six sigma** — reduce defects to only **3.4 per million opportunities**.
- **Define** — define scope, goal, and financial performance targets (e.g., improve order recording; customer information is missing so exact service cannot be provided).
- **Measure** — current state of performance (how many wrong orders recorded) and the reasons; identify the root cause; understand the complete cycle — customer → **Zomato** → restaurant → courier partner → customer. Information should be shared with Zomato, restaurant, and courier partner.
- **Analyze** — better visibility and traceability throughout the distribution network. **Restaurant/Zomato example:** if the customer says "make it **less spicy**," that information is important for the restaurant; if the customer places an order but does not want delivery within 30 minutes (will be free late from office, so deliver after **1 hour 30 minutes**), that information is important for the courier partner so they can use the time for other orders.
- **Improve** — design the process/platform better so all stakeholders are included; change the recipe if needed; include the KPIs.
- **Control** — track performance indicators vs. actual output; check for deviation; if deviation, change the process; review performance again and again.

### 17.2 Just-in-Time (Detailed)
- Goal: get rid of managing/storing inventory (damage, expiry). Raw material comes directly to the production line, is streamlined with production, packaging done, moved to the final dispatch center for shipping to markets.
- Benefits: eliminates inventory waste and **improves quality** — fresh raw material is better than **electronic components left for 100 days/3–4 months**.
- Requires **close coordination with suppliers**. **Eight steps:** design the process so raw material feeds directly to production lines; manage overall quality (quality of product, work life, equipment, production floor, all stakeholders); use **Kanban production cards** to pull (break the order into small parts, assign responsibilities to vendors); **establish strong vendor relationships**; **fine-tune inventory** (very fine forecasting, predictive analytics, observe buying behavior/patterns, consider disruptions like **strikes, floods, natural disasters**); develop skills/capabilities in-house and with stakeholders; **refine the product and processes** (avoid one process taking too long while another waits — remove process bottlenecks); analyze KPIs (how efficiently orders are delivered/recorded, inventory/handling/damage/obsolete costs).
- **Vendor proximity:** develop **one or two big vendors near the manufacturing house** so they can be fed large orders and they are happy to set up production units nearby to directly feed the line.
- **Strong order channel:** cannot have data processed through district → state → regional → national levels; the customer-entered feedback must be shared quickly throughout the network.

### 17.3 5S Approach (Lean Context)
- Japanese concept for a **sorted, clean, standardized, efficient, safe** workstation; reduces accident rates.
- **Sort** — know where the key, allen key, plucker, hammer (of various sizes) are; if you keep searching for equipment, that is wastage of time. Service stations arrange tools so they can be identified easily. In a manufacturing facility with **thousands of people** doing repetitive actions (**50,000 products/day** = one person repeats an activity ~**50,000 times**), you cannot spend time searching. The same applies to raw/supply material — automated warehouses help locate products by scanning codes; robots can pick and drive them to the line.
- **Shine** (cleanliness), **Standardize/Sustain** — standardization is something to achieve ASAP so the process moves toward productivity, efficiency, lower cost, better margins, reduced (process) rejection, and a sustained environment of **continuous improvement**.

### 17.4 Kaizen
- **Kaizen** = **change for improvement** — **small-step improvements**. Plan → do → study effects → continue if positive.
- Focus is on **continual improvement**, not continuous: achieve a **2% improvement**, **stabilize** it, then go for another **1%**, stabilize, then another **2%**, stabilize. In **continuous** improvement, if you fail at any point you fall to 0 and must abort the whole mission (investment wasted). In **continual**, if you fail, you are still at the previously stabilized level.
- "Make it better, make it faster, make it cheaper" — small investments and small efforts from employees → a **safe approach**.
- **Examples:** earlier lubricating a gearbox with oil was difficult; now a small design change makes it easy. Earlier the belt was covered so inspection was difficult; a small design change makes it quick. **F1 race example:** all **4 tyres** replaced in **5 seconds**; normally replacing one tyre takes **30 minutes**.
- **SMED (Single-Minute Exchange of Die):** change-over should be done in **less than 10 minutes (single-digit minutes)**. **Restaurant example:** a non-veg order followed by a veg order — clean and change the recipe/ingredients; or use separate veg/non-veg workstations (if enough orders justify it; otherwise change over quickly on a single oven).
- **SMED benchmarks:** **Toyota bolt maker — 8 hours → 58 seconds**; **Mitsubishi — 24 hours → 22.7 minutes**; **Hitachi die-cast — 75 min → 3 min**; **HP IC insert — 30 min → 3 min**.

### 17.5 Challenges in Implementing Lean
1. **Culture resistance** — people are happy with the current situation; "I have been doing this for 30 years" → resist change (basic human nature). (Humans will be replaced by machines/robots, which do not resist.)
2. **Lack of leadership commitment** — initial resource investment is required; committed leadership needed; communication barriers; fear of failure (not recovering the initial investment).
3. **Limited employee engagement** — **90% of kaizen suggestions come from production-line workers** (often illiterate or IT-course holders). If we don't engage them/make them comfortable, we lose their input. A worker repeating an activity **50,000 times a day** has unmatched expertise/proficiency — train them, make them capable of thinking, make them fearless ("if we fail we fail together; if we rise we rise together").
4. **Measurement and accountability** — track suggestions; even if some go the other way, cannot stop the thinking/continuous improvement process.
5. **External factors** — technological position changes, political scenario changes, global scenario (war between **Ukraine and Russia** → crude oil price goes up → affects almost **every industry**, not only transportation). How **resilient** is your supply chain; how you tap the opportunity.

### 17.6 Lean vs. Agile Logistics
| Aspect | Lean | Agile |
|---|---|---|
| Focus | Reduce waste → be **efficient** | Be **flexible** |
| Customer demand | Long-term stability/standardized work | Dynamic environment; e.g., 10-minute delivery → "send a private jet" |
| Cost | Cost-efficient (constraint; like **Maruti** mileage) | Not cost-focused (like **BMW/Mercedes/Volvo** — safety, comfort) |
| Product | Uniform standardized work | Customer is **part of the production process** (wants to contribute; e.g., ice cream — one or a thousand, flexible network) |
| Target | Long-term productivity | Flexible enough to give 1 or 1,000 ice creams |

### 17.7 Toyota Production System (TPS) — Case Study
- Based on lean logistics concepts; many concepts came earlier from their **spinning and weaving industry**. Founders/contributors: **Taiichi Ohno** and **Shigeo Shingo**. They positioned their organization as a **"poor organization that cannot afford to produce waste."**
- **Seven principles of TPS:**
  1. **Setup time should be minimum.**
  2. **Small lot production** — if something goes wrong, only that lot is spoiled (a big lot spoils everything).
  3. **Employee involvement/empowerment** — suggestion box, rewards for good suggestions.
  4. **Quality at source** — equip and train raw-material suppliers (they are the **extended hands**); cutting cost at the initial stage cuts cost throughout.
  5. **Equipment maintenance** — **predictive maintenance** (before something goes wrong).
  6. **Pull production system** — let the order come, then provide to the customer.
  7. **Supplier involvement.**
- **The "House" of TPS:** the **roof/target** = **highest quality, lowest cost, shortest lead time**, achieved by eliminating all waste. **Foundation** = **heijunka, standard work, total productive maintenance, value chain**. **Pillars** = **Just-in-Time** and **Jidoka**. Environment = **continuous improvement**.
- **Continuous flow of material / Heijunka:** ensure evenness (avoid mura/muri/muda). Example: if **20 products** are required, exactly **20 wooden sticks and 20 iron hammers** come — no extra inventory. (Having 50 hammers against a need of 20 mismatches inventory.)
- **Batch vs. continuous flow (first-product time):**
  - **Batch process:** 3 steps, each **10 minutes**; the whole batch passes to the next stage → minimum **21 minutes** to produce the first product (10 + 10, then first minute of stage 3).
  - **Continuous flow:** each stage takes **1 minute** per piece → first product ready in **3 minutes**.
- **Just-in-Time history:** **Kiichiro Toyoda** in **1937** — "we are a poor company, we cannot afford waste"; collaborate with raw-material suppliers so material ships to production lines when required. After WWII, **Taiichi Ohno** (from spinning/weaving) implemented JIT and Jidoka, then was transferred to the automobile industry to improve quality.
- **Jidoka (autonomation):** in the **spinning/weaving industry**, many threads (24, 40–64, 98) make quality cloth. If one thread **breaks**, a line appears in the cloth. Ohno's idea: if a thread breaks at that point, the **machine stops automatically**. Without this, a **100-metre cloth** with a break after **20 metres** wastes the remaining **80 metres**.
- **Poka-Yoke (mistake-proofing):** even if you want to make a mistake intentionally, you cannot. **CPU/computer example:** plugging in keyboard, mouse, CPU, UPS, screen, pen drive, power/data cables — jacks are designed so only the **power cable fits the power plug** and only the **data cable fits the data point**.
- **Andon system:** an indication board — **red light** if there is a problem (e.g., at stage 3 of 100), **yellow** for warning, **green** for fine. If something goes wrong, the whole production system stops.
- **Gemba / Genchi Genbutsu:** "go and see" — visit the defect stage, observe, and ask the **5 Whys** to find the root cause; identify muda/muri/mura; do it as a **team** (respectful togetherness); include the stakeholders working at that stage.
- **Heijunka:** smooth the production process. Example: if stage 1 takes **5 seconds**, design the next stage to also take ~**5 seconds**; if it takes **7–8 seconds**, semi-finished inventory piles up at that stage. Heijunka is the **base of TPS**.
- **Kaizen:** small steps, "everybody, every day, everywhere" — with the process, equipment, and the person.
- **Standardization and Takt time:** **Takt time** = production time available / market demand — how quickly you produce to meet demand. **Working sequence** — sequential, one piece at a time. **Standard in-process stock** — the inventory required to ensure minimum takt time and work sequence (first stage should not wait for raw material). Standardization is critical for Jidoka and JIT.
- **Performance improvement:**
  - **80% increase in per-head production:** earlier **39.7 vehicles per person** → after TPS (late 1980s) ~**71 vehicles per person**.
  - **US market share (car and light trucks):** GM initially **40%**, Toyota only **2%**. After TPS: Toyota improved to **3%** (80s), **8%** (90s), **9%** (2000), **more than 10%** (2006), then **13%**; GM fell to **26%**.
- **Conclusion:** small-step improvements led to big overall improvement.

---

## Lecture 18 — Trends in Logistics

### 18.1 History After WWII
- After World War II, many countries realized they had **enough resources** but **lagged in optimal utilization** and **coordination** among supply-chain stakeholders; **technological integration** was not at that level. These failures/drawbacks were investigated, especially in the **military context**.
- Then they shifted towards **computing capability**: mathematical modeling and software — **warehouse management software, transportation management software**; tracking unutilized capacity to design packaging/complete ship load.
- **Operation Research algorithms:** **assignment problem** (which market supplied from which factory), **transportation algorithm** (best route considering distance, road condition, weather → minimize cost), **queuing theory**, and the **simplex method** — to remove subjectivity and make objective decisions.
- Realization: logistics is a separate area requiring special attention — **50–60% of cost** (60–70% including raw material sourcing, manufacturing, transportation, distribution, warehousing, order management, doorstep delivery). So, outsource to a professional agency — **third-party logistics** (and the evolution towards **6PL**).
- **Modern logistics stalwarts:** UPS, FedEx, Walmart, Flipkart, Amazon, eBay, Ekart.

### 18.2 Modern-Day Logistics Categories and Industries
- Need a **multifaceted approach** for consumption, production, and distribution of goods, within or outside the city — wide coverage network with variations in city size, geography, economy, culture, politics; political instability, natural disasters, economic fluctuations → the logistics network is **diverse and complex**.
- **Retail** — fragmented stores or one-stop-solution markets; understand what items/how many/quality level/delivery patterns (small lots vs. big lots) to design the next-stage logistics network.
- **Consumer shopping trips** — visiting a mall with family, addressing all demand at one place; stores promise "**pick the stock, we deliver to your doorstep**" (prominent for grocery). Courier services like **Delhivery, Ekart, UPS** handle these stocks, sometimes doing cross-docking.
- **Hotel/restaurant/catering (HORECA)** — **Zomato, Swiggy**; exclusive outlets (**Domino's Pizza, McDonald's**) promising delivery within **30 minutes**, either via local partners or their own distribution. People have limited time, so **hotels come to your doorstep**.
- **Construction** — easy in rural/semi-urban areas; in the **city** there are logistics problems (where to store material; not enough area) → need **temporary storage centers** or a third party storing construction raw material; JIT-type services in urban areas avoiding traffic/restrictions.
- **Waste management / circular economy / closed-loop supply chain** (the professor's own research area): collection from households → **segregation** (wet vs. dry; infectious vs. non-infectious) → transport to waste-treatment facilities, with warehouses for temporary storage → composting plant, recycling (plastic), road metalling, etc. Industries reusing used products are reportedly **5 times more profitable** than making fresh raw material.
- **Industrial and terminal haulage** — distribution centers/hubs in cities temporarily storing industrial products/supplies.

### 18.3 Stakeholders in Modern Logistics
- **Shippers (who ship)** and **receivers (who receive)** are the two prominent players.
- Shipper demands are driven by the customer: **lead time, cycle time, quantity, frequency, delivery options** (e.g., evening hours, 2–3 pm), **quality**, and **after-sales services** — all at **minimum cost** (Amazon/Flipkart customers first check whether **free returns** are available and how easily a product can be returned; then **payment options** — how quickly money returns to the wallet/account).
- **Carrier** — takes the product from manufacturer to doorstep. Old-school thought: who cares how the packet is handled. Now customers want to see **where the packet is dropped/picked** and how it is handled throughout the distribution network.
- **Public authorities** — ensure the **infrastructure** (ship, air, rail, road); handle operations (consumer code if payment made but product not received); packaging/sustainability norms.

### 18.4 Logistics 1.0 to 4.0 Evolution
- **Steam engine era** — local distribution, animal force.
- **Electrical power** — automation of handling systems, electrical engines, quicker/efficient delivery.
- **Computers/IT** — **WMS, TMS** for best route, minimum distance/cost/inventory (not manual).
- **IoT systems, RFID tagging, cyber-physical systems** — connectivity, transparency; customers have visibility of where their product is and how long it will take; service providers get information for **more informed decisions**.
- Basic drivers: **automation, sustainability, technology.**

### 18.5 Modern Logistics Technologies
1. **Elastic logistics** — use 3PL so you pay for actual volume (10 packets today, 100 tomorrow — the courier partner's headache to arrange manpower/vehicles).
2. **Automation** — software, minimum human intervention; robots manage inventory/replenishment; **DHL** video shown of automated warehouse/drones.
3. **Blockchain** — a parallel digital system giving a complete, transparent, **error-proof, tamper-proof** picture from first supplier to end customer; fraud cannot happen.
4. **Smart contracts** — **IQC example:** raw material comes to the shop floor and goes for **incoming quality control**; if accepted, it is stored and information goes to accounts to raise a **credit note** to the vendor. With a smart contract, as soon as IQC clicks "lot OK," the contract executes and **payment is made automatically** (no human intervention/documentation delay).
5. **IoT, cloud computing** — share resources; software analyzes inventory and places orders automatically.
6. **Advanced/predictive analytics** — predict demand and disruptions.
7. **Big data** — large data generated from customer, distribution partner, shipping agency, manufacturer, warehouse partner, raw-material supplier.
8. **Logistics robots** — manage inventory in warehouses.
9. **AI-enabled solutions** — with IoT/cloud, decide when to ship, when to pack, quantity, which pin code, when to reorder raw material, when to start the cycle time of a model.
10. **AR (Augmented Reality)** — in a huge warehouse (say **10 km²**), find the shortest route to a product; a robot/drone picks and drops it at the packaging stage.
11. **GPS/Bluetooth/Wi-Fi/cellular/IoT-enabled tracking.**
12. **Digital twin** — replicate the practical scenario in the lab to test how resilient the supply chain is.
- **Smart trolley example:** in multi-brand stores, as you pick/drop products in the trolley, the **bill is generated automatically** and shows the **Amazon-style rating** of the product — reducing weekend queue time.

### 18.6 Modern Logistics Concepts (Detailed)
- **Drones** — last-mile delivery; within a warehouse, connect shelves via Wi-Fi so drones/robots find and deliver items (e.g., 5 items from a shelf); track even inventory traveling in trucks.
- **Cold chain logistics** — maintain temperature throughout for perishables (vegetables, milk products) and medicines/vaccines (temperature affects **potency**). Components: **temperature control** (including the **cold corridor** during container transfer/unloading), **insulated packaging** (prone to outside temperature variation), **monitoring and tracking** (contingency if there is fluctuation/failure), **regulatory compliance** (food/medicine guidelines).
- **Blockchain (detail)** — tamper-proof records using **cryptographic encryption** and a **decentralized consensus mechanism**. Documents at each handoff (loading certificate, batch number, processing data, shipment, delivery, packing list, order number). Example: if the factory needs to know whether a warehouse maintained proper temperature (else quality at the end customer fails), it can only know with transparency throughout. Blockchain gives visibility → informed decisions.
- **Smart contracts (detail)** — payment executes at each executed stage without human verification; instead of opening every box to count 20 items, check the **box weight** (average weight range indicates the count).
- **Big data analytics** — track patterns, trends, correlations (weekend visits), stakeholder performance matrices, competitor renovation, disruption sources; demand forecasting via customer behavior → more supply chain visibility and collaboration → better risk management (e.g., heavy rain for 3 days → mitigate).

### 18.7 Conclusion
- Modern logistics concepts and technologies; continued in the next session.

---

## Lecture 19 — Trends in Logistics (Contd.)

### 19.1 Factors Forcing Innovation in Distribution/Logistics Networks
1. **Supply chain agility** — the environment is very dynamic/fragile; sticking to legacy won't work. If you don't change, your **competitor will** — providing the same product at lesser cost and adding **experience** to the basket, taking away market share.
   - **Self-managed vs. outsourced example (Tata Sky):** compare new installation/new connection vs. an existing connection not working. When outsourced to a third person, tokens are generated "who came first is processed first" — the **new client** does not get the special attention required. **Jio example:** message Jio on WhatsApp to port a connection — within **20 minutes** they come home, process documents/take a picture within **2 minutes**, and ensure it is done within **2 days**. But **Jio Fiber** (old customer) gets less immediate attention — part of the strategy: give a welcoming note to the **new client**.
2. **Global labor shortage** — 3PL needs special skills (proper packaging/handling); trained people leave. This **forces automation** (remove human intervention), but some human intervention remains — now skills are at a different level (operate automated warehouses/software, digital tracking). Earlier **100 manpower**, now maybe **10** required. **Driverless trucks:** first truck is manually operated; the **second truck mimics the first**, tracks the pattern, and takes decisions on the road.
3. **Complexity generated through automation** — different software platforms: supplier negotiation/quality/quantity/vendor assignment; transportation/intermodal (best route/mode/container size); manufacturing inventory track; warehouse management in the distribution center. Moving from one platform to another makes it hard to get the final decision-driving information — need one **integrated platform** giving one option, passed to every player.
4. **Delivery promises (2-day, same-day, 30-minute)** — affecting customer expectations; achievable only with updated software to track the product, estimate time, and provide alternatives (source from another vendor ready with final delivery). **Warehouse management/ERP platforms** create visibility; projects like **project44, FourKites** track every shipment/return activity and share refund status with customers.
5. **Supply chain transparency and collaboration mandate** — now **mandatory** for every player to be integrated through the network, via **EDI (Electronic Data Interchange)** or **APIs (application programming interfaces)**, to avoid the **bullwhip effect**.
   - **Bullwhip effect example:** order required at the retailer is **10 units** → must not become **15** at the distributor, **20** at the wholesaler, **25** at the manufacturer, **35** at the raw-material supplier. The exact **10** should pass to the raw-material supplier.
6. **Less-than-truck-load (LTL)** — small players cannot fill a container. Consolidate orders from other players in the same/other industry → pay only for the capacity used. Useful for **e-commerce** (major cities generate enough demand to exhaust capacity; urban/rural/semi-urban areas may use less than available capacity). **Small businesses** benefit by collaborating to reduce transportation cost. **Environmental angle:** transporting **50 items** instead of 10 in the same container reduces the **per-unit carbon footprint**.

### 19.2 Persisting with Digital Transformation
- Share electronic records from customer to warehouse to distribution network; if inventory isn't ready, place order immediately with manufacturing and share immediately with the raw-material supplier; the courier partner gets an alert for emergency delivery.
- **API-based integration** — process **real-time** information; not batch processing (process fully then shift to next stage). Even if **one unit** is produced, share it with the next stage.
- **Logistics demand forecasting** — design the demand function using predictive analytics/big data; plan production, storage, and inventories.
  - Factors: **historical data, seasonality** (summer → coolers, water coolers, ACs, refrigerators), **economy** (country/region economic condition), **market trends, pricing, competition, price of complementary goods, price of competitors**. Information is shared throughout the network to the raw-material supplier (so they don't overproduce, avoid obsolete inventory or 50%-off seasonal sales).
- **Digital freight marketplaces** — comparison: shifting household items from **Kharagpur to Calcutta**, you search online packers-and-movers, collect quotations (4–5 days), then packaging/loading (a full-day activity), shipping, unloading, repacking — yet only **6–7 hours** of actual loading/unloading/transporting work, taking a minimum of **3 days**; the container may have to return to base due to union restrictions.
  - **Ola/Uber analogy:** a taxi is available anywhere; log in and within **2 minutes** the nearest one takes the ride. Why can't the freight industry do this? Anyone near a container can use its capacity; drop the container if unloading is delayed, get a new one at the site; automatic containers unload in **2 minutes**.
  - Need to create an **ecosystem** by integrating all internal/external disparate systems; it is unsuccessful if only the distribution partner is digitally strong and others avoid the initial investment (money, training, systems).
- **Technological advancement in India** — the Indian market is not away from these dynamics (whole world is one market). **Fleet management** and capacity utilization improve vehicle performance and reduce fuel. **Driver behavior** can be recorded (rash/wrong driving causes more wear and tear, more fuel, higher accident rates); it also improves the driver's quality of life.
- **Last-mile delivery** — **Flipkart** doing drone delivery in some areas (thickly populated, traffic bottlenecks; fly drones within one kilometer). **Crowdshipping model** — Flipkart, **Ekart, Delhivery, Swiggy** partner with local service providers/courier partners/restaurants.
- **Sustainable practices** — electric vehicles, bicycles; sustainable customer. On the package, mention the **carbon footprint** from raw-material supplier to manufacture, in manufacturing, and for distribution to the doorstep — customers become aware, are more responsible when ordering, and reduce returns.
  - **Amazon** objective: **electrify vehicles 100% by 2030**.
- **Warehouse automation** — **DHL** (prominent player): in **Delhi** an automation sortation center handles **6,000 shipments/hour**; the main warehouse in the **US/China** handles more than **40,000 shipments/hour** (needs that much demand). DHL is initiating this in India too.
- **Predictive analytics/demand forecasting** — **Delhivery** does very well using predictive analytics, big data analytics, cloud computing; tracks forward and backward supply-chain patterns to optimize delivery routes (minimum distance, avoid traffic in populated urban areas).
- **Collaboration and integration** — a **digital freight platform** connects all shippers and truckers (search a **10-ton container** on an app, use the nearest one). Many taxi drivers attach to Ola/Uber — rides increased (from **10 → 100** a day), maybe charging a little less (Ola/Uber take ~**25%** share) but it is a **win-win** (economies of scale). Waiting for the next ride is **muda (waiting waste)**.
- **E-commerce logistics focus** — how quickly to deliver, nature of product, and the return supply chain are equally important. **Ekart** (Flipkart's official partner) — order grocery items in the evening, get them by morning; they are working on generating enough orders to be efficient.

### 19.3 Challenges for Modern-Day Logistics
1. **Supply chain disruptions / unforeseen global events** — **COVID-19** (sudden shutdown); **Russia-Ukraine war** (crude oil supplies → petrol/diesel/natural gas price rise → supply chain cost rise). Need **resilience**: how quickly you find alternatives if a vendor is hit by a natural disaster/flood so the smooth production continues (500 workers should not sit idle).
2. **Trading partners failing to make promises** — a report says **80% of companies** have trading partners failing to make their promises; **27%** of respondents say **11 or more** trading partners fail; many are still looking to set up new business partnerships. Business partnership is a **long-term strategic decision** — the main manufacturer must **train and equip** raw-material suppliers with the latest technology (if they are efficient, you are efficient). This is a big problem in Indian logistics.
3. **Logistics cost** — India goes through ~**60–65% road transportation** → adds **14%** as logistics cost, vs. **7–8%** in developed nations. **32%** of companies said they will invest heavily in **supply chain integration technology**.
4. **Sustainability targets** — manufacturers are moving towards sustainability, but measures change rapidly (government first imposes heavy taxes on plastic packaging, then decides to **phase out** that packaging) — difficult for logistic players to cope.

### 19.4 Performance Measures (Modern Logistics)
- **Efficiency** — order fulfillment cycle time, packaging cycle time, manufacturing cycle time.
- **Resource utilization rate** — how well resources (warehouse, distribution network) are utilized.
- **Cost effectiveness / operation cost** — raw material cost, transportation cost (minimize via routing), manufacturing cost, warehousing cost, last-mile delivery cost, and **returns** (also a cost).
- **Customer satisfaction** — on-time service, hassle-free returns, quick delivery, demanded quality → loyal customers.
- **Flexibility and agility** — how quickly you adapt resources to lower/higher demand.
- **Innovation adoption** — how quickly new technology is implemented, adoption rate, and whether the initial cost is recovered (cannot randomly upgrade technology that doesn't ensure minimum returns).
- **Supply chain visibility** — track the order; the customer also demands this information (when shipped, packed, how packed, out for delivery).

### 19.5 Case Studies
- **DHL** — huge investment to create a **central nervous system** for operations: optimizing resource allocation, automating workflows, dynamically adapting to real-time business changes and customer demands.
- **Amazon** — predictive analytics on **when, where, and which items** are required; check if the item is available in a nearby hub; pick orders near that customer for a short lead time and efficient last-mile delivery.
- **Swiggy** — **hyper-local delivery network**; collaborates with local restaurants and local delivery partners for on-time delivery, fresh food, hygiene, minimum transportation time.
- **Flipkart** — partners with local vendors for efficient delivery; faster delivery, increased coverage, deeper penetration into remote areas (selling local items); enjoys **60–65% share** in the Indian market.

### 19.6 Conclusion
- Three key parameters force the next-age distribution network: **digitalization, innovation, sustainability**. The network must be **informed and agile** — adapt quickly to external disruptions, switch to alternatives **cost-effectively**, and provide **resilience** (tapping disruptions in a better way when you know they are coming). This requires **complete integration of all stakeholders** and an **ecosystem for quick information sharing**. Next: supply chain management.

---

## Lecture 20 — Logistics vs. Supply Chain Management

### 20.1 The Blurred Boundary
- Logistics and supply chain management are often used **interchangeably** by academicians/researchers.
- **Old theory:** first the **logistics** concept came, then it matured and was converted into **supply chain management**, thinking of the whole chain as one functional area with logistics working under it.
- **Regional terminology:** in the **United States**, supply chain management is more commonly known as **logistics management**; in **Europe**, different usage.
- **Wayne and Johnson:** "There is no difference today" — what we did as logistics management earlier, we now do as supply chain management.
- **Another view:** supply chain management **incorporates** the field of logistics; logistics is a **number of sub-processes** within supply chain management (e.g., transportation from supplier to manufacturing = one functional area; outbound transportation from manufacturer to customer = another sub-process).
- **Third-party operator:** a supply chain management company is generally a third-party operator managing the overall movement of the product, whether **inbound or outbound**.

### 20.2 Inbound vs. Outbound Logistics
- **Simple structure:** raw-material suppliers → manufacturer → customer.
- For the manufacturer:
  - **Inbound logistics** — transportation from raw-material supplier to manufacturer; storage between raw-material supplier and manufacturer; **packaging of that raw material**.
  - **Outbound logistics** — the same functions downstream: transportation, distribution, storage in between, to the customer.
- **Logistics includes:** demand planning, inventory management, transportation, fleet management, material handling, and customer order fulfillment.

### 20.3 Traditional vs. Modern Views
- **Traditional view:** logistics is the **broader picture** and supply chain management is a small picture under it (old-school). In the **1980s** it was realized logistics requires special attention (continuous supply of raw material/finished goods, transportation) — if you are not competent in logistics, **outsource**.
- **Modern view:** there is no separate term — replace logistics completely with **supply chain management**; logistics is a **sub-part** of supply chain management.
- **Some still argue** logistics and SCM are separate functional units, but they share **common points** — the common basic objective is the **performance, productivity, efficiency of delivering finished goods from source to customer**.

### 20.4 What Logistics Includes
- The **physical transportation** of the product from one point to another.
- **Warehousing/storage** of the product.
- **Information** transferred in the channel.
- **Value-adding activities** in the warehouse — packaging, kitting, labeling.

### 20.5 What Supply Chain Management Includes (Beyond Logistics)
- **R&D / product innovation and development** — information comes through the logistics network; realize the need for new features due to competitors/customer expectations.
- **Manufacturing** — basic questions: **what** to manufacture, **how much**, **where**, **when**. If multiple models (A, B, C), how much of each is required based on forecasting models.
- **Purchasing and sourcing** — order allocation among vendors (e.g., **60%** to vendor A based on **vendor rating** — quality, pricing, delivery schedules). Also what to **outsource**.
- **Manufacturing and operations** — sourcing sub-assemblies/raw-material components, assembling on the production line, final packaging.
- **Customer service** — doorstep delivery, installation, demonstration, and warranty/guarantee replacements.
- **Global deployment** — in the international market, both outbound logistics to global markets and inbound logistics from global markets.
- **A model of SCM activities:** production, inventory, **labor planning**, material, **facility management** (locating manufacturing facilities and warehouses), manufacturing, delivery of goods and services → drives **competitive advantage**. (Logistics did not discuss converting raw material into finished goods, labor planning, product/process design — these are under SCM.)

### 20.6 Michigan State University Definition
- **Supply chain logistics** involves **collaboration between firms, suppliers, customers, and other partners** to boost **efficiency** and provide **value to the customer**.
- Purpose: deliver quality products with maximum value and highest efficiency → minimize operation/manufacturing/delivery cost → more competitive than competitors → extra margin to share with customers or keep for expansion.

### 20.7 System View (Shared Profit/Loss)
- SCM is a **system view**: from raw material to end customer; if there is a **profit of $10**, it is shared with suppliers, manufacturer, wholesaler, retailer, distributor — **all stakeholders**. Likewise, a **loss is shared** through all.
- **Travel aggregator example (Goibibo, MakeMyTrip, ixigo):** they claim the **cheapest flight/hotel**. If a hotel promises cancellation with refund **in the last hour**, that promise is only possible if the **hotel/property owner** is also ready for it → **complete integration of all stakeholders** is required.

### 20.8 Two-Concept Illustration (Inbound/Outbound and Distance)
- **Furniture example:** ordering heavy furniture via **Amazon/Flipkart** — they prepare the whole furniture, then **dismantle** it, and at the location either **reassemble** it or give easy **self-install instructions**.
- **Distance/efficiency model:** manufacturer with raw-material supplier at **10 km** and customer at **5 km** (Structure 1, inbound distance > outbound) vs. supplier at **5 km** and customer at **10 km** (Structure 2, inbound < outbound).
  - **Structure 1 (outbound distance smaller) is more cost-efficient.** Reason: a container may carry **8–10 cars** (final product), but **10 containers can carry more than 200 cars of raw material** because it is **dismantled** (less space). So, set up manufacturing **near the customer/market** so the final product travels the **minimum distance** (outbound logistics requires more space → costly).

### 20.9 Key Differences
- **Logistics** — physical distribution/transportation; inbound and outbound; transportation, warehousing/packaging, final distribution.
- **Supply chain management** — controls the **development of raw material into finished goods** and their transfer to the end customer (and returns); includes facility management (locating facilities/warehouses), labor planning, product/process design, sourcing, manufacturing, customer service, global deployment.
- **Keith Oliver** — a logistician who also coined the term **supply chain management**; his findings explain how the logistics concept matured and needed additional functional areas.
- **Why logistics is important to supply chain:**
  - New product ideas come from information through the **logistics/distribution network**.
  - Deliver right products at the right time → through the logistics network (smooth raw-material supply → on-time final delivery).
  - Reduce cost and improve efficiency → implementing **lean logistics** (remove non-value-adding activities).
  - Minimize waste → increase customer loyalty (mostly on time).
  - Unique value proposition — new ideas and a means to deliver goods cost-effectively.

### 20.10 Logistics Components of the Supply Chain
- **Information** — status of items (shipped, in warehouse, inventory status).
- **Storage** — ensures you are never stock-out and maintain a minimum level.
- **Warehousing** — value-adding beyond picking/packing/handling: resale of returned products, kitting, labeling.
- **Material handling** — within one facility: store department → production department → production line → outgoing quality control → dispatch area → loading.
- **Packaging** — minimize space/cost without damaging the final product.
- **Transportation** — efficient use of routes, vehicles, warehousing capacity, distribution and last-mile delivery.
- **Inventory control** — plan demand vs. supply; control raw material, finished, and semi-finished inventory.
- **Intermodal transportation** — transportation manager decides, bringing cost into the picture.
- **Role of logistics in SCM:** in **planning** (information from logistics), **inventory control**, **sourcing** (information, material handling, transportation), **manufacturing** (storage, handling, shipping between stages, warehousing utilization, packaging, transportation), **delivering** (information, warehousing, inventory, packaging, transportation), and **returning** (the same logistics functions for end-of-use/damaged/recycled/refurbished products).

### 20.11 Case Study — GeoDis
- A **logistics service provider** addressing challenges of **small online retailers**:
  - Small retailers are **not sure about demand** (sometimes it comes, sometimes not) → setting up a separate channel is a big question.
  - **Seasonal fluctuations** — sometimes increase volume, sometimes reduce supply.
- GeoDis helps them **survive**, maintain **accurate inventory levels** (not stock-out, not excess), and ensure **next-day/two-day delivery** — providing **fast and reliable fulfillment** with **~91% fulfillment accuracy**.
- Small players collaborate with GeoDis for **demand forecasting/planning**, scaling warehouses up/down, and **optimized shipping practices** (routes, container capacity designed as per packaging to minimize cost, delivery times promised to customers).
- From **small outsourced facility and transport** into a **multi-country network** with **91% fulfillment rate** for European customers — reliable and cost-efficient.
- **Taxi analogy:** one individual taxi in the market gets few rides; connecting with **Ola/Uber** increases the utilization rate.

### 20.12 Conclusion
- Logistics is **very much part of supply chain management**; smooth supply chain operations require the three basic logistics functions to work perfectly:
  1. **Transportation** happening on time.
  2. **Storage** — maintaining safety stock so you never tell the customer "we are out of stock."
  3. **Distribution** of the product to the end customer → improving customer experience.
- Many platforms/softwares exist for distribution, sourcing, manufacturing, inventory, warehousing, and transportation — the need is to **integrate all into one platform** to enhance overall customer experience and deliver cost-effectively and efficiently.
- **References:** **Simchi-Levi** (good for further reading), **Wayne and Coyle — Fundamentals of Supply Chain Management**, **Sunil Chopra and Peter Meindl — Supply Chain Management: Strategy, Planning, and Operations**.

---

## Quick-Revision Cheat Sheet

| Lecture | Core Topic | Key Takeaways |
|---|---|---|
| 11 | Tools for Improving Efficiency (Contd.) | 7 QC tools (Ishikawa): flow chart (bottleneck 8 s of 5/6/4/8/6 s), check sheet (feedback form), histogram (restaurant delivery-time bins), Pareto 80-20 (scratched screen/battery/missing components ≈ 80%), fishbone + 5-Why (packaging problem), scatter (compensation vs. productivity), control chart (Shewhart ±3 sigma; common vs. special cause); quality circle (8–10 voluntary members, coordinator/facilitator/leader/steering committee); 5S (seiri, seiton, seiso, seiketsu, shitsuke); benchmarking (6 steps, house of quality, balanced scorecard) |
| 12 | Reverse Logistics | Returns 25–30%; forward vs. reverse (collection → consolidation → sorting → treatment); types (customer returns/destroyed packaging, warranty, end-of-life); modular design (TV sound panel, AC motor/board); Aquaguard AMC (service over product); 3 R's; drivers (Netherlands take-back, Germany packaging ordinance, ACC CSR energy, e-waste, 80% mobiles replaced every 2 years); informal recycling sector |
| 13 | Reverse Logistics (Contd.) | Key aspects + steps: gate keeping → collection → sorting → processing → treatment → disposal; Canon prepaid coupons (24 countries); consolidation/sorting; remanufacture, refurbish, recycle, donate, secondary market; incineration 1000–1200°C (smoke through water; ash fertilizer/burial; microwaving/autoclaving); hybrid engine (Grand Vitara ~30 km/l); factors (visibility, network design, tech, compliance, circular economy); KPIs (return rate, processing time, recovery rate, disposition/transportation/holding cost); Amazon ($761 bn returns 2021; 2M tons packaging avoided; SIP −14 components, −69% volume) and IKEA (full refund, material recovery, durability/repairability/recyclability) |
| 14 | Green Logistics | Reverse vs. green vs. sustainability (env + economic + social); green SC functions (raw material, design, purchasing, production, warehousing, distribution, marketing); CO₂ up 71% in 2016; Delhi Odd-Even, BS4, 15-year trucks; fridge inventory-energy link; inverter AC (aluminum vs. copper, 3/5 star); 500 dustbin routing + sensors; emissions (electricity 0.85, petrol 2.296, diesel 2.653); LCA software; DHL GoGreen (CO₂ −50%, pollution −70%, 2009); Myntra plastic-free (paper tape, shredded cartons, Canopy, cotton, solar) |
| 15 | Lean Logistics | Waste minimization; John Krafcik (1988 thesis); Taiichi Ohno (Toyota); three M's — muda, muri, mura; 7 wastes (TIMWOOD: transport, inventory, motion, waiting, over-production, over-processing, defects); Zomato waiting; t-shirt over-production; bread 100°C vs 150°C; assignment 4-week hockey stick; principles (eliminate waste, efficiency, streamline, constant flow, collaboration, quality); KPIs (on-time delivery, lead time, inventory turnover, perfect order, back order, supplier on-time, damage rate, sustainability) |
| 16 | Lean Logistics (Contd.) | Value stream mapping (100 cars/every 3–3.5 min → save 2–3 s → 1 extra car per 100; stapler 4 s value of 14 s = 28%); JIT; standardized work; kaizen; supplier collaboration; DMAIC/six sigma (3.4 defects/million; zero-hour vs process rejection; 100 AC → 2–3 defective); technology (TMS, WMS, consolidation); sustainable packaging; smart contracts; COVID demand shift (masks/sanitizer); modular container + intermodal; VSM 5 steps; on-time delivery 12 h target; wrong order/R&D platform fix |
| 17 | Lean Logistics (Contd.) | DMAIC detail (define–measure–analyze–improve–control; Zomato less-spicy & late delivery info); JIT 8 steps + nearby big vendors; 5S; kaizen (continual vs continuous; SMED <10 min; Toyota bolt maker 8 h→58 s, Mitsubishi 24 h→22.7 min, Hitachi 75→3 min, HP IC 30→3 min); challenges (culture, leadership, 90% suggestions from shop floor, external factors, Russia-Ukraine oil); lean vs agile (efficiency vs flexibility; Maruti vs BMW/Volvo; ice cream 1 or 1000); TPS (Ohno & Shingo; 7 principles; house — foundation heijunka/standard work/TPM/value chain, pillars JIT & Jidoka; jidoka thread break; poka-yoke CPU cables; andon; gemba/5 Why; takt time; batch first product 21 min vs flow 3 min; 39.7→71 vehicles/person; GM 40%→26%, Toyota 2%→13%) |
| 18 | Trends in Logistics | Post-WWII OR algorithms (assignment, transportation, queuing, simplex); 50–60% SC cost; 1PL→6PL; industries (retail, mall pick-and-deliver, HORECA 30-min, construction, waste management 5× profitability, industrial haulage); stakeholders (shippers, carriers, public authorities); Logistics 1.0→4.0 (steam→electric→IT/WMS/TMS→IoT/RFID/cyber-physical); technologies: elastic logistics, automation, blockchain, smart contracts (IQC auto-payment), IoT, cloud, predictive analytics, big data, robots, AI, AR (10 km² warehouse), digital twin; cold chain (temperature, insulated packaging, monitoring, compliance); smart trolley auto-billing |
| 19 | Trends in Logistics (Contd.) | Factors: agility (Tata Sky new vs old, Jio 20-min port), global labor shortage (driverless trucks mimicking), complexity (multiple platforms → integrate), delivery promises, transparency/collaboration mandate (EDI/API; bullwhip 10→15→20→25→35), LTL consolidation; digital transformation; demand forecasting (seasonality); digital freight marketplaces (Ola/Uber for freight; Kharagpur→Calcutta 6–7 h work vs 3 days); fleet/driver behavior; drones (Flipkart); crowdshipping (Ekart/Delhivery/Swiggy); Amazon EV 100% by 2030; DHL Delhi 6,000 shipments/h vs US/China 40,000/h; challenges (COVID, Russia-Ukraine, 80% trading partners fail, India 14% vs 7–8% cost, 60–65% road); KPIs; cases DHL (central nervous system), Amazon, Swiggy (hyper-local), Flipkart (60–65% share); conclusion: digitalization, innovation, sustainability |
| 20 | Logistics vs SCM | Used interchangeably; US = logistics management; Wayne & Johnson "no difference"; logistics = sub-process of SCM; inbound (raw material, packaging) vs outbound logistics; logistics = transport, warehousing, information, value-add; SCM adds R&D, manufacturing (what/how much/where/when), purchasing/sourcing (vendor rating 60%), customer service, global deployment, facility & labor planning; Michigan State University definition (collaboration); system view (share $10 profit/loss); furniture dismantle-and-reassemble; distance model (outbound shorter = cost-efficient; container 8–10 cars vs 200 cars raw material → locate plant near customer); Keith Oliver coined SCM; logistics components (information, storage, warehousing, material handling, packaging, transportation, inventory control, intermodal); GeoDis case (small e-tailers, 91% fulfillment); conclusion: logistics is part of SCM (transportation on time, safety stock storage, distribution) + integrate platforms |

---

*End of Decade 2 notes (Lectures 11–20).*
