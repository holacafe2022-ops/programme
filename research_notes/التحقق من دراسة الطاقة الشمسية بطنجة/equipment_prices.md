# Equipment specifications, PV yield and Moroccan prices: hybrid solar + battery villa, Tangier (checked Nov 2026)

## Q1. AstralPool / Fluidra Eco Elyo-13 (ref 76660) pool heat pump: capacity, input, COP, control, power-cutting

### Takeaway
The study's figures match the official Fluidra leaflet exactly. At 26/26: 13 to 2.4 kW thermal, 2 to 0.1 kW electric, COP 6.5 to 16.4. At 15/26: 9 to 1.7 kW thermal, 1.9 to 0.2 kW electric, COP 4.8 to 7.8. The unit has Wi-Fi and Bluetooth control through the Fluidra Pool app. I found no published external on/off dry contact and no maker guidance on frequent power-cutting.

### Cited Findings
- Fluidra Eco Elyo leaflet (EN, 2024), Air 26°C / Water 26°C / RH 80%, for the 13 kW model: heating capacity max–min 13–2.4 kW, power consumed max–min 2–0.1 kW, COP 6.5–16.4. **Datasheet-confirmed.** — [Fluidra leaflet Eco Elyo 2024](https://fluidra.bynder.com/m/4bffa94575a89c7f/original/leaflet_ecoelyo_EN_2024_01.pdf)
- Same leaflet, Air 15°C / Water 26°C / RH 70%: 9–1.7 kW thermal, 1.9–0.2 kW electric, COP 4.8–7.8. **Datasheet-confirmed.** — [Fluidra leaflet Eco Elyo 2024](https://fluidra.bynder.com/m/4bffa94575a89c7f/original/leaflet_ecoelyo_EN_2024_01.pdf)
- The leaflet says the unit has Bluetooth and Wi-Fi, and the "Fluidra Pool application lets you control all the settings remotely, 24 hours a day". It does not mention a remote on/off input or a dry contact. — [Fluidra leaflet Eco Elyo 2024](https://fluidra.bynder.com/m/4bffa94575a89c7f/original/leaflet_ecoelyo_EN_2024_01.pdf)
- Retailer listing for ref 76660: 13 kW (26-26) / 9 kW (15-26), COP 6.5–16.4, 220–240 V / 1 ph / 50–60 Hz, recommended flow 5 m³/h, Wi-Fi and Bluetooth with the Fluidra Pool App. Price €1,449. — [Quimipool](https://www.quimipool.com/en/13590-heat-pump-astralpool-eco-elyo-13-full-inverter.html)
- The Eco Elyo range runs down to −5°C air temperature, uses full-inverter compressor and fan speed control, and has a titanium exchanger that tolerates salt water. — [AstralPool Eco Elyo page](https://www.astralpool.com/en/en/heating/heat-pumps/eco-elyo.html); [Hidraulicart leaflet](http://www.hidraulicart.pt/wp-content/uploads/Bomba_Eco_Elyo_EN.pdf)
- General HVAC guidance (not specific to Fluidra): after a compressor stops, it should wait about 3–5 minutes before restarting, and many controllers enforce this anti-short-cycle delay. — [DIY StackExchange](https://diy.stackexchange.com/questions/145791/how-bad-is-it-for-my-a-c-unit-if-i-cut-the-power-while-its-working)
- User-forum view: frequent on/off cycling "may reduce compressor longevity, but actual impact is hard to quantify". This is anecdotal. — [Facebook group thread](https://www.facebook.com/groups/MyEfficientElectricHome/posts/24087414760876307/)

### Inferences
- The minimum-point COPs in the leaflet do not match the rounded inputs. 2.4/0.1 gives 24, not 16.4, and 1.7/0.2 gives 8.5, not 7.8. The input values are probably rounded (about 0.15 kW and 0.22 kW). The study should model with the COP values, not with the rounded kW inputs.
- At the maximum point, 13/2 = 6.5 and 9/1.9 = 4.7 (about 4.8), so the maximum figures are internally consistent.
- Recommended control strategy: modulate or schedule the unit through the app or its own timer, or switch the filtration pump that the heat pump relies on for flow. Avoid hard power cuts. Cutting mains bypasses the inverter's controlled ramp-down and may also lose its Wi-Fi state. If a Deye Smart Load / GEN-port output is used, set an SOC hysteresis band and a minimum on/off time of at least 10 minutes.

### Gaps
- I could not find the Eco Elyo installation manual, so the following are unconfirmed: a remote on/off or external contact terminal, an on-board timer, filtration pump priority, auto-restart after a power cut, and maximum current.
- I found no Fluidra statement on whether frequent mains interruption is harmful.
- I found no Moroccan price for the unit.

## Q2. Deye SUN-5/6/8/10/12K-SG04LP3-EU: unbalance, pass-through, battery, GEN port, zero-export; SG05LP3 comparison; warranty

### Takeaway
"100% unbalanced output" is confirmed, but the datasheet caps each phase at 50% of rated power. For the 12K that means about 6 kW per phase, or 26.1 A maximum unbalanced current. One phase cannot carry the full 12 kW. Other confirmed specs:
- Grid-to-load pass-through: 45 A continuous (the 2021 datasheet said 50 A).
- Battery: 48 V nominal, 40–60 V range, 240 A maximum charge/discharge on the 12K.
- GEN port: generator input, Smart Load output, or AC-coupled micro-inverter input, on a 63 A breaker.
- Warranty: officially 5 years, with 10 years optional.

### Cited Findings
- Datasheet (Oct 2024): "100% unbalanced output, each phase; Max. output up to 50% rated power". Battery voltage range 40–60 V. Maximum charge/discharge current 120/150/190/210/240 A for the 5/6/8/10/12K. Maximum continuous AC pass-through (grid to load) 45 A. Rated AC output 5–12 kW, maximum apparent power 5.5–13.2 kVA. Maximum PV input 7.5/9/12/15/18 kW. MPPT range 200–650 V, maximum 800 V. Efficiency 97.6% maximum. Grid codes include VDE-AR-N 4105 and EN 50549. Warranty: "5 Years/10 Years the Warranty Period Depends the Final Installation Site… refer to Warranty Policy". **Datasheet-confirmed.** — [Deye datasheet SG04LP3 2024](https://www.deyeinverter.com/deyeinverter/2024/10/21/datasheet_sun-5-12k-sg04lp3_241021_en.pdf)
- Maximum three-phase unbalanced output current is 10.9 / 13 / 17.4 / 21.7 / 26.1 A for the 5/6/8/10/12K. — [Deye datasheet SG04LP3 2025](https://www.deyeinverter.com/deyeinverter/2025/05/16/datasheet_sun-5-12k-sg04lp3.pdf); the manual gives the same figures (11.4/10.9 … 27.3/26.1 A) — [Deye manual SG04LP3-EU](https://www.deyeinverter.com/deyeinverter/2024/02/03/instructions_sun-5-12k-sg04lp3-eu_240203_en.pdf)
- The older 2021 datasheet listed 50 A maximum continuous AC pass-through and a 5-year warranty. — [Deye datasheet 2021](https://www.deyeinverter.com/deyeinverter/2021/06/30/%E3%80%90b%E3%80%91hybridinvertersun-8-10-12k-sg04lp3.pdf)
- From the manual, GEN port functions:
  - Generator input with settable rated power (e.g. 8,000 W).
  - "Smart Load Output: …utilizes the Gen input connection as an output which only receives power when the battery SOC is above a user programmable threshold."
  - "Micro Inv Input" for AC coupling (also works with grid-tied inverters).
  - The recommended GEN-port breaker is 63 A for all models. The manual lists 4 work modes including "Zero export to CT".
  — [Deye manual SG04LP3-EU](https://www.deyeinverter.com/deyeinverter/2024/02/03/instructions_sun-5-12k-sg04lp3-eu_240203_en.pdf)
- SG05LP3-EU-SM2 (3–12 kW), compared with the SG04LP3:
  - Same 40–60 V battery range and 240 A maximum (12K).
  - Same "100% unbalanced output, max 50% rated power per phase" and same 45 A pass-through.
  - Higher PV current: 20+20 A (3–8K) and 26+26 A on the 10/12K, versus 13+13 or 26+13 A on the SG04LP3.
  - Maximum PV input 19.2 kW on the 12K per the latest manual (18 kW in the 2024 datasheet).
  - Lighter at 35.2 kg versus 38 kg, and permits 3,000 m altitude versus 2,000 m.
  - Adds 3 kW and 4 kW models.
  - Warranty is the same 5/10 years by installation site.
  **Datasheet-confirmed.** — [Deye datasheet SG05LP3-EU-SM2](https://www.deyeinverter.com/deyeinverter/2024/09/27/datasheet_sun-3-12k-sg05lp3-eu-sm2_240927_en.pdf); [Deye SG05LP3 manual 2025](https://www.deyeinverter.com/deyeinverter/2025/11/17/%E3%80%90B%E3%80%91Manual_SUN-3-12K-SG05LP3-EU-SM2_20251115_en.pdf); [Deye product page](https://www.deyeinverter.com/product/three-phase-hybrid-inverter-1/sun3-4-5-6-8-10-12ksg05lp3eusm2-312kw-three-phase-2-mppt-hybrid-inverter-lv-battery-supported.html)
- Deye warranty terms v1.7: "The warranty period is 5 Years (10 Years Optional) from the date of installation, and no more than 5 Years (10 Years Optional) and half years from the date of delivery". The service table lists SUN-5/6/8/10/12K-SG04LP3 as 5 years (10 years optional). Under customer replacement, faulty units go back to Deye. **Document-confirmed.** — [Deye Warranty v1.7](https://www.deyeinverter.com/deyeinverter/2023/08/04/warranty-deye-v1.7.pdf)
- Some regions (Australia/NZ, EU for some models) have a dedicated 10-year limited warranty document: the first 5 years cover all parts, then a reduced scope. — [Deye AU/NZ 10-yr warranty V2.7](https://www.deyeinverter.com/deyeinverter/2025/11/28/WarrantyDocument-DeyeSUNSeriesinverter10-YearLimitedWarrantyforInstallationinAustraliaandNewZealand-V2.7.pdf); [EU SG01HP3 10-yr warranty](https://7sun.eu/wp-content/uploads/2025/06/warranty-deye-sun-5k-sg01hp3-eu-am2-sun-25k-sg01hp3-eu-am2.pdf.pdf)
- User report: with grid charging on a 12K-SG04LP3, grid current draw is "not balanced at all". — [Facebook Deye group](https://www.facebook.com/groups/419156130163742/posts/770805111665507/)

### Inferences
- The study's "100% unbalance" claim needs a caveat: it is 100% unbalanced only up to 50% of rated power per phase. For example, a 6 kW single-phase pool or EV load on one phase is the limit for the 12K model and exceeds the 10K (5 kW/phase).
- 45 A pass-through per phase is roughly 10.3 kW per phase at 230 V. This governs the backup/load-port circuits when the grid is present.
- Whether Morocco counts as a "10-year" site depends on the Deye distributor and the policy. Unless the installer documents the extension, the safe assumption is 5 years standard.
- Zero-export: the manual confirms a "Zero export to CT" mode and three-phase metering. Whether it regulates the per-phase sum or each phase individually is not stated (see Gaps).

### Gaps
- The manual does not state whether zero-export on the SG04LP3 nets the three-phase total (vector or arithmetic sum) or regulates each phase.
- I found no official maximum current or power for the Smart Load output itself, other than the 63 A breaker and the generator rated-power setting.

## Q3. Single-phase 10 kW hybrid (Deye SUN-10K-SG02LP1) on a three-phase supply: zero-export and phase netting

### Takeaway
A single-phase hybrid can only push power into its own phase. It cannot directly serve loads on L2/L3. Whether the bill reflects that offset depends on whether the utility meter nets the phases ("saldierend"). Deye's manual for a three-phase meter only asks which phase the inverter sits on, which implies it regulates against that phase only. German VDE-AR-N 4105 caps single-phase unbalance at 4.6 kVA per phase, so a 10 kW single-phase unit would not be allowed in Germany.

### Cited Findings
- Deye SUN-5-12K-SG02LP1 manual: "Ex_Meter For CT: when in Three phase system with CHNT Three phase energy meter (DTSU666), click corresponding phase where hybrid inverter is connected. e.g. when the hybrid inverter output connects to A phase, please click A Phase." — [Deye SG02LP1 manual V3.2.1](https://www.deyeinverter.com/deyeinverter/2025/12/04/InstallationManual-SUN-5-12K-SG02LP1-AU-AM3-V3.2.1.pdf)
- VDE-AR-N 4105: the maximum power difference between phases must not exceed 4.6 kVA (≈20 A). Larger systems need a three-phase inverter or several communicatively coupled single-phase units. — [energie-experten.org](https://www.energie-experten.org/erneuerbare-energien/photovoltaik/planung/vde-ar-n-4105); [solar-energy-consult.de](https://www.solar-energy-consult.de/photovoltaik/wissenswertes/niederspannungsrichtlinie-vde-ar-n-4105/)
- With a phase-netting ("saldierender") meter, single-phase feed-in (up to 4.6 kVA) is netted against three-phase household consumption. — [SENEC](https://senec.com/de/magazin/saldierender-zaehler)
- Forum reports of Deye zero-export behaviour on three phase: users note that three CTs or a Modbus meter are needed, and that export spikes occur when large loads drop. These are anecdotal. — [DIY Solar Forum](https://diysolarforum.com/threads/deye-weird-zero-export-to-ct-behavior.34974/); [Reddit r/SolarDIY](https://www.reddit.com/r/SolarDIY/comments/15lcjnt/deye_hybrid_inverter_pushing_power_to_grid_when/)

### Inferences
- With a netting meter (vector or arithmetic total), export on L1 can offset imports on L2/L3 for billing, but only if the inverter is allowed to export on L1. In strict per-phase zero-export (as the Deye phase-selection setting implies), the inverter throttles to the L1 load, and L2/L3 loads still import.
- With a per-phase or non-netting meter (common for older Moroccan ONEE/Amendis meters, unverified), any L1 export is lost or counted as export while L2/L3 import is billed. A three-phase hybrid avoids the problem.
- A 10 kW single-phase unit would breach the 4.6 kVA per-phase unbalance rule wherever that rule applies.

### Gaps
- I found no confirmation of which Moroccan utility meters (Amendis Tangier) net across phases, or of Moroccan unbalance limits under Law 82-21.
- I found no Deye statement on whether SG02LP1 firmware can regulate to a three-phase total.

## Q4. PV yield Tangier (35.76 N, −5.83 W)

### Takeaway
The Global Solar Atlas value in the study is confirmed exactly: PVOUT 1,693.8 kWh/kWp/yr, December 99.9 and July 174.3, data v1.7, updated April 2026. PVGIS-SARAH3 is about 2% lower at 1,661.8 kWh/kWp/yr for the optimum 32°/azimuth 4° with 14% losses. East or west at 15° tilt yields about 1,419–1,443 kWh/kWp, roughly 13–15% below optimum.

### Cited Findings
- Global Solar Atlas API (data v1.7, Solargis 2.2.68, updated 2026-04-01) at 35.76, −5.83:
  - PVOUT 1,693.8 kWh/kWp, GHI 1,849 kWh/m², GTI at optimum 2,100 kWh/m², DNI 1,949 kWh/m², optimum tilt 32°, mean temperature 17.9°C.
  - Monthly PVOUT (kWh/kWp), Jan–Dec: 108.3, 116.8, 145.0, 154.5, 165.3, 166.3, 174.3, 169.7, 151.4, 133.7, 108.6, 99.9.
  **Confirmed.** — [Global Solar Atlas API](https://api.globalsolaratlas.info/data/lta?loc=35.76,-5.83)
- PVGIS 5.3, PVGIS-SARAH3 2005–2023, ERA5 meteo, horizon on, free-standing, 14% system loss, optimum slope 32° / azimuth 4°:
  - E_y 1,661.75 kWh/kWp, SD_y 49.6 kWh, H(i)_y 2,128.8 kWh/m², total loss −21.9% (temperature −7.2%).
  - Monthly (kWh/kWp): Jan 111.6, Feb 112.5, Mar 137.9, Apr 146.9, May 159.8, Jun 159.5, Jul 170.1, Aug 166.9, Sep 148.9, Oct 134.1, Nov 107.6, Dec 106.0.
  — [PVGIS API optimum](https://re.jrc.ec.europa.eu/api/v5_3/PVcalc?lat=35.76&lon=-5.83&peakpower=1&loss=14&optimalangles=1&outputformat=json)
- PVGIS SARAH3, 15° tilt, 14% loss:
  - East (−90°): 1,419.4 kWh/kWp/yr (Dec 60.7, Jul 178.1).
  - West (+90°): 1,442.9 kWh/kWp/yr (Dec 60.0, Jul 181.7).
  — [PVGIS east](https://re.jrc.ec.europa.eu/api/v5_3/PVcalc?lat=35.76&lon=-5.83&peakpower=1&loss=14&angle=15&aspect=-90&outputformat=basic); [PVGIS west](https://re.jrc.ec.europa.eu/api/v5_3/PVcalc?lat=35.76&lon=-5.83&peakpower=1&loss=14&angle=15&aspect=90&outputformat=basic)

### Inferences
- An east/west 15° array averages about 1,431 kWh/kWp, a 13.9% loss against PVGIS optimum and 15.5% against GSA. Winter months fall by about 43%: December goes from 106 to about 60 kWh/kWp. This matters for winter self-sufficiency and for pool heating in shoulder seasons.
- GSA is about 1.9% above PVGIS. A conservative study could use 1,660 kWh/kWp for south and optimum tilt.

### Gaps
- I did not compute a south-facing 15° roof case or a rooftop (building-integrated/close-roof) mounting loss in PVGIS.

## Q5. Moroccan prices 2025–2026 (MAD), cycle life, BNEF

### Takeaway
The study's price assumptions check out against Moroccan retailers:
- 20 kWh LFP: 45,000–55,000 MAD is consistent (2 × MUST 10 kWh = 43,900 MAD; 4 × 5 kWh ≈ 56,000 MAD).
- MUST 10 kWh at 21,950 MAD (Misterelec): confirmed.
- Deye 12 kW three-phase hybrid: about 27,000–27,500 MAD.
- 575–620 W panels: about 900–1,300 MAD each.

Deye SE-G5.1 Pro is confirmed at ≥6,000 cycles at 90% DoD to 70% end-of-life, with a 10-year warranty. BNEF 2025: average pack $108/kWh, stationary storage $70/kWh, LFP $81/kWh.

### Cited Findings
- Misterelec (mrelec.ma):
  - MUST LiFePO4 10 kWh 200 Ah: **21,950 DH** (confirmed).
  - MUST LiFePO4 15 kWh 300 Ah: 27,650 DH.
  — [Misterelec batteries](https://mrelec.ma/collections/batteries-solaires)
- Misterelec Deye hybrid three-phase: 12 kW 27,500 DH, 15 kW 29,800 DH, 20 kW 37,900 DH. — [Misterelec Deye triphasé](https://mrelec.ma/products/onduleur-hybride-deye-triphase-20kw)
- Other Deye 12 kW three-phase hybrid quotes:
  - Special Energy: 27,000 MAD. — [Special Energy](https://specialenergie.com/product-category/onduleurs-hybrides/)
  - Battery Shop Maroc: 50,000 DH (sale price, from 60,000). This is an outlier. — [Battery Shop](https://batteryshop.ma/shop/energie-solaire/onduleurs-convertisseurs-solaires-off-grid-hybride/onduleur-deye-12kw-hybrid-triphase/)
- MUST PH3000 10–12 kW three-phase hybrid: 28,000–35,000 DH. — [panneauxsolaire.ma](https://panneauxsolaire.ma/product-category/onduleur-hybride/)
- Lithium battery prices at other shops:
  - 51.2 V 100 Ah (≈5.1 kWh): about 13,900 DH; 12 V 100 Ah: 3,800 DH. — [CP Tech Maroc](https://cptechmaroc.ma/product-category/produits-a-lunite/batterie-solaire/batterie-lithium/)
  - Lithium battery range 14,000–16,000 DH (capacity unspecified, likely 5 kWh). — [Electrosolarplus](https://electrosolarplus.ma/categorie-produit/batterie-solaire/)
  - Huawei LUNA: 65,000–145,800 MAD. — [Greenwagic](https://greenwagic.com/product-category/batteries-solaires/)
- Panel prices:
  - Briconet: Jinko 620 W bifacial 1,126 DH; Canadian Solar 580 W 1,067 DH. — [Briconet](https://briconet.ma/product-category/panneaux-solaires)
  - Electrosolarplus: Canadian TOPBiHiKu6 580–620 W, 900–1,100 DH. — [Electrosolarplus Canadian](https://electrosolarplus.ma/product-brand/canadian-solar/)
  - Iris.ma: Jinko bifacial 580 W, 1,299 DH TTC. — [iris.ma](https://www.iris.ma/46319-panneau-solaire-pv-jinko-bifacial-580w.html)
  - Greenwagic: Jinko 580–625 W, 980 MAD. — [Greenwagic Jinko](https://greenwagic.com/produit/jinko-solar-72hl4-580-tiger-neo-580-wc/)
  - Misterelec: Canadian 710 W bifacial 1,360 DH. — [Misterelec panels](https://mrelec.ma/collections/panneaux-solaires)
  - Facebook dealer: Sunrise 580 W, 800 DH. — [Facebook](https://www.facebook.com/groups/829823191789879/posts/1340121497426710/)
- Turnkey cost estimates:
  - Ecovolt (2025): 3 kW kit 25,000–35,000 MAD, 5 kW 40,000–60,000 MAD, 10 kW villa 80,000–120,000 MAD (≈8,000–12,000 MAD/kWc; scope unclear). — [Ecovolt](https://ecovolt.ma/prix-installation-solaire-au-maroc-en-2025/)
  - Installation labour 2,000–4,000 MAD/kWc. — [sunenergy.ma](https://sunenergy.ma/category/panneau-solaire/)
  - Entry systems from 22,024 MAD TTC. — [SolairOMaroc](https://solairomaroc.com/)
- Deye SE-G5.1 Pro-B datasheet: cycle life ≥6,000 (25±2°C, 0.5C/0.5C, 90% DoD, 70% EOL), recommended DoD 90%, warranty 10 years, up to 64 packs in parallel. **Datasheet-confirmed.** — [Deye SE-G5.1 Pro-B datasheet](https://nastechsolar.com.tr/content/STORAGE/DEYE/SE-G5.1%20PRO/Datasheet%20Deye%20SE-G5.1-Pro%20B.pdf); [Lirik Solar datasheet](https://liriksolar.com/image/uploads/Deye%20SE-G5.1%20Pro%20Datasheet.pdf)
- BNEF 2025 Battery Price Survey (9 Dec 2025):
  - Average Li-ion pack price $108/kWh (−8% year on year).
  - Stationary storage packs $70/kWh (−45%), the lowest segment for the first time.
  - BEV packs $99/kWh.
  - LFP average $81/kWh, NMC $128/kWh.
  - China average $84/kWh; North America and Europe 44% and 56% higher.
  - Lowest observed cell and pack prices $36 and $50/kWh.
  - BNEF expects a further decline in 2026.
  — [BNEF press release](https://about.bnef.com/insights/clean-transport/lithium-ion-battery-pack-prices-fall-to-108-per-kilowatt-hour-despite-rising-metal-prices-bloombergnef/); [BNEF "New record lows"](https://about.bnef.com/insights/clean-transport/new-record-lows-for-battery-prices/)

### Inferences
- Moroccan retail LFP costs about 2,200 MAD/kWh (MUST 10 kWh) and about 1,840 MAD/kWh (MUST 15 kWh), roughly $220/kWh and $185/kWh at about 10 MAD/USD. That is about 2.5–3× BNEF's stationary pack price, which is normal for retail plus BMS, enclosure, import duty and VAT. The 45,000–55,000 MAD for 20 kWh (2,250–2,750 MAD/kWh) is realistic and slightly conservative.
- Panel cost is about 1.6–2.2 MAD/Wc.
- Inverter replacement cost proxy: about 27,000–30,000 MAD today for a 12 kW Deye three-phase hybrid, before installation labour. This is expected to fall in real terms.
- A turnkey hybrid villa system (PV + hybrid inverter + 20 kWh) would plausibly land at about 8,000–12,000 MAD/kWc of PV including the battery share. Ecovolt's ranges are indicative, not itemised quotes.

### Gaps
- I found no Moroccan price for Deye SE-G5.1 Pro batteries or for the Deye SUN-10K-SG02LP1.
- I found no Wafir.ma data, no MUST battery cycle-life datasheet, and no Tangier-specific installer quotes. Prices are from Casablanca and online retailers and were not re-checked for stock or VAT inclusion.
