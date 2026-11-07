# Amendis (Tangier) BT residential electricity tariffs, as of November 2026: verification of the solar study's tariff model

Research date: 2026-11-07. All prices are in MAD (DH). HT = before VAT, TTC = including VAT. "Confirmed" means read from an official grid or document. "Derived" means computed here.

## 1. Actual 2026 prices for the six BT domestic tranches (Amendis Tanger)

### Takeaway
Amendis publishes a 2026 grid for Tangier ("Tarifs en vigueur à partir du 01/01/2026"). It confirms the study's tranche 5 figure (1.3172 HT). It does not confirm tranche 6: the official price is **1.5272 HT, not 1.5515**. The study's ×1.0492 extrapolation overstates T6 by about 0.024 DH/kWh, roughly 1.6%.

### Cited Findings
- The Amendis "Consommations et factures" page publishes "Amendis Tanger : Tarifs en vigueur à partir du 01/01/2026" as image tables. The Tangier electricity table is the image `electricit%C3%A9.png` (uploaded 2026/06). — [Amendis – Consommations et factures](https://www.amendis.ma/fr/nos-activites/relation-client/client-particulier/consommations-factures)
- Tangier BT "Usage domestique" grid, transcribed from that image (two separate OCR passes gave the same numbers) — [Amendis Tanger 2026 electricity grid (image)](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/electricit%C3%A9.png.webp?itok=Kpa7Uw_7):

| Tranche | kWh/month | Billing mode | Price HT (DH/kWh), confirmed | TTC at 20% VAT (derived) |
|---|---|---|---|---|
| T1 | 0–100 | Progressive (≤150 kWh) | 0.8098 | 0.9718 |
| T2 | 101–150 | Progressive (≤150 kWh) | 0.9005 | 1.0806 |
| T3 | 151–210 | Sélective (>150 kWh) | 0.9639 | 1.1567 |
| T4 | 211–310 | Sélective | 1.0697 | 1.2836 |
| T5 | 311–510 | Sélective | **1.3172** | 1.5806 |
| T6 | >510 | Sélective | **1.5272** | 1.8326 |

- The same Tangier image also lists other BT tariffs: Eclairage patenté 0–150 kWh 1.5384 and >150 kWh 1.7591; Force motrice 0–100 1.3821, 101–500 1.5020, >500 1.7097; Eclairage public 1.3077; Eclairage administratif 1.9229. — [Amendis Tanger 2026 grid](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/electricit%C3%A9.png.webp?itok=Kpa7Uw_7)
- The image itself does not say "HT" or "TTC". — [same image](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/electricit%C3%A9.png.webp?itok=Kpa7Uw_7)
- Tétouan has a different 2026 grid. Read from the Tétouan image: T3 1.0116, T4 1.1223, T5 1.3336, T6 1.5449. T1 reads 0.8098 and T2 about 0.8996, but the OCR output for those two rows was garbled. — [Amendis Tétouan 2026 grid (image)](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/%C3%A9lectricit%C3%A9.png.webp?itok=G3Xt3hxo)
- Redal (Rabat) 2026 grid, labelled "hors TVA, en vigueur depuis le 1er janvier 2026": T1 0.79927, T2 0.95064, T3 0.95064, T4 1.05684, T5 1.23225, T6 1.45167. — [Redal – Grille tarifaire 2026 (PDF)](https://www.redal.ma/sites/g/files/dvc3366/files/document/2026/04/Grille%20tarifaire%202026.pdf)
- ONEE's direct-customer page shows slightly different bands: 0–100 0.9010; 101–150 1.0732; 151–200 1.0732; 201–300 1.1676; 301–500 1.3817; >500 1.5958. Its bands end at 200/300/500 rather than 210/310/510, and the page does not say whether the prices are HT or TTC. — [ONEE – Nos tarifs](https://www.one.org.ma/FR/pages/interne.asp?esp=1&id1=3&id2=113&t2=1)

### Inferences
- The study's T5 is right: 1.3172 HT × 1.20 = 1.58064, which matches the bill's 1.5806 TTC. This shows that the Amendis grid prices are HT and that 20% VAT applies in 2026.
- The study's T6 needs correcting: use **1.5272 HT (1.8326 TTC)**, not 1.5515 HT.
- In Tangier, T3 (0.9639) is higher than T2 (0.9005). In Redal's grid T3 equals T2. Any model that sets T3 = T2 for Tangier is wrong.
- The claim of "national uniform prices since decision 451.14 (2014)" does not hold for the final unit prices. Amendis Tanger, Amendis Tétouan, Redal and ONEE all publish different 2026 figures. The tranche structure (progressive up to 150 kWh, selective above) is common to them; the exact prices differ by distributor and city. The relative ratios are similar, which is why the ×1.0492 scaling came close but still missed.

### Gaps
- I could not open decision "451.14" (2014) itself, so I could not check its exact wording.
- Prices were transcribed by OCR from webp images. The figures were consistent across two passes, and T5 matches the user's bill, but a visual check of the image is still advisable.

## 2. Is "facturation sélective" above 150 kWh correct?

### Takeaway
Yes. Official 2026 grids label consumption ≤150 kWh/month "Facturation progressive" (block by block) and >150 kWh/month "Facturation sélective". Under selective billing the whole monthly consumption is charged at the price of the tranche reached.

### Cited Findings
- Redal 2026 grid: "Facturation progressive ≤150kWh" covers T1–T2; "Facturation sélective >150kWh" covers T3–T6. — [Redal 2026 PDF](https://www.redal.ma/sites/g/files/dvc3366/files/document/2026/04/Grille%20tarifaire%202026.pdf)
- Amendis Tanger 2026 grid uses the same labels: "Facturation progressive ≤150 KWh" for T1–T2 and "Facturation sélective >150kWh" for T3–T6. — [Amendis Tanger 2026 grid](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/electricit%C3%A9.png.webp?itok=Kpa7Uw_7)
- Kherba.com, a non-official aggregator, claims that above 150 kWh each tranche is billed at its own price "sans pénalisation rétroactive". This contradicts the official "sélective" labelling. The same page also still cites "TVA 18%", so it is out of date and should not be relied on. — [kherba.com/tarifs](https://kherba.com/tarifs)
- The Conseil de la concurrence's 2024 opinion refers to protecting consumers below 150 kWh/month (tranches 1–2). — [Conseil de la concurrence, Avis A/1/24](https://conseil-concurrence.ma/wp-content/uploads/2024/04/AVIS-A-1-24-FR-WEB.pdf)

### Inferences
- With selective billing, a villa drawing about 520 kWh/month pays 520 × 1.5272 HT. At 500 kWh it would pay 500 × 1.3172. The jump at each threshold (150/210/310/510) is large. The marginal value of solar self-consumption is therefore highest when it pulls consumption below a threshold, and the sizing model should keep this step behaviour.

### Gaps
- None material.

## 3. Fixed charge (redevance fixe) of 39.77 DH HT/month: what is it based on?

### Takeaway
Confirmed. 39.77 DH HT/month is the Amendis Tanger 2026 fixed charge for a **single-phase (2-wire) meter rated 15–25 A**. The charge depends on the number of wires (single- or three-phase) and the meter rating ("calibre").

### Cited Findings
- Tangier "Redevance fixe Basse tension" 2026, as transcribed. Some labels look garbled; see the Gaps — [Amendis Tanger 2026 grid](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/electricit%C3%A9.png.webp?itok=Kpa7Uw_7):
  - 2 wires, 5–10 A: 24.32
  - **2 wires, 15–25 A: 39.77**
  - 2 wires, 30–50 A: 49.60
  - 2 wires, 60–120 A: 49.60 (the duplicate value is suspicious)
  - "5–10 A": 53.68 (probably 4 wires, 5–10 A)
  - 4 wires, 15–25 A: 80.52
  - 4 wires, 30–50 A: 110.58
  - 4 wires, 60–120 A: 161.03
- Amendis describes the fixed charges as covering meter rental and maintenance, connection upkeep, meter reading and billing, and says they are payable whatever the consumption. — [Amendis – Consommations et factures](https://www.amendis.ma/fr/nos-activites/relation-client/client-particulier/consommations-factures)
- For comparison, the Tétouan 2026 fixed charges are: 2 wires 5–10 A 28.45; 15–20 A 39.83; ≥25 A 49.60; 4 wires 5–10 A 51.85; 15–20 A 83.20; 25–50 A 117.02; ≥60 A 158.78. — [Amendis Tétouan 2026 grid](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/%C3%A9lectricit%C3%A9.png.webp?itok=G3Xt3hxo)

### Inferences
- A villa with a three-phase supply would pay 80.52–161.03 DH HT/month, not 39.77. The study should confirm from the bill that the meter is single-phase 15–25 A.
- Derived: 39.77 HT × 1.20 = 47.72 TTC.
- Under the Amendis rule, the fixed charge is prorated by days billed when the period is shorter than 30 days (see section 6).

### Gaps
- The OCR of the fixed-charge rows had label defects (a repeated 49.60, and a missing "4 fils" label on the 53.68 row). Check against the image or the bill.
- I did not confirm whether the VAT on the meter-rental part follows a separate schedule. One secondary source says electricity meter rental went 7% → 11% → 15% → 20% by 2026 ([Upsilon Consulting](https://www.upsilon-consulting.com/reforme-tva-maroc-2024-2026/)). Either way the rate is 20% in 2026.

## 4. TPPAN: still in force in 2026?

### Takeaway
Yes, TPPAN still exists in 2026 and still applies only above 200 kWh/month. I could not confirm the exact formula, min(100, 25 + 0.20×(C−200)) DH, from a primary source within this session.

### Cited Findings
- Amendis (current page) lists among the taxes collected for the State: "la Taxe pour la Promotion du Paysage Audiovisuel National (TPPAN), en cas de consommation mensuelle supérieure à 200 kWh, de la TVA et des frais de timbres". — [Amendis – Consommations et factures](https://www.amendis.ma/fr/nos-activites/relation-client/client-particulier/consommations-factures)
- The Ministry of Finance's 2026 report on public enterprises refers to TPPAN "collectée par l'ONEE, les Régies de Distribution opérationnelles à date et les SRM", so it is still collected in 2026 and was carried over into the SRMs. — [MEF – Rapport EEP (PLF 2026)](https://www.finances.gov.ma/Publication/db/2026/Rapport-etablissements-entreprises-publics_Fr.pdf)
- The Cour des comptes report on the national audiovisual landscape covers TPPAN collection by the distributors. — [Cour des comptes – Paysage audiovisuel national](https://www.courdescomptes.ma/wp-content/uploads/2023/01/Paysage-Audiovisuel-National.pdf)

### Inferences
- The 200 kWh threshold in the study matches Amendis. Nothing suggests TPPAN was abolished or changed in 2025–2026.

### Gaps
- I did not retrieve the BO 4391 bis (1996) text or any later amendment giving the 25 DH base, the 0.20 DH/kWh rate and the 100 DH cap. Treat the formula as plausible but unverified here, and cross-check it against the TPPAN line on an actual Amendis bill above 200 kWh.

## 5. VAT on electricity at 20% from January 2026

### Takeaway
Confirmed. The 2024 Finance Law raised VAT on electricity from 14% to 16% (2024), 18% (2025) and 20% (January 2026). The study's bill (1.3172 HT → 1.5806 TTC) matches 20% exactly.

### Cited Findings
- "la TVA sur l'électricité va passer de 14% à 16% dès ce mois de janvier 2024. Deux points seront respectivement rajoutés, en janvier 2025 et en janvier 2026, pour que le taux … se retrouve porté à 20%." — [Le360, Jan 2024](https://fr.le360.ma/societe/hausse-de-la-tva-sur-les-factures-deau-et-delectricite-ce-qui-va-changer-dans-vos-montants-mensuels_BKIJGJTLDVBMVFWFDLURFXLB74/)
- A secondary summary gives conventional electrical energy 14% → 20% (16 → 18 → 20) and electricity meter rental 7% → 20% (11 → 15 → 20). Since 1 January 2026 Morocco has only two VAT rates, 20% and 10%. — [Upsilon Consulting](https://www.upsilon-consulting.com/reforme-tva-maroc-2024-2026/)
- The CGI 2026 edition (Finance Law 50-25) is the official consolidated text. — [MEF – CGI 2026 (PDF)](https://www.finances.gov.ma/Publication/dgi/2025/CGI-2026-FR.pdf)
- Le360 also reports that water-related meter rental by the delegated manager became VAT-exempt. That concerns water, not electricity. — [Le360](https://fr.le360.ma/societe/hausse-de-la-tva-sur-les-factures-deau-et-delectricite-ce-qui-va-changer-dans-vos-montants-mensuels_BKIJGJTLDVBMVFWFDLURFXLB74/)

### Inferences
- Use a 20% VAT rate on both the energy charge and the electricity fixed charge in 2026.

### Gaps
- I did not open and quote the exact CGI 2026 article.

## 6. How Amendis prorates tranches when the reading period is not 30 days

### Takeaway
Amendis bills on a 30-day monthly basis. If the period is **shorter** than 30 days, the tranches are **not** resized; only the fixed charge is prorated by days. If the reading period runs **longer** than 30 days, the tranche limits **are** resized, with rounding to the unit in the customer's favour.

### Cited Findings
- Quoted from the Amendis Guide pratique du Client: "La facturation de la consommation est effectuée par période mensuelle de 30 jours. Pour une période inférieure à 30 jours : la facturation de la consommation s'effectue sans redimensionnement des tranches … ; la facturation de la redevance fixe s'effectue avec redimensionnement au prorata du nombre de jours facturés. Un dérapage du délai de lecture de plus de 30 jours donne lieu à un redimensionnement des tranches de facturation qui devra se faire en tenant compte d'un arrondi à l'unité en faveur de l'abonné." — [Amendis – Guide pratique du Client (Tétouan edition, 2018, PDF)](https://www.amendis.ma/sites/g/files/dvc3316/files/document/2018/09/KIT_client_VF_Tetouan_final.pdf)

### Inferences
- Example for a 35-day period: the 510 kWh limit becomes about 510 × 35/30 = 595 kWh, and the T5 limit rounds in the customer's favour. A model using calendar months of 28–31 days, or bills covering more than 30 days, should apply this scaling rather than fixed 150/210/310/510 limits.

### Gaps
- The guide is the 2018 Tétouan edition. I found no 2025–2026 document confirming that the rule is unchanged for Tangier under SRM-TTA, though nothing suggests it changed.

## 7. Is there a time-of-use (day/night) option for BT residential customers?

### Takeaway
Not on the Amendis Tangier BT grid. The published 2026 Tangier BT table has no bi-hourly domestic option; time-of-use rates appear only under Moyenne Tension. ONEE (and some régies) offer a BT bi-hourly option restricted to high consumers.

### Cited Findings
- The Amendis Tanger 2026 grid shows hourly rates (Pointe 1.28394, Pleines 0.96739, Creuses 0.75277, outside the TFZ) only under "MOYENNE TENSION". The BT section has only tranche prices and fixed charges. — [Amendis Tanger 2026 grid](https://www.amendis.ma/sites/g/files/dvc3316/files/styles/default/public/image/2026/06/electricit%C3%A9.png.webp?itok=Kpa7Uw_7)
- The Redal 2026 grid does include a time-of-use block: Heures pleines 0.92034, pointe 1.28408, creuses 0.64734, with a fixed charge of 36.15970 DH/kVA/month. — [Redal 2026 PDF](https://www.redal.ma/sites/g/files/dvc3366/files/document/2026/04/Grille%20tarifaire%202026.pdf)
- ONEE bi-hourly BT eligibility, as summarised by an aggregator: BT customer not on prepayment ("Nour"); domestic, industrial or agricultural use; average consumption >500 kWh/month (existing customers) or subscribed power >26 kVA (new customers). — [kherba.com/tarifs](https://kherba.com/tarifs). RADEEJ's tariff PDF likewise lists a "Tarif bihoraire" for consumption >500 kWh/month. — [RADEEJ tarif PDF](https://radeej.ma/assets/espace%20client/elec%20tarif.pdf)

### Inferences
- For the Tangier villa, plan on the selective tranche tariff only. A time-of-use option for BT domestic customers at Amendis or SRM-TTA is not documented online. It may exist on request for customers above 500 kWh, but this is unconfirmed.

### Gaps
- I found no Amendis or SRM-TTA document on a BT bi-hourly option. Ask an agency directly.

## 8. ANRE tariff reform planned for 1 March 2027: what is planned, and any update?

### Takeaway
The ANRE has launched a complete overhaul of tariff methodology for March 2027. The stated principles are cost-reflective prices, a possible regional (per-SRM) or national tariff, time-of-day and seasonal modulation, and two-part (capacity plus energy) tariffs. The tender documents published so far concern mainly **network-use tariffs** (TURT, TSS, MV TURD) and surplus-energy and distribution-contribution tariffs. **No new residential tranche grid has been published**, and no public source announces the end of selective billing. The consultant's deliverable is due about 10 months after December 2025, i.e. around late 2026.

### Cited Findings
- On 12 December 2025 ANRE awarded a contract for technical support on reforming electricity tariffs "à l'horizon de mars 2027". Its principle is "mettre en place des signaux tarifaires qui reflètent la réalité des coûts du système électrique". The specification (CPS) covers TURT (transport), TSS (system services), TURD (MV distribution), TEX (surplus energy under laws 13-09 and 82-21) and the CSD for self-producers. It also asks for options on TURD per SRM versus a single national tariff, nodal or zonal differentiation, "horosaisonnières" modulations and "tarifs binômes". The mission lasts 10 months (to about end-2026), with implementation "dès mars 2027". — [Médias24, 22 Dec 2025](https://medias24.com/2025/12/22/reforme-de-la-tarification-de-lelectricite-de-lanre-vers-une-hausse-des-tarifs-en-2027-1601033/)
- Same article: the 2022 average cost price was 1.21 DH/kWh against an average sale price of 0.94 DH/kWh, and the last tariff revision was in 2015. The author's own view is that "les tarifs vont sûrement devoir augmenter". — [Médias24](https://medias24.com/2025/12/22/reforme-de-la-tarification-de-lelectricite-de-lanre-vers-une-hausse-des-tarifs-en-2027-1601033/)
- Maroc Diplomatique (23 Dec 2025): the reform will apply from 1 March 2027 and aims for "vérité des prix". It will bring upward revisions for categories whose tariffs are furthest from cost. The government expects stability for low-consumption households, and ANRE stresses social-protection mechanisms. No figures are given. — [Maroc Diplomatique](https://maroc-diplomatique.net/factures-delectricite-qui-paiera-plus-des-2027/)
- On 19 February 2026, ANRE decision n°04/26 set the surplus-energy tariff for 1 March 2026 to 28 February 2027 at **0.21 DH/kWh in peak hours and 0.18 DH/kWh off-peak**, for HV, EHV and MV networks. "Le tarif applicable au réseau de la basse tension sera fixé par l'ANRE après la mise en place du cadre réglementaire et technique adéquat." — [ANRE, 19/02/2026](https://anre.ma/actualites/lanre-fixe-le-tarif-de-lexcedent-de-lenergie-electrique-pour-la-periode-de-regulation-allant-du-1er-mars-2026-au-28-fevrier-2027/)
- Hespress notes that ANRE launched the overhaul at the end of 2025. — [Hespress FR](https://fr.hespress.com/484689-pourquoi-les-partis-marocains-ne-parlent-ils-pas-denergie.html)

### Inferences
- For the solar study, the tariff after March 2027 is uncertain, with a risk of increases for large consumers. A villa in T5–T6 is a large residential consumer, so higher future prices would improve the case for solar. The study should present this as a scenario, not a fact.
- No BT surplus buy-back tariff exists as of November 2026. A residential system in Tangier should be sized for self-consumption, with export valued at 0 or treated as unregulated.

### Gaps
- I could not access the Le Matin article of 18 December 2025 that the study cites.
- I found no official ANRE publication after February 2026 giving the content of the retail BT reform: no draft grid, no consultation results, no decision. Recent news in November 2026 mentions a new government and a renamed "ministère de l'Énergie", but I found no tariff announcement linked to it.

## 9. Announced tariff increases for 2026–2027

### Takeaway
The only 2026 change I could confirm for households is the January 2026 VAT step to 20%, together with each distributor's 1 January 2026 grid. I found no official announcement of a BT residential price increase for 2026. Any 2027 change depends on the ANRE reform, for which no figures have been published.

### Cited Findings
- Amendis and Redal both publish grids "en vigueur à partir du 01/01/2026". — [Amendis](https://www.amendis.ma/fr/nos-activites/relation-client/client-particulier/consommations-factures); [Redal 2026 PDF](https://www.redal.ma/sites/g/files/dvc3366/files/document/2026/04/Grille%20tarifaire%202026.pdf)
- An industrial-tariff aggregator says the national grid has not changed since 2015 and that ANRE is preparing an overhaul for March 2027. — [kherba.com – prix industrie](https://kherba.com/electricite/prix-industrie)
- SRM Tanger-Tétouan-Al Hoceïma (SRM-TTA) officially started distribution on 1 September 2025, taking over from the delegated operators, Amendis among them. — [Le Matin](https://lematin.ma/regions/lancement-officiel-de-la-srm-tanger-tetouan-al-hoceima/299637); [SRM-TTA](https://srm-tta.ma/)

### Inferences
- The 2026 Amendis Tangier grid differs from the study's Redal-2023 × 1.0492 scaling. I cannot tell from the sources whether these figures reflect a new 2026 price change or the indexation that has been applied in the past. Use the published 2026 values directly rather than any scaling.
- Since SRM-TTA has taken over, future grids may be published by SRM-TTA rather than Amendis. Watch srm-tta.ma.

### Gaps
- I did not find the 2025 Amendis Tangier grid, so the 2025→2026 change cannot be measured.
- I found no reliable source for a "2.5% increase on 1 August". That snippet appears to come from foreign (French or Belgian) news shared on Facebook and is not about Morocco.
