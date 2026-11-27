# Programma van Eisen – DELTA testopstelling

[← terug naar de README](../README.md)

Dit PvE bevat alleen eisen en keuzes die door de projectleider zijn vastgelegd. Maten die nog bevestigd moeten worden staan apart onder [Aannames en open punten](#aannames-en-open-punten). Elke eis heeft een nummer, zodat je er vanuit andere documenten naar kunt verwijzen (bijv. `PvE.md#alg-01`).

| Versie | Datum | Wijziging |
|---|---|---|
| 0.1 | 27-11-2026 | Eerste versie, samengesteld uit de vastgelegde beslissingen t/m 04-11-2026 |
| 0.2 | 27-11-2026 | Krachtstroom vanaf fase 2 is niet meer vastgelegd; staat nu bij de open punten (voorkeur: eigen 230 V-groep) |

---

## 1. Algemeen

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="alg-01"></a>ALG-01 | De opstelling bestaat uit twee losse, verrijdbare karren: een koelzijde (kar 1) en een serverzijde (kar 2). | – |
| <a id="alg-02"></a>ALG-02 | De karren worden gekoppeld met flexibele leidingen met zelfsluitende quick-connectors, zodat de koelkar los kan staan (bijv. in een klimaatkamer). | – |
| <a id="alg-03"></a>ALG-03 | De koelzijde wordt ontwikkeld door IJskoud; de HvA stuurt IJskoud aan en is het aanspreekpunt. De fysieke serverzijde (koud water → koude lucht → warmtelast) wordt gebouwd door het HvA Maintenance Lab, met ROC-studenten. Lucend maakt de Modelica-simulaties van de opstelling. | – |
| <a id="alg-04"></a>ALG-04 | De warmtelast moet iets boven de koelcapaciteit uit kunnen: koelcapaciteit ca. 2,8 kW, warmtelast 3,0 kW. | 02-11-2026 |
| <a id="alg-05"></a>ALG-05 | Componenten zijn zo natuurgetrouw mogelijk, zodat de opstelling zich gedraagt als een echt datacenter. | – |
| <a id="alg-06"></a>ALG-06 | De opstelling moet de storingen en scenario's uit [hoofdstuk 6](#6-te-simuleren-storingen-en-scenarios) kunnen nabootsen. | – |

## 2. Koelzijde (kar 1 – IJskoud)

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="kz-01"></a>KZ-01 | Koelcapaciteit ca. 2,8 kW (gevolg van de beschikbare compressoren en chillers). | 02-11-2026 |
| <a id="kz-02"></a>KZ-02 | 2 chillers, met per chiller 2 compressoren. | – |
| <a id="kz-03"></a>KZ-03 | Dubbele waterloop, zodat naast mechanische koeling ook dry cooling mogelijk is. | – |
| <a id="kz-04"></a>KZ-04 | De regelaars van de koelzijde worden geleverd door APAC. | – |

## 3. Serverkar (kar 2) – mechanisch

### 3.1 Kar

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="kar-01"></a>KAR-01 | Afmetingen volgens tekening "DATACENTER CAR" ([tekeningen frames](../hardware/karren-frame/tekeningen/)) (T. Pieters, 07-10-2026): 2300 × 980 × 780 mm (l × b × h, incl. wielen), frame 650 mm hoog, kokerprofiel 40 × 40 × 3,2 mm. | 25-10-2026 |
| <a id="kar-02"></a>KAR-02 | De eerdere eis "max. 750 mm breed" is vervallen: 980 mm past door de deur die gebruikt wordt. | 25-10-2026 |
| <a id="kar-03"></a>KAR-03 | De schakelkast moet onder het dek passen: vrije hoogte ca. 570 mm, kast dus max. ca. 500 mm hoog (liever breder dan hoger). | 25-10-2026 |
| <a id="kar-04"></a>KAR-04 | PIR-plaat onder de datacenterzijde van de kar, voor isolatie. | – |
| <a id="kar-05"></a>KAR-05 | De montageplaat E_KAST_PLT op de kar wordt aangepast aan de schakelkast Rittal AX 1094.000 (800 mm breed). | 02-11-2026 |

### 3.2 Indeling serverruimte

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="sr-01"></a>SR-01 | "Box in een box": de ruimte onder de kap is de kamer, met 4 CRAH's, één in elke hoek. | 04-11-2026 (in uitwerking) |
| <a id="sr-02"></a>SR-02 | Daarbinnen een gesloten binnenbox (serverruimte) met twee rekken tegenover elkaar en de koude gang in het midden. De koude gang loopt niet door tot de buitenwand. | 04-11-2026 (in uitwerking) |
| <a id="sr-03"></a>SR-03 | Bakjes zuigen alleen uit de koude gang en blazen in de kamer; de CRAH's zuigen de kamer leeg. | 04-11-2026 (in uitwerking) |
| <a id="sr-04"></a>SR-04 | Bij een koude gang van 300 mm: binnenbox ca. 880 × 600 mm, min. 190 mm tot de CRAH's. | 04-11-2026 |
| <a id="sr-05"></a>SR-05 | Hoogte bij 30 bakjes: 780 (dek) + 100 (vloer) + 15 × 72 + 40 = 2000 mm. De kar kan niet lager (schakelkast). | 04-11-2026 |

### 3.3 Warmtebakje ("nepserver")

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="bak-01"></a>BAK-01 | Vermogen 100 W per bakje. Geen bakjes van 150 W: de 0,50 mm NiCr wordt dan te heet. | 02-11-2026 |
| <a id="bak-02"></a>BAK-02 | NiCr-strip dwars op de luchtstroom. | 04-11-2026 |
| <a id="bak-03"></a>BAK-03 | Afmetingen 500 breed × 200 diep × 60 hoog mm, steek 72 mm in het rek. | 04-11-2026 |
| <a id="bak-04"></a>BAK-04 | 2 ventilatoren 50 × 50 × 15 mm aan de koude kant. | 04-11-2026 |
| <a id="bak-05"></a>BAK-05 | Het bakje schuift op 2 geleiders (L 20 × 20 × 2) en wordt aan de koude kant vastgezet met een flens 580 × 70 mm (2× M5 in de stijlen, 40 mm breed). | 04-11-2026 |
| <a id="bak-06"></a>BAK-06 | Schuimrubber afdichting op de flens (zijkanten en bovenrand). Blindflens op lege plekken. Warme kant vrij. | 04-11-2026 |
| <a id="bak-07"></a>BAK-07 | Geen stekker: de aansluiting in het bakje blijft een porseleinen busklem. | 04-11-2026 |
| <a id="bak-08"></a>BAK-08 | Eén kabel 5G1 per bakje, binnen aan de koude kant via een tule in de flens. Alle kabels als bundel via de koude gang naar de kast, met een lus van ca. 60 cm. | 04-11-2026 |
| <a id="bak-09"></a>BAK-09 | Een bakje wordt verwisseld via de koude gang en de deur van de binnenbox. | 04-11-2026 |
| <a id="bak-10"></a>BAK-10 | Vermogen per bakje terug te regelen met PWM. | 02-11-2026 |

## 4. Serverkar – elektrisch

### 4.1 Voeding en groepen

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="el-01"></a>EL-01 | 3× Mean Well SDR-960-48, elk een eigen groep van 10 bakjes (niet parallel geschakeld). | 02-11-2026 |
| <a id="el-02"></a>EL-02 | Per bakje is in elke fase alles gelijk (draad, MOSFET, zekering, kabel); uitbreiden gaat per groep van 10. | 02-11-2026 |
| <a id="el-03"></a>EL-03 | Elke groep heeft een eigen +48 V (vrijloopdiodes naar de +48 V van de eigen SDR). De drie −48 V zijn verbonden (gemeenschappelijke GND voor de ESP32's via één DDR-15). | 02-11-2026 |
| <a id="el-04"></a>EL-04 | 5 V- en 12 V-converters hangen aan de 48 V. | 15-10-2026 |

### 4.2 Netaansluiting

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="net-01"></a>NET-01 | Fase 1 (1 SDR, 10 bakjes): 230 V, vaste kabel 3 × 1,5 mm² met randaardestekker, kabelwartel als trekontlasting in de schakelkast. | 15-10-2026 |
| <a id="net-05"></a>NET-05 | Op de kar nooit een contactdoos (bussen) als voedingsingang, altijd een inbouwstekker (pennen). | 15-10-2026 |
| <a id="net-06"></a>NET-06 | Werkschakelaar 4-polig rood/geel, vergrendelbaar, van buiten bereikbaar. Door de 4 polen blijft krachtstroom later mogelijk. | 15-10-2026 |
| <a id="net-07"></a>NET-07 | Eén aardlekautomaat (RCBO) per voeding: EMAT 85006005 (1 module breed). | 02-11-2026 |
| <a id="net-08"></a>NET-08 | De netzijde (230 V, en 400 V als het krachtstroom wordt) wordt aangesloten en gekeurd door een bevoegd persoon (NEN 3140). | 15-10-2026 |

### 4.3 Schakelkast

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="sk-01"></a>SK-01 | Rittal AX 1094.000, 800 × 400 × 250 mm, montageplaat 750 × 375 mm. Vervangt de AX 1050.000. | 02-11-2026 |
| <a id="sk-02"></a>SK-02 | Indeling montageplaat: 3 rails boven elkaar, per groep een kolom. Rail 1: RCBO + SDR (+ DDR-15/DDR-60/F11–13). Rail 2: PTFIX +48/−48/+12/−12 + 11 zekeringklemmen. Rij 3: MOSFET-print + ESP32. | 02-11-2026 |
| <a id="sk-03"></a>SK-03 | Ventilatie van de kast is verplicht bij 3 kW: ca. 185 W verlies in de kast, filterventilator ca. 60 m³/h. | 02-11-2026 |

### 4.4 Opbouw in fasen

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="fa-01"></a>FA-01 | Fase 1 = 10 bakjes (1 kW), fase 2 = 20 (2 kW), fase 3 = 30 (3 kW). | 02-11-2026 |
| <a id="fa-02"></a>FA-02 | Fase 1 is geen wegwerpopstelling maar de permanente v0.5. Wat moeilijk te vervangen is (kast, kabelgoten, DIN-rail, doorvoeren, werkschakelaar, 12 V-voeding) wordt nu al gedimensioneerd op 30 bakjes / 3× SDR-960-48. Alleen de aantallen per bakje komen later. | 25-10-2026 |
| <a id="fa-03"></a>FA-03 | Wat later bijbesteld wordt, staat op het tabblad "Fase 2 later bijbestellen" van de [BOM van de serverkar](../hardware/serverkar/bom/). | 25-10-2026 |

## 5. CRAH

| Nr. | Eis | Vastgelegd |
|---|---|---|
| <a id="crah-01"></a>CRAH-01 | 4 CRAH's op de serverkar, één in elke hoek van de kamer. | 04-11-2026 |
| <a id="crah-02"></a>CRAH-02 | Luchtverplaatsing 250 m³/h per CRAH. | – |

## 6. Te simuleren storingen en scenario's

De opstelling moet de volgende situaties kunnen nabootsen of meten:

| Nr. | Scenario |
|---|---|
| <a id="sim-01"></a>SIM-01 | Temperatuur van de waterloop aanpassen |
| <a id="sim-02"></a>SIM-02 | Fout in de waterklep bij een CRAH |
| <a id="sim-03"></a>SIM-03 | Type klep in de CRAH: modulerend (variabel) in plaats van open/dicht |
| <a id="sim-04"></a>SIM-04 | Pendelen van de dry cooler (en onderzoeken waarom) |
| <a id="sim-05"></a>SIM-05 | Luchtfilters van de dry cooler |
| <a id="sim-06"></a>SIM-06 | Filters in de gekoelde waterloop |
| <a id="sim-07"></a>SIM-07 | Floor tiles open of dicht |
| <a id="sim-08"></a>SIM-08 | Wisselende capaciteit van een chiller |
| <a id="sim-09"></a>SIM-09 | Verschillende configuraties van echte datacenters, door meerdere chillers, compressoren en CRAH's |
| <a id="sim-10"></a>SIM-10 | Analysedoel: chiller-setpoints herkennen uit andere data, voor gevallen waarin de fabrikant ze niet deelt |

---

## Aannames en open punten

Deze punten zijn nog **niet** vastgelegd en moeten bevestigd worden:

- Aangenomen maten: CRAH 300 mm dwars (ca. 500 mm langs de kar), verhoogde vloer 100 mm, kapwand 20 mm, wand binnenbox 10 mm, max. hoogte 2000 mm.
- Deurhoogte nameten: de hoogte van 2000 mm bij 30 bakjes is precies de aangenomen grens.
- Koude lucht naar de koude gang via de verhoogde vloer (aanname).
- Krachtstroomaansluiting in het lab: 16 A of 32 A, en 5-polig (met nul)?
- **Netaansluiting serverkar vanaf fase 2 (2–3 SDR's): nog niet besloten.**
  - *Voorkeur:* een eigen 230 V-groep voor de kar, zodat de kar op meer plekken kan draaien. Aandachtspunt: 2 SDR's trekken samen ca. 9 A continu en 3 SDR's ca. 14 A, dagen tot een week lang. De inschakelpieken kunnen een B16-groep laten afslaan. Nog uitzoeken wat de groep en de stekker daarvoor moeten kunnen.
  - *Alternatief:* krachtstroom. Eén rode CEE-inbouwstekker 16 A, 5-polig (3P+N+PE), 400 V, 6h, met kabel 5 × 2,5 mm² (H07RN-F) en een CEE-koppelcontactstop. Verdeling: L1 = SDR A, L2 = SDR B, L3 = SDR C (ca. 5 A per fase), elke SDR op 230 V (fase-nul). Daarvoor eerst controleren of de aansluiting in het lab 16 A of 32 A is, en 5-polig (met nul).
- Netaansluiting van beide karren samen: krachtstroom voor beide karren, of één kar op krachtstroom die een 230 V-aansluiting voor de andere kar biedt? Bij twee 230 V-aansluitingen heeft elke kar een eigen groep nodig.
