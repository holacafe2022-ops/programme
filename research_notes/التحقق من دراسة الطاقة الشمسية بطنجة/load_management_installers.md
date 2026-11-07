# Load management for zero-export residential solar (Tangier villa) and installer due diligence — as of Nov 2026

Research budget note: about 15 tool calls. Several items (filtration pump consumption, single vs three-phase steam generator, AMEE villa consumption statistics, TAQA Pro public list) could not be confirmed from primary sources in this pass and are listed as gaps. Physics-based numbers are marked as inferences (standard constants), not cited facts.

## 1. Pool heating: energy, losses, covers, daytime heat-pump scheduling, filtration pump

### Takeaway
The pool-cover claim (50–70% savings) is confirmed in US DOE documents, and evaporation is the dominant loss (about 50–70% of pool heat loss), so a cover is the main lever. The 1.163 kWh/m³·°C figure is correct physics. Running the pool heat pump in daytime on PV surplus is reasonable in principle (warmer air raises the heat pump's COP, and solar output is available), but no Morocco-specific measurement was found.

### Cited Findings
- DOE's 2023 energy conservation standards rulemaking for consumer pool heaters states that "DOE assumes that a pool cover can save up to 50-70 percent" of pool heating energy — [US DOE, Energy Conservation Standards for Consumer Pool Heaters (2023 final rule PDF)](https://www.energy.gov/sites/default/files/2023-03/ph-ecs-fr.pdf)
- DOE BTO report: "Properly employed and regularly-used pool covers can save pools between 50-70%", with results varying by site — [US DOE BTO, Energy Savings Potential and RD&D Opportunities for Commercial Appliances (2016)](https://www.energy.gov/sites/prod/files/2016/06/f32/DOE-BTO%20Comml%20Appl%20Report%20-%20Full%20Report_0.pdf)
- DOE school O&M guide: pool covers give energy savings of 50–70%, plus 30–50% less make-up water and 35–60% less chemicals — [US DOE, School O&M Best Practices](https://www.energy.gov/sites/prod/files/2015/04/f21/ED486496.pdf)
- Evaporation accounts for 50–60% of a pool's heat loss (M&V study of a pool with a liquid cover) — [ETCC Engineering M&V Study (2010)](https://www.etcc-ca.com/sites/default/files/OLD/images/stories/heatsavr_expr_workout_club_report_r2_4-12-10.pdf); a utility article puts it at about 70% — [Tennessee Electric Cooperative Assoc.](https://tnelectric.org/2014/07/01/limiting-swimming-pool-heat-loss/)
- Evaporation depends on water temperature, air humidity and wind, which the heat pump cannot control. This is why heat-pump sizing assumes a cover — [PHNIX (heat-pump manufacturer)](https://www.phnix-e.com/index.php/slug/pool-cover-evaporation-heat-pump-sizing.html)
- A state-of-the-art review of pool heating models (heat-loss and heat-gain calculation) exists for detailed modelling — [Building Simulation review, Swimming pool heating technology](https://www.sciopen.com/article/10.1007/s12273-020-0669-3?issn=1996-3599)

### Inferences
- 1.163 kWh/m³·°C is correct: water's specific heat is 4.186 kJ/kg·K, so 1,000 kg × 4.186 kJ ÷ 3,600 = 1.163 kWh per m³ per °C. A 50 m³ pool raised 5 °C needs about 291 kWh thermal; with a heat pump at COP 4–5 that is about 58–73 kWh electric. These are standard-physics figures, not from a fetched source.
- In Tangier, a windy coastal site, evaporative and convective losses are likely high on an uncovered pool. The cover is the precondition: without it, a PV-surplus heat pump mainly offsets evaporation losses.
- Daytime scheduling is sound for two reasons: (a) PV output peaks at midday and (b) a heat pump's COP is higher with warm afternoon air. In a zero-export system this is one of the easiest flexible loads to absorb, because surplus PV is otherwise curtailed and wasted.

### Gaps
- No fetched source for typical filtration-pump consumption. A commonly quoted range is 0.75–1.5 kW single-speed or 0.2–0.6 kW variable-speed, run 4–8 h/day, but this was not verified here. The DOE pool pump rulemaking would be the primary source.
- No Mediterranean or Moroccan measured study of outdoor pool losses was retrieved.

## 2. Steam hammam / 9 kW steam generator: energy per session; single vs three-phase

### Takeaway
I found no primary manufacturer data. A ~8 kWh session for a 9 kW unit (versus 13.5 kWh theoretical maximum over 1.5 h) means a ~60% average duty cycle. That is plausible, because the heat-up phase runs at 100% and then the thermostat cycles, but it is not verified. Treat ~8 kWh as an estimate that depends on room size, insulation and session length.

### Cited Findings
- A retailer states that a typical 20–30 min home steam-shower session uses about 1–4 kWh. This refers to small steam showers, not a 9 kW hammam room — [SteamShowers4Less](https://steamshowers4less.com/Do-Steam-Showers-Use-A-Lot-Of-Water-And-Electricity)
- Sauna analogy: Harvia gives about 7–9 kWh over two hours for a home sauna heater (4.5–9 kW class), i.e. well below nameplate × hours because of thermostat cycling — [SaunaSteamCenter, citing Harvia](https://saunasteamcenter.com/sauna-electricity-cost/)
- Operating-cost blog: a 6 kW heater for 1.5 h including preheat is costed as a full-power run, which overestimates — [InHouseWellness](https://inhousewellness.com/blogs/saunas/home-sauna-steam-room-lifetime-operating-costs)
- Forum estimate: ~7.5 kWh per 1-h session, with a real duty cycle "closer to 30%" for a well-insulated room (anecdotal, low reliability) — [Reddit r/Sauna](https://www.reddit.com/r/Sauna/comments/1r2ohoq/how_many_kw_per_hour/)

### Inferences
- A steam generator differs from a sauna heater because it must keep boiling water to replace steam that condenses on walls. Duty cycles for steam rooms are therefore probably higher than for well-insulated saunas. A 50–70% average (≈7–9.5 kWh per 1.5 h) seems a reasonable band, so the study's ~8 kWh is in range but optimistic for a poorly insulated or tiled room with a long preheat.
- Electrical calculation (not sourced): 9 kW on 230 V single-phase draws ≈39 A, which needs a dedicated 40 A circuit and heavy cable. On 400 V three-phase it draws ≈13 A per phase. Many 9 kW generators are sold as dual-voltage or three-phase. For zero-export sizing, a 9 kW block exceeds the output of most residential hybrid inverters (5–8 kW single-phase), so sessions will mostly draw from the grid or battery unless scheduled at midday and limited in power.
- Load-shifting lever: running sessions in early afternoon (PV peak) and preheating on PV is the only meaningful shift. Otherwise the hammam is a large evening grid load.

### Gaps
- No manufacturer data (e.g. Tylö, Helo, Mr.Steam) on measured kWh per session or duty cycle was retrieved.
- Whether this villa's supply is single- or three-phase, and what ONEE/Amendis subscription power it has, is unknown.

## 3. PV surplus to water heater in a ZERO-EXPORT system; 300 L storage; butane price

### Takeaway
Classic solar routers (diverters) measure current exported to the grid at the meter CT and divert it. In zero-export mode the inverter throttles PV so that export never appears, so the router never sees a surplus and does not trigger. Alternatives are inverter-side: Deye's GEN port in "Smart Load" mode (switched on SOC/voltage thresholds), inverter-driven relays, or Home Assistant automations that read inverter data. A 300 L tank heated +40 °C stores ≈14 kWh thermal. Butane 12 kg is still 50 MAD as of Nov 2026: the planned 2025 and 2026 increases were cancelled, and the government confirmed the freeze again in 2026.

### Cited Findings
- A Deye owner in a country where export is not allowed asks how to divert surplus. The thread illustrates that grid-export-sensing diverters cannot work under zero export — [Reddit r/SolarDIY, "Power diverter with zero export to grid"](https://www.reddit.com/r/SolarDIY/comments/17myiby/power_diverter_with_zero_export_to_grid/)
- Deye hybrids have a programmable GEN port that can be set as a "Smart Load" output. It is configured with battery SOC/voltage on/off thresholds under the GEN port menu, alongside "Zero Export to CT" work mode — [PowerForum.co.za thread on Deye Smart Load settings](https://powerforum.co.za/topic/28278-deye-5kw-inverter-advise-needed-for-smart-load-settings-when-in-off-grid-mode-only-running-solar-power-and-batteries/); [YouTube: Deye 12 kW Gen Port Smart Load functionality](https://www.youtube.com/watch?v=kwLk8vvkq2Q)
- The Deye hybrid manual (SUN-7.6/8K-SG01LP1-EU, Aug 2025) documents the "Selling First" and "Zero export to Load" work modes — [Deye manual PDF](https://www.deyeinverter.com/deyeinverter/2025/08/19/%E3%80%90b%E3%80%91manual_sun-7.6-8k-sg01lp1-eu_20250819_en-1.pdf)
- Users report unexpected Smart Load port behaviour (triggering with zero solar input) when zero-export-to-CT settings are combined with charge limits. Configuration errors are common — [Facebook Deye user group](https://www.facebook.com/groups/1238752480298654/posts/2344137453093479/)
- **Butane history:** the 12 kg cylinder rose from 40 to 50 MAD in May 2024 (first decompensation step) — [L'Économiste](https://www.leconomiste.com/1120511-decompensation-du-gaz-butane-le-gouvernement-passe-l-acte/); [Le Desk](https://ledesk.ma/encontinu/prix-du-gaz-butane-la-decompensation-partielle-prend-effet-a-partir-de-ce-lundi/). The original plan was 60 MAD in 2025 and 70 MAD in 2026 — [EcoActu](https://ecoactu.ma/decompensation-gaz-butane-une-hausse-a-70-dh/); [L'Opinion](https://lopinion.ma/fr/actu-maroc/decompensation-partielle-du-gaz-butane--quelles-repercussions-sur-les-menages-marocains--integral_a53287)
- The 2025 increase was dropped: the 12 kg cylinder stayed at 50 MAD and the 3 kg at 12.5 MAD — [Hespress FR](https://fr.hespress.com/451302-gaz-butane-le-gouvernement-renonce-a-la-hausse-des-prix.html); [Bladi.net](https://www.bladi.net/maroc-prix-gaz-butane-changera-2025,118097.html)
- PLF 2026 coverage (21 Oct 2025): the real cost of the 12 kg cylinder is ≈140 MAD, with a state subsidy of ≈70 MAD. The article referred to a 70 MAD target price — [H24info](https://h24info.ma/economie/plf-combien-bonbonne-de-gaz-en-2026/)
- 25 Nov 2025: PM Aziz Akhannouch told Parliament there would be no increase. The 12 kg cylinder stays at 50 MAD and the 3 kg at 12.5 MAD — [Médias24](https://medias24.com/2025/11/25/aziz-akhannouch-le-prix-du-gaz-restera-inchange-1584007/); [L'Opinion](https://lopinion.ma/fr/actu-maroc/gaz-butane--aucune-nouvelle-augmentation-du-prix-nest-prevue-selon-aziz-akhannouch_a98317)
- 2026 developments: after an international butane price spike tied to a Middle East crisis (+68%), the government in March–April 2026 confirmed it would keep the cylinder price unchanged. It is spending about 600 MDH/month on butane, within ~1.6 bn MAD/month of energy support, and also froze electricity tariffs — [Le Desk, 3 Apr 2026](https://ledesk.ma/2026/04/03/subventions-de-lenergie-16-milliard-de-dirhams-par-mois-pour-proteger-le-pouvoir-dachat/); [LeBrief](https://www.lebrief.ma/crise-au-moyen-orient-soutien-exceptionnel-du-gouvernement-au-gaz-et-transport-100146442/); [Atalayar, 31 Mar 2026](https://www.atalayar.com/fr/articulo/economie-et-entreprises/maroc-gele-tarifs-du-butane-et-lelectricite-face-hausse-mondiale-des-prix-lenergie/20260331210000224449.html); [Yabiladi](https://www.yabiladi.com/articles/details/191328/akhannouch-rassure-hausse-prix-butane.html)

### Inferences
- 300 L × 40 °C × 1.163 Wh/L·°C ≈ 13.96 kWh thermal stored. This is standard physics and matches a typical claim of "~14 kWh".
- Butane comparison (inference using butane's standard lower heating value of ≈45.7 MJ/kg ≈ 12.7 kWh/kg, not from a fetched source): 12 kg ≈ 152 kWh thermal for 50 MAD ≈ 0.33 MAD/kWh. With a gas water heater at ~80–85% efficiency, that is ≈0.39–0.41 MAD per useful kWh. This is cheap compared with grid electricity, so displacing butane with "free" curtailed PV is worth roughly 5–6 MAD per full 300 L reheat. Savings are modest in money terms; the main argument is using PV that would otherwise be curtailed.
- The claim "fixed at 50 MAD as of Nov 2025 (Hespress)" is confirmed, and as of Nov 2026 the price is still 50 MAD. The 60/70 MAD trajectory has been suspended, not formally replaced by a new schedule. Future increases remain a policy risk (real cost ≈140 MAD) but have not been announced.
- Practical zero-export diverter options: (1) Deye GEN port in Smart Load mode driving a contactor to a resistive element. This is binary on/off with SOC thresholds, not proportional. (2) Inverter dry-contact/relay, or Home Assistant (e.g. Solarman/Modbus integration) switching the heater when battery SOC is high and PV power is near its limit. (3) Proportional routers placed on the inverter output instead of the grid connection. These need a "fake surplus" logic and are unreliable in zero-export mode. A timer at solar noon is the crude fallback.

### Gaps
- I did not find an authoritative Deye document that explains the GEN Smart Load logic step by step in zero-export mode. Forum and YouTube sources only.
- No source found for a Moroccan market price list of resistive or heat-pump water heaters integrated with hybrid inverters.

## 4. Pre-cooling with inverter ACs to shift load into solar hours

### Takeaway
The cited Mayes et al. paper exists, but it was published online in Oct 2023 (Environ. Res.: Energy 1, 015001, often cited as 2024). It is a California TOU/grid study, not a zero-export study. It shows 1–4 kWh/day of peak-period load can be shifted, with smaller absolute shifts in mild coastal climates (e.g. San Francisco CZ3). Australian work on "solar pre-cooling" is the closer analogue. For Tangier's mild summers, the expected shift is likely small, about 1–2 kWh/day on hot days.

### Cited Findings
- Mayes S., Zhang T., Sanders K.T., "Residential precooling on a high-solar grid: impacts on CO2 emissions, peak period demand, and electricity costs across California", *Environmental Research: Energy* 1 (2024) 015001, published online 9 Oct 2023. Results: precooling reduces peak-period consumption by 1–4 kWh/day (up to 4.2), eliminating 8–61% (Building 1) and 18–82% (Building 4) of peak-period demand, with CO2 reductions of 1–22%. In mild coastal zones (CZ3/San Francisco) reductions are smaller in absolute terms (1.1–2.4 kWh/day) but larger in percentage, and need a larger on/off-peak price ratio to save money — [IOPscience](https://iopscience.iop.org/article/10.1088/2753-3751/acfa91); dataset: [Mendeley Data](https://data.mendeley.com/datasets/333jfmpvb8/1)
- Earlier work by the same group: replacing a constant setpoint with precooling cut peak-period electricity by 57% for a Southern California single-family home — [Mayes & Sanders 2022, Environ. Res. Infrastruct. Sustain. (NSF PAR)](https://par.nsf.gov/biblio/10397154)
- Australian research on using surplus PV for Solar Pre-Cooling and pre-Heating (SPCaH) across the housing stock — [Energy and Buildings 2025 (ScienceDirect S0378778825002865)](https://www.sciencedirect.com/science/article/pii/S0378778825002865); a temperature-independent model for solar pre-cooling potential — [MDPI Energies 15(23) 9257](https://www.mdpi.com/1996-1073/15/23/9257); a review of pre-cooling and solar pre-cooling — Naderi et al., Energy & Buildings 272 (2022) 112340 (cited in the Mayes paper's references).

### Inferences
- In a zero-export system the benefit differs from TOU arbitrage. The gain is using PV that would otherwise be curtailed, at no extra cost, so even small shifts (1–2 kWh/day) have value. The price-ratio barrier in the Mayes paper does not apply.
- Tangier has mild summers moderated by the sea (CZ3-like rather than inland California), so cooling demand and the shiftable load are modest. Pre-cooling helps most on hot east-wind (chergui/levante) days. Heavy masonry villas store more coolth, which favours pre-cooling.
- The paper does not study Morocco or zero-export systems. A writer citing it should say "California simulation; directional evidence only".

### Gaps
- No Australian zero-feed-in field measurement with numeric results was retrieved in full. The ScienceDirect/MDPI items were seen as abstracts only.
- No Moroccan or Mediterranean pre-cooling study was found.

## 5. Typical electricity consumption of Moroccan villas with pool and AC

### Takeaway
No ONEE, AMEE or other Moroccan statistic for villa consumption (with pool and AC) was found in this pass. Searches returned only European averages.

### Cited Findings
- Search results gave only European averages (e.g. France ≈4,000 kWh/yr per dwelling — [EDF](https://particulier.edf.fr/fr/accueil/guide-energie/electricite/consommation-moyenne-electricite.html)), which do not apply to Morocco.

### Inferences
- The study's consumption baseline should come from the villa's own 12 months of ONEE/Amendis bills (Tangier is served by Amendis/Veolia, now in transition to the regional multiservice company SRM). Bills are more reliable than any national average.

### Gaps
- No ONEE, AMEE, HCP or ANRE published figure on villa-type consumption was found. HCP household energy surveys or ANRE reports may hold these figures but were not retrieved.

## 6. Installer due diligence: GEOMAREC, Solarex Maroc, TAQA Pro, low-quote red flags

### Takeaway
Both companies exist as registered SARLs in Tangier. GEOMAREC is young (Jan 2022) and a generalist in plumbing, AC, solar and pools. Solarex (2018) is a small solar specialist with 1–9 staff. Neither has meaningful public reviews. TAQA Pro is the AMEE-run PV installer quality label, created with the Cluster Solaire and AMISOLE. I could not find the public list, so ask each installer for its certificate. A quote of ~6,000 MAD/kWc is well below the market range quoted in 2026 Moroccan sources and needs a line-by-line check.

### Cited Findings
**GEOMAREC**
- Charika.ma (Inforisk): SARL, created 22 Jan 2022, capital 100,000 MAD. Corporate purpose: general plumbing, electrical works, air-conditioning, solar energy, refrigeration, plastics. Address: Résidence Al Azizia, Bd Royaume d'Arabie Saoudite, 3e étage N°20, Tanger-Médina. ICE begins "0029…" (full ICE/RC behind paywall). 2 directors listed — [Charika.ma](https://www.charika.ma/societe-geomarec-1076942); same address on [Business Trust Africa](https://www.bt-africa.com/fr/entreprise/cdb90afa379e9a01dac690949fe4f424-geomarec)
- Self-description: "climatisation, énergies solaires, chauffage, piscines et plomberie général" — [Tachrone.ma](https://tachrone.ma/en/profile/geomarec/5785); [lechantier.ma](https://lechantier.ma/pros/profil/geomarec)
- Social media shows small hybrid PV projects in Tangier (e.g. a July 2025 "mini projet photovoltaïque", hybrid installation) — [Instagram @geomarec](https://www.instagram.com/geomarec/); [Facebook Geomarec](https://www.facebook.com/p/Geomarec-100061038827868/)

**Solarex (Solarex Maroc)**
- Telecontact: SARL created 2018, capital 90,000 MAD, 1–9 employees, manager M. Ahariz Nourddin, 49 rue Soudan, Saâda, Tanger. RC 89057 (Tanger), ICE 002080243000028. Activities: design, installation and maintenance of solar stations. "Aucun avis" (no reviews) — [Telecontact.ma](https://www.telecontact.ma/annonceur/solarex/9035101/tanger.php)
- Company website: "fondée en 2018", 49 Rue Soudan Assaada, Tanger; +212 539 365 432; contact@solarexmaroc… — [solarexmaroc.com](https://solarex.solarexmaroc.com/); listed "Vérifié" on [Kerix](https://www.kerix.net/fr/annuaire-entreprise/solarex-maroc)
- Facebook page "Solarex Sarl": not yet rated (0 reviews), phone +212 661-964659 — [Facebook](https://www.facebook.com/p/Solarex-Sarl-100064370611334/)
- Discrepancy: Charika lists a "SOLAREX" at a different address (2 Rue Yacoub Mansour, 1er étage N°01, Tanger-Médina) with ICE beginning "0020…". This could be the same company at an earlier or registered address, or a different entity — [Charika.ma](https://www.charika.ma/societe-solarex-769637). Not resolved.

**TAQA Pro label**
- TAQA Pro is the Moroccan quality label for PV installers, run by AMEE — [Energy Partnership Morocco–Germany (GIZ/PAREMA)](https://energypartnership.ma/news/taqa-pro-quality-label/); [Watt Power Engineering (mentions "Taqa Pro PV Plus certified by AMEE")](https://wattpowerengineering.com/en/solaire-photovoltaique.html)
- It was launched by the Cluster Solaire with AMEE. Certificates are described as issued by AMISOLE, AMEE and the Cluster Solaire, with variants including PV pumping — [Cluster Solaire Facebook](https://www.facebook.com/ClusterENR/posts/dans-le-cadre-du-label-taqa-pro-lanc%C3%A9-par-le-cluster-solaire-en-partenariat-avec/2759533540980970/); [Shamsiyah/DLM ENR](https://shamsiyah.ma/taqa-pro-pompage-pv/); [Aujourd'hui le Maroc](https://aujourdhui.ma/economie/taqa-pro-lancement-du-label-des-installateurs-dans-le-secteur-du-photovoltaique-au-maroc)
- AMEE has a parallel "ThermoPro" label for solar thermal installers — [M24TV YouTube](https://www.youtube.com/watch?v=nacuimoYkyM)

**Pricing / low-quote red flags**
- Wafir.ma (12 Jun 2026) quotes installation costs of 35,000–160,000 MAD for 3–10 kWc, 60–80% bill savings and a 5–7 year ROI. I could not extract the article body to confirm the per-kWc figure — [Wafir.ma guide](https://wafir.ma/fr/guide/credit-panneaux-solaires-maroc-2026-5-banques-roi-6-ans)
- A Moroccan discount installer advertises ~2.4 kWc from 22,024 MAD TTC (≈9,200 MAD/kWc) as "25–40% cheaper" than the market — [SolairOMaroc](https://solairomaroc.com/)

### Inferences
- 35,000 MAD for 3 kWc ≈ 11,700 MAD/kWc, and 160,000 MAD for 10 kWc ≈ 16,000 MAD/kWc. Both sit within the 10,000–16,000 MAD/kWc range the study attributes to Wafir; the exact page wording was not confirmed. Even a self-declared discount installer is at ≈9,200 MAD/kWc. A quote of ~6,000 MAD/kWc is therefore ~35–60% below market. Possible explanations: no battery or battery priced separately, panels only with no inverter, grade-B or unbranded modules, no mounting structure or protections (DC/AC SPDs, fuses, earthing), no Amendis/ONEE declaration, labour only, or VAT excluded. Request an itemised BOM with brands and models, datasheets, warranty terms, a TTC/HT breakdown and a written scope.
- Due-diligence checklist: verify the full ICE/RC via OMPIC (directinfo/charika paid view), ask for the TAQA Pro certificate (name of certified technician and validity date) and for 2–3 local references you can visit, and check insurance (RC décennale/professionnelle). Under Law 82-21 on self-production, check that the installer will handle the declaration to the distributor.
- GEOMAREC's generalist profile (pool, AC, plumbing, solar) could suit the whole-villa load-management plan, but it is a young company with limited capital. Solarex is longer-established but also small, with no public reviews. Neither showed evidence of TAQA Pro certification online.

### Gaps
- No public, searchable TAQA Pro installer registry was found online. Whether AMEE publishes the list could not be confirmed, so ask AMEE or the Cluster Solaire directly.
- No reviews (Google Maps or forums) with substantive content were found for either company.
- Full ICE for GEOMAREC and the reconciliation of the two Solarex addresses need a paid OMPIC/Charika lookup.
- The Wafir.ma per-kWc numbers were not extracted verbatim.
