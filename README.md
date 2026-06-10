# SCM Assistant — Supply Chain Chatbot

## Public Chatbot URL
[https://cloud.flowiseai.com/chatbot/[YOUR-ID-HERE]](https://cloud.flowiseai.com/chatbot/03bbee71-7ae5-4765-a212-3bd178a75a30)

## Tech Stack
- **LLM:** gemini-2.5-flash
- **Embeddings:** HuggingFace Inference 
- **Vector Store:** Qdrant
- **Framework:** Flowise Cloud

## Chunk Configurations Tested

### Config 1 
- Chunk Size: 1000 | Overlap: 100
- PDF chunks: [19] | CSV chunks: [2000]

### Config 2 (Experimental)
- Chunk Size: 500 | Overlap: 100

- Result: Smaller chunks improved precision on policy section references
  but reduced context for multi-row CSV queries.

## Q&A Results

**Q1:** Which Tier-3 suppliers have an active disruption flag...?
**A1:** The following Tier-3 suppliers have an active disruption flag, and the corresponding response levels are detailed below:
1. Maghreb Castworks (SUP-080)
PO-10312 (SKU-MC-1053):
Active Disruption: Regulatory enforcement pending
Risk Level: High
Response Level: Level 3 — Activate.
Rationale: This supplier is classified as High Risk with an active disruption flag. Additionally, "Regulatory enforcement actions" are explicitly listed as a disruption category requiring a mandatory Level 3 response regardless of risk level (Doc 0).
Actions: Immediate escalation to CPO. Alternate supplier activated for minimum 40% of volume within 10 business days. Safety stock adjusted by +50%. Full RCA required within 15 business days (Doc 0).
PO-10196 (SKU-MC-1034):
Active Disruption: Regulatory enforcement pending
Risk Level: High
Response Level: Level 3 — Activate.
Rationale: This supplier is classified as High Risk with an active disruption flag. Additionally, "Regulatory enforcement actions" are explicitly listed as a disruption category requiring a mandatory Level 3 response regardless of risk level (Doc 0).
Actions: Immediate escalation to CPO. Alternate supplier activated for minimum 40% of volume within 10 business days. Safety stock adjusted by +50%. Full RCA required within 15 business days (Doc 0).
2. Bohai Electronics (SUP-010)
PO-10126 (SKU-EC-1020):
Active Disruption: Regulatory enforcement pending
Risk Level: High
Response Level: Level 3 — Activate.
Rationale: This supplier is classified as High Risk with an active disruption flag. Additionally, "Regulatory enforcement actions" are explicitly listed as a disruption category requiring a mandatory Level 3 response regardless of risk level (Doc 0).
Actions: Immediate escalation to CPO. Alternate supplier activated for minimum 40% of volume within 10 business days. Safety stock adjusted by +50%. Full RCA required within 15 business days (Doc 0).
PO-10590 (SKU-EC-1084):
Active Disruption: Tariff adjustment pending
Risk Level: Medium
Response Level: Level 2 — Manage.
Rationale: This supplier is classified as Medium Risk with an active disruption flag (Doc 0).
Actions: Bi-weekly escalation calls. Safety stock adjusted by +30%. Alternate supplier placed on 48-hour readiness notice (Doc 0).
PO-11750 (SKU-EC-1244):
Active Disruption: Typhoon season disruption
Risk Level: High
Response Level: Level 3 — Activate.
Rationale: This supplier is classified as High Risk with an active disruption flag (Doc 0).
Actions: Immediate escalation to CPO. Alternate supplier activated for minimum 40% of volume within 10 business days. Safety stock adjusted by +50%. Full RCA required within 15 business days (Doc 0).
PO-10358 (SKU-EC-1052):
Active Disruption: Geopolitical tension flag
Risk Level: Medium
Response Level: Level 2 — Manage.
Rationale: This supplier is classified as Medium Risk with an active disruption flag (Doc 0).
Actions: Bi-weekly escalation calls. Safety stock adjusted by +30%. Alternate supplier placed on 48-hour readiness notice (Doc 0).
PO-10010 (SKU-EC-1004):
Active Disruption: Typhoon season disruption
Risk Level: High
Response Level: Level 3 — Activate.
Rationale: This supplier is classified as High Risk with an active disruption flag (Doc 0).
Actions: Immediate escalation to CPO. Alternate supplier activated for minimum 40% of volume within 10 business days. Safety stock adjusted by +50%. Full RCA required within 15 business days (Doc 0).
Policy Citation: The disruption response procedures are outlined in Section 9, "Disruption Response Procedures," of the governance policy (Doc 0). Risk level definitions are found in Section 5.1, "Risk Level Definitions" (Doc 1).


**Q2:** Which suppliers qualify for the annual Volume Rebate Program...?
**A2:** To qualify for the annual Volume Rebate Program, a supplier must meet the following criteria as per Section 4.2 of the governance policy:
Be a Tier-1 supplier.
Achieve an OTD Rate at or above 93.0%.
Maintain a Defect Rate below 0.5%.
Have a Sustainability Score at or above 85.
These metrics must be maintained "for a full calendar year". Since the provided data consists of individual Purchase Order (PO) records, each with its own performance metrics, we will assess if any single PO record for a Tier-1 supplier meets all the specified criteria. If no single PO record meets all criteria, then based on the available data, no supplier can be confirmed to qualify for the annual rebate.
First, let's identify all Tier-1 suppliers from the provided context:
Cascade Pack Corp (SUP-107)
Orrentek Precision Mfg (SUP-001)
Rheinwerk Precision AG (SUP-047)
Crestline Chemical Supply (SUP-102)
Toreval Electronics (SUP-051)
Now, let's evaluate each of these Tier-1 suppliers against the OTD, Defect Rate, and Sustainability Score criteria using their individual PO records:
Cascade Pack Corp (SUP-107)
PO-11035: OTD: 88.5% (Fail - below 93.0%), Defect: 0.7% (Fail - not below 0.5%), Sustainability: 98%
PO-11963: OTD: 93.6%, Defect: 1.49% (Fail - not below 0.5%), Sustainability: 75% (Fail - below 85)
PO-10803: OTD: 93.6%, Defect: 1.25% (Fail - not below 0.5%), Sustainability: 76% (Fail - below 85)
PO-11267: OTD: 94.6%, Defect: 1.06% (Fail - not below 0.5%), Sustainability: 76% (Fail - below 85)
PO-10571: OTD: 98.2%, Defect: 0.47%, Sustainability: 70% (Fail - below 85)
PO-11615: OTD: 94.4%, Defect: 1.52% (Fail - not below 0.5%), Sustainability: 84% (Fail - below 85)
PO-11499: OTD: 90.9% (Fail - below 93.0%), Defect: 0.7% (Fail - not below 0.5%), Sustainability: 97%
PO-10455: OTD: 92.8% (Fail - below 93.0%), Defect: 1.47% (Fail - not below 0.5%), Sustainability: 92%
PO-10107: OTD: 90.1% (Fail - below 93.0%), Defect: 1.28% (Fail - not below 0.5%), Sustainability: 95%
Result for Cascade Pack Corp: Does not qualify.
Orrentek Precision Mfg (SUP-001)
PO-11045: OTD: 96.4%, Defect: 1.35% (Fail - not below 0.5%), Sustainability: 86%
Result for Orrentek Precision Mfg: Does not qualify.
Rheinwerk Precision AG (SUP-047)
PO-10743: OTD: 88.2% (Fail - below 93.0%), Defect: 1.62% (Fail - not below 0.5%), Sustainability: 96%
PO-10163: OTD: 97.9%, Defect: 0.35%, Sustainability: 71% (Fail - below 85)
Result for Rheinwerk Precision AG: Does not qualify.
Crestline Chemical Supply (SUP-102)
PO-10798: OTD: 93.8%, Defect: 1.56% (Fail - not below 0.5%), Sustainability: 81% (Fail - below 85)
Result for Crestline Chemical Supply: Does not qualify.
Toreval Electronics (SUP-051)
PO-10631: OTD: 97.1%, Defect: 1.67% (Fail - not below 0.5%), Sustainability: 75% (Fail - below 85)
Result for Toreval Electronics: Does not qualify.
Based on the provided supplier performance data and the criteria outlined in Section 4.2 of the governance policy, no suppliers qualify for the annual Volume Rebate Program. There are 0 qualifying suppliers.


**Q3:** Which region has the highest total PO value...?
**A3:** Based on the provided supplier performance data:
1. Region with the highest total PO value:
Let's calculate the total PO value for each region:
APAC (Asia-Pacific):
Seoultech Micro: $155,685.58 + $124,070.05 = $279,755.63
Wanlong Composites Ltd: $266,371.16 + $231,272.10 + $294,128.68 + $284,868.72 + $556,714.06 + $932,066.26 + $440,127.55 + $826,522.88 + $22,778.00 + $189,991.56 + $330,630.15 + $750,364.16 + $109,598.16 + $67,117.05 = $5,307,052.43
Osaka Polymer Systems: $26,156.90 + $74,369.82 = $100,526.72
Kinki Precision Corp: $62,403.60 + $30,874.97 + $23,702.12 + $59,836.52 = $176,817.21
Dravex Components India: $113,453.68 + $172,676.40 = $286,130.08
Zhenlong ElectroCo: $231,215.55
Archipelago PCB Corp: $258,844.95
ChaoPhaya Pack: $22,113.00
Deccan Polymer Mfg: $369,997.35
Sibertek Molding: $271,397.28 + $179,592.42 + $273,315.21 = $724,304.91
Bohai Electronics: $268,621.92
Busan Pack Corp: $11,731.58 Total APAC PO Value: $8,000,409.58
EMEA (Europe, Middle East, Africa):
Helios Pack Greece: $31,598.92 + $49,235.36 + $168,904.85 = $249,739.13
Varna Electronics EAD: $313,486.34
Solveig Eco Packaging: $12,003.57 + $27,825.60 + $13,205.60 + $14,160.25 = $67,195.02 Total EMEA PO Value: $630,420.49
LATAM (Latin America):
Lima Polymer SA: $463,438.29 + $1,176,649.50 + $468,187.65 + $267,387.86 + $145,617.75 = $2,521,281.05
Santiago Pack Corp: $22,958.54 Total LATAM PO Value: $2,544,239.59
NA (North America):
Ohio Valley Electronics: $174,821.49 + $94,562.67 = $269,384.16
Cascade Pack Corp: $14,893.20 Total NA PO Value: $284,277.36
Comparing the regional totals:
APAC: $8,000,409.58
EMEA: $630,420.49
LATAM: $2,544,239.59
NA: $284,277.36
The region with the highest total PO value is APAC, with a total of $8,000,409.58.
2. Does it breach the concentration limit?
The governance policy PDF is the authoritative source for concentration limits. However, the specific concentration limit value from the policy PDF is not provided in the retrieved context. Therefore, it is not possible to determine if the total PO value for APAC breaches the concentration limit.



**Q4:** Which suppliers are on Supplier Watch List (SWL) status...?
**A4:** Based on the retrieved context, suppliers are placed on the Supplier Watch List (SWL) status if their Compliance Score falls below 60 at any audit (Section 3.4).
The following suppliers are on Supplier Watch List (SWL) status:
SUP-080 (Maghreb Castworks):
PO-10196: Compliance Score of 64 (This score is above 60, so this specific PO does not trigger SWL).
PO-10312: Compliance Score of 66 (This score is above 60, so this specific PO does not trigger SWL).
Correction: Upon re-evaluation, none of the provided PO records show a Compliance Score below 60 for any supplier.
Let's re-check all suppliers mentioned in the PO data for a Compliance Score below 60:
SUP-098 (Cobre del Sur SA): Scores are 90, 67, 74, 83, 79, 68, 91, 91, 72, 87. All are 60 or above.
SUP-057 (Norrsken Textiles AB): Scores are 90, 95, 87, 93, 92, 81, 84, 87, 87, 82. All are 60 or above.
SUP-050 (Dresdner Textilwerk): Scores are 75, 88, 75, 89, 70. All are 60 or above.
SUP-063 (Elsinor Pack AS): Scores are 88, 74, 84, 92, 71, 74, 90, 92. All are 60 or above.
SUP-006 (Dongfeng Castings Co): Scores are 85, 68, 83. All are 60 or above.
SUP-062 (Borealis Composites): Scores are 96, 90. All are 60 or above.
SUP-107 (Cascade Pack Corp): Scores are 99, 99. All are 60 or above.
SUP-086 (Tecovar Industrial Textiles): Scores are 92, 82. All are 60 or above.
SUP-047 (Rheinwerk Precision AG): Score is 96. All are 60 or above.
SUP-056 (Solveig Eco Packaging): Score is 96. All are 60 or above.
SUP-048 (Berliner Pack GmbH): Score is 89. All are 60 or above.
SUP-080 (Maghreb Castworks): Scores are 64, 66. All are 60 or above.
Based on the provided supplier performance data, no suppliers are currently on Supplier Watch List (SWL) status as none of their Compliance Scores are below 60.
Restriction for SWL status:
If a supplier were to be placed on SWL status, it would limit new PO issuance to 20% of their prior quarter volume (Section 3.4, Compliance Score Floor).


**Q5:** Which product category has the highest average defect rate...?
**A5:** Based on the provided supplier performance data:
1. Product category with the highest average defect rate:
Let's calculate the average defect rate for each product category:
Packaging Materials (PM)
Defect Rates: 1.25%, 1.47%, 0.44%, 0.5%, 1.28%, 0.47%, 0.8%, 1.3%, 0.55%, 0.7%, 1.49%, 0.99%, 2.69%, 0.37%, 0.43%, 1.06%
Sum of Defect Rates = 1.25 + 1.47 + 0.44 + 0.5 + 1.28 + 0.47 + 0.8 + 1.3 + 0.55 + 0.7 + 1.49 + 0.99 + 2.69 + 0.37 + 0.43 + 1.06 = 17.79
Number of POs = 16
Average Defect Rate (PM) = 17.79 / 16 = 1.11%
Electronic Components (EC)
Defect Rates: 3.41%, 1.44%, 1.04%, 1.06%, 1.65%, 1.67%, 0.86%, 1.05%, 2.15%, 4.16%, 3.9%, 1.45%, 3.44%
Sum of Defect Rates = 3.41 + 1.44 + 1.04 + 1.06 + 1.65 + 1.67 + 0.86 + 1.05 + 2.15 + 4.16 + 3.9 + 1.45 + 3.44 = 27.28
Number of POs = 13
Average Defect Rate (EC) = 27.28 / 13 = 2.10%
Mechanical Components (MC)
Defect Rates: 4.45%, 4.28%, 3.28%, 1.76%, 3.97%, 3.75%, 1.34%, 4.29%, 1.86%, 4.45%
Sum of Defect Rates = 4.45 + 4.28 + 3.28 + 1.76 + 3.97 + 3.75 + 1.34 + 4.29 + 1.86 + 4.45 = 33.43
Number of POs = 10
Average Defect Rate (MC) = 33.43 / 10 = 3.34%
Raw Materials (RM)
Defect Rates: 0.37%, 0.37%, 1.07%, 3.9%
Sum of Defect Rates = 0.37 + 0.37 + 1.07 + 3.9 = 5.71
Number of POs = 4
Average Defect Rate (RM) = 5.71 / 4 = 1.43%
Comparing the average defect rates:
Packaging Materials: 1.11%
Electronic Components: 2.10%
Mechanical Components: 3.34%
Raw Materials: 1.43%
The product category with the highest average defect rate is Mechanical Components (MC) at 3.34%.
2. Does it exceed the Tier-2 limit?
According to the policy (Section 3.2, doc id='1' and Section 2, doc id='0'), the Tier-2 maximum permissible defect rate is 2.50%.
The average defect rate for Mechanical Components is 3.34%.
Since 3.34% is greater than 2.50%, the average defect rate for Mechanical Components exceeds the Tier-2 limit.


## What I'd Improve
- Add a reranker node for better retrieval accuracy on CSV data
- Use persistent vector store (e.g. Pinecone) instead of in-memory
- Add query decomposition for multi-part questions
- Fine-tune chunk overlap specifically for tabular CSV rows
