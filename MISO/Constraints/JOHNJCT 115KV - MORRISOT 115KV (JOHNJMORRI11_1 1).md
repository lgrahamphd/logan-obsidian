### Basic Facts
**Monitored Element:** JOHNJCT 115 KV - MORRISOT 115KV
	- 115 kV line
**ISO:** [[MISO]]
	- OTP, OTP
**For loss of:**
1. WAHPEHANKS23_1 1
	- 230 kV line
2. WAHPETN TR21
	- 230/1 kV transformer
3. WAHPETN TR22
	- 115/1 kV transformer
4. WAHPETN TR23
	- 41.6/1 kV transformer
5. WAHPEWAHPE23_1 S
	- 230 kV line

- Direction: forward
- Constraint ID: 349876
- June, 2024 History
	- **DA**: $3.53/MWh shadow price; 17 hours
		- Peak: $2.66/MWh; 9 hours
		- Off-peak: $4.23; 8 hours
	- **RT**: $1.74/MWh shadow price; 3.9 hours
		- Peak: $0.64/MWh; 0.9 hours
		- Off-peak: $2.62/MWh; 3 hours
- July 1, 2024 - July 14, 2024 History
	- **DA**: $5.64/MWh shadow price; 17 hours
		- Peak: $9.25/MWh; 8 hours
		- Off-peak: $2.75; 9 hours
	- **RT**: $0.52/MWh shadow price; 1.5 hours
		- Peak: $1.25/MWh; 1.5 hours
		- Off-peak: $0/MWh; 0 hours
### Drivers
Upstream wind generation
1. Dakota Range I, II
	- 304 MW
2. Crowned Ridge Wind II
	- 201 MW
3. Crowned Ridge Wind Energy Center
	- 200 MW
4. Dakota Range III
	- 154 MW
5. Foxtail Wind
	- 150 MW
6. Deuel Harvest Wind
	- 300 MW

Big Stone output also pushes on the constraint with TRAVPFAIRM11_1 1 (115 kv line) out.

**Topology**
Two Big Stone transformers (115/1 kV, named BIGSTON TR12 and 13.8/1 kV, named BIGSTON TR23) were out during binding event on 6/27/2024, both with material LCDFs. Both are now out of service.

The 345 kV line BRKNGCO3 - BS1_GEN1 is on outage from 6/17/2024 - 8/14/2024. The BS1_GEN1 - LYON CO 3 345 kV line is on outage from 5/31/2024 - 9/30/2024, and the HAWKSNEST 3 - BRKNGCO3 345 kV line is out of service (since 5/31/2024). With these 345 kV lines out, key West -> East flow capacity has been removed, and the monitored element has received increased flows.

The above constraint bound even with other large supply into Minneapolis running at high capacity factors (Monticello, Sherburne County, Prairie Island, Coal Creek).
### Forward View
This constraint seems likely to bind throughout July and August. When BRKNGCO3 - BS1_GEN1 returns from outage mid-August, more West -> East flow capacity will be available, However, BS1_GEN1 - LYON CO 3 will be out through the end of September, and HAWKSNEST 3 - BRKNGCO3 is (recently) out of service.

Historically, the above topological drivers (which are to remain in place in the near term) dominated any sort of bearish high-side supply risk for the constraint. Even with high-side generation running at a high capacity factor, the constraint bound.

Generator shift factors indicate an exposure to Big Stone (~350 MW Coal plant), which was running at eco-min when the constraint bound.

The constraint appears to be exposed to low wind generation in Western Minnesota and Eastern South Dakota.

As long as we are comfortable with the risk of low levels of wind generation, this seems like a great short-term long position (subject to the caveat that we make this recommendation in isolation without regard for other elements of the portfolio).