Last updated: 2025-09-03
#### Summary Characterization
Chronic MISO-SPP tie line constraint driven by Southward wind transfer. More localized to Omaha load (pulling) and Sioux City-area wind generation than Raun - Ft. Calhoun, which is at the 345 kV level (and hence more driven by macro effects). Flows over Raun-Tekamah have a strong negative correlation with Walter Scott Jr. output.
### Basic Facts
**Monitored Element:** RAUNTEKAM16_1 1
- Common Name: Raun - Tekamah
- From Bus: RAUN 5 161 kV
- To Bus: TEKAMAH5 161 kV
- From Zone: [[MidAmerican Energy Company|MEC]] ([[MISO]])
- To Zone: [[Omaha Public Power District|OPPD]] ([[SPP]])
**For loss of:** MECOPP1
1. FT_CARAUN34_1 1
    - From Bus: FT_CAL
    - To Bus: RAUN
**Direction Bound:** Southward from Raun to Tekamah

---
### Ratings, Flows, Generation, and Load
**Line Ratings:** ratings fluctuate from 217 MW to 284 MW (both post-contingent). These appear to be seasonal ratings. SPP's state estimator ratings for the line look to be incorrect. Need to look at FFEs to get a better idea for the rating ground truth.

**Flow Bias:**
Southward from Raun to Tekamah, though flow can reverse. Roughly 70% of the time, flows are southward.

**Low-Side Generation:**
Wind generation to the North, East, and West.

**High-Side Generation:**
- Lon Wright (130 MW coal ST, 40 MW NG GT, 2 MW solar)
- Walter Scott Jr.

**Load:**
Omaha, NE.

---
### Binding Events and Drivers
**Transmission Outages:**
- Tekamah - Oakland 115 kV is a switching solution that relieves Tekamah-Substation 1226 at the expense of increasing flows on Raun-Tekamah.