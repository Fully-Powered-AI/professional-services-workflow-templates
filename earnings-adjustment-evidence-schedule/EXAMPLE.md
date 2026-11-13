# Quality of earnings adjustment evidence schedule: an invented example

*Illustrative example with invented data.* The businesses, suppliers, customers, people, documents and figures below are all invented. Company K is an invented 70-person maker of shop fittings that is being sold. An invented advisory firm is carrying out financial due diligence for the buyer. Company K's management has proposed six adjustments to its reported EBITDA for the twelve months to 30 September 2026. First come the inputs the deal team supplied, in full, then the schedule the workflow template returned.

## The inputs

### 1. Engagement settings

```
Target: Company K
Test period: 2025-10-01 to 2026-09-30
Look-back period: 2024-10-01 to 2025-09-30
Currency: dollars (all amounts)
Reported EBITDA for the test period per the financial statements: 842600.00
Management's adjusted EBITDA as stated: 975800.00
Tie tolerance: 0.00
One-off categories: non-recurring
Estimate categories: normalisation; pro forma
Files received on: 2026-11-06
Engagement lead: Engagement lead
Finance contact: Company K finance contact
```

### 2. Management's adjustment list

```
adj_ref,description,mgmt_category,amount,entries_cited
A1,Owner-director salary to the cost of a general manager,normalisation,90000.00,P-01;P-02;P-03;P-04
A2,Adviser fees for the settled dispute with a former distributor,non-recurring,18400.00,G-211;G-219;G-230
A3,Office relocation,non-recurring,12500.00,R-301;R-305
A4,Bad debt on Customer Q after it ceased trading,non-recurring,7300.00,B-410
A5,Sale preparation adviser fees,non-recurring,11000.00,C-501;G-230
A6,Insurance proceeds for storm damage,non-recurring,-6000.00,I-601
```

### 3. Ledger detail for the accounts cited

```
entry_id,date,account_code,account_name,counterparty,description,amount
P-91,2024-12-31,6010,Salaries - directors,Owner-director,Owner-director salary Oct to Dec 2024,57500.00
P-92,2025-03-31,6010,Salaries - directors,Owner-director,Owner-director salary Jan to Mar 2025,57500.00
P-93,2025-06-30,6010,Salaries - directors,Owner-director,Owner-director salary Apr to Jun 2025,57500.00
P-94,2025-09-30,6010,Salaries - directors,Owner-director,Owner-director salary Jul to Sep 2025,57500.00
P-01,2025-12-31,6010,Salaries - directors,Owner-director,Owner-director salary Oct to Dec 2025,60000.00
P-02,2026-03-31,6010,Salaries - directors,Owner-director,Owner-director salary Jan to Mar 2026,60000.00
P-03,2026-06-30,6010,Salaries - directors,Owner-director,Owner-director salary Apr to Jun 2026,60000.00
P-04,2026-09-30,6010,Salaries - directors,Owner-director,Owner-director salary Jul to Sep 2026,60000.00
G-150,2025-03-14,6200,Professional fees,Supplier L,Dispute advice,4200.00
G-160,2025-06-30,6200,Professional fees,Supplier R,Annual accounts,5500.00
G-211,2025-11-20,6200,Professional fees,Supplier L,Distributor dispute,9000.00
G-219,2026-01-22,6200,Professional fees,Supplier L,Distributor dispute,6400.00
G-230,2026-03-05,6200,Professional fees,Supplier L,Settlement and sale review,3000.00
G-240,2026-06-30,6200,Professional fees,Supplier R,Annual accounts,5800.00
C-501,2026-08-08,6200,Professional fees,Supplier S,Sale preparation,8000.00
R-301,2026-04-18,6800,Relocation costs,Supplier M,Office removal,7500.00
R-305,2026-04-30,1610,Leasehold improvements,Supplier N,Fit-out of new office,5000.00
B-310,2025-02-10,6400,Bad debts,Customer W,Write-off Customer W,2100.00
B-410,2026-06-12,6400,Bad debts,Customer Q,Write-off Customer Q,7300.00
I-601,2025-09-28,4900,Other income,Insurer V,Storm damage claim,-6000.00
```

### 4. Account map

```
account_code,account_name,statement_line,in_ebitda
1610,Leasehold improvements,Fixed assets,no
4900,Other income,Other income,yes
6010,Salaries - directors,Staff costs,yes
6200,Professional fees,Overheads,yes
6400,Bad debts,Overheads,yes
6800,Relocation costs,Overheads,yes
7100,Depreciation,Depreciation and amortisation,no
```

### 5. Management's explanations (received 2026-11-04)

```
A1. The owner-director drew 240,000 in salary in the year. After the sale a general manager would run the business. We put the cost of that role at 150,000 a year, so the adjustment is 240,000 less 150,000, which is 90,000.

A2. Supplier L's fees for the dispute with our former distributor, which was settled in March 2026. We do not expect another dispute of this kind.

A3. We moved office in April 2026. These are the removal costs and the fit-out of the new premises. This will not happen again.

A4. Customer Q ceased trading in May 2026 owing 7,300. We have never lost a customer balance of this size before.

A5. Fees for getting the business ready for sale: Supplier S's preparation work and Supplier L's review of the sale documents.
```

### 6. Supporting documents index

```
doc_ref,adj_ref,doc_type,doc_date,counterparty,amount,what_it_shows
D-01,A2,invoice,2025-11-18,Supplier L,9000.00,Fees for the distributor dispute Oct to Nov 2025
D-02,A2,invoice,2026-01-20,Supplier L,6400.00,Fees for the distributor dispute Dec 2025 to Jan 2026
D-03,A3,invoice,2026-04-16,Supplier M,7500.00,Office removal
D-04,A3,invoice,2026-04-29,Supplier N,5000.00,Fit-out of the new office
D-05,A4,write-off memo,2026-06-10,Customer Q,7300.00,Balance written off after the customer ceased trading
D-06,A5,invoice,2026-08-06,Supplier S,8000.00,Sale preparation work
D-07,A6,settlement letter,2025-09-20,Insurer V,6000.00,Storm damage claim settled
```

### 7. Earlier questions and answers

```
None. First run.
```

## The schedule

```
QUALITY OF EARNINGS ADJUSTMENT EVIDENCE SCHEDULE: Company K, test period 2025-10-01 to 2026-09-30

Draft for: Engagement lead. Files received 2026-11-06. Currency: dollars. Run: first run.
File checks: None.
This schedule traces Company K management's proposed adjustments to the evidence supplied. It proposes no adjustment, states no adjusted earnings of its own, and gives no valuation and no opinion.

1. Management's bridge (management's figures, as supplied)
Reported EBITDA per the financial statements: 842,600.00
A1, Owner-director salary to the cost of a general manager, normalisation: 90,000.00
A2, Adviser fees for the settled dispute with a former distributor, non-recurring: 18,400.00
A3, Office relocation, non-recurring: 12,500.00
A4, Bad debt on Customer Q after it ceased trading, non-recurring: 7,300.00
A5, Sale preparation adviser fees, non-recurring: 11,000.00
A6, Insurance proceeds for storm damage, non-recurring: -6,000.00
Management's adjustments, total: 133,200.00
Reported EBITDA plus management's adjustments: 975,800.00. Management's adjusted EBITDA as stated: 975,800.00. Agrees.

2. Summary by evidence status
Traced: 1, 7,300.00: A4.
Traced with flags: 1, 12,500.00: A3.
Not traced: 4, 113,400.00 net: A1, A2, A5, A6.
Total: 6, 133,200.00. Agrees to management's total, 133,200.00.
Entries cited by more than one adjustment: G-230, 3,000.00, A2 and A5.

3. Adjustments
A1. Owner-director salary to the cost of a general manager. Category: normalisation. Amount: 90,000.00. Evidence status: Not traced.
Ledger: P-01, 2025-12-31, 6010, Owner-director, 60,000.00; P-02, 2026-03-31, 6010, Owner-director, 60,000.00; P-03, 2026-06-30, 6010, Owner-director, 60,000.00; P-04, 2026-09-30, 6010, Owner-director, 60,000.00. Linked entries in the test period: 240,000.00. Estimate: tied in the calculation.
Calculation: 240,000 less 150,000 (management's explanation); recomputed 90,000.00, agrees; ledger figure 240,000.00 ties to P-01 to P-04; assumptions: 150,000.00 yearly cost of a general manager, no document.
Explanation: supplied 2026-11-04: the owner-director's salary is replaced by management's figure for a general manager after the sale.
Documents: P-01: no document; P-02: no document; P-03: no document; P-04: no document. None indexed.
Look-back: not checked; normalisation is not a one-off category.
Flags: None.
Questions: Q1, Q2, Q3.

A2. Adviser fees for the settled dispute with a former distributor. Category: non-recurring. Amount: 18,400.00. Evidence status: Not traced.
Ledger: G-211, 2025-11-20, 6200, Supplier L, 9,000.00; G-219, 2026-01-22, 6200, Supplier L, 6,400.00; G-230, 2026-03-05, 6200, Supplier L, 3,000.00. Linked entries in the test period: 18,400.00. Ties.
Calculation: Not an estimate.
Explanation: supplied 2026-11-04: Supplier L's fees for a dispute with a former distributor, settled in March 2026; management does not expect another of this kind.
Documents: D-01 matches G-211; D-02 matches G-219; G-230: no document.
Look-back 2024-10-01 to 2025-09-30: same accounts 2 entries, 9,700.00; same counterparty G-150, 2025-03-14, Supplier L, "Dispute advice", 4,200.00.
Flags: Recurs: Supplier L was also paid 4,200.00 in the look-back period (G-150). Overlap: G-230, 3,000.00, is also cited by A5.
Questions: Q4, Q5.

A3. Office relocation. Category: non-recurring. Amount: 12,500.00. Evidence status: Traced with flags.
Ledger: R-301, 2026-04-18, 6800, Supplier M, 7,500.00; R-305, 2026-04-30, 1610, Supplier N, 5,000.00. Linked entries in the test period: 12,500.00. Ties.
Calculation: Not an estimate.
Explanation: supplied 2026-11-04: removal costs and the fit-out of new premises for the April 2026 move; management says it will not happen again.
Documents: D-03 matches R-301; D-04 matches R-305.
Look-back 2024-10-01 to 2025-09-30: same accounts 0 entries, 0.00; same counterparty none.
Flags: Outside EBITDA: R-305, 5,000.00, is in 1610 Leasehold improvements, which the account map marks in_ebitda no.
Questions: Q6.

A4. Bad debt on Customer Q after it ceased trading. Category: non-recurring. Amount: 7,300.00. Evidence status: Traced.
Ledger: B-410, 2026-06-12, 6400, Customer Q, 7,300.00. Linked entries in the test period: 7,300.00. Ties.
Calculation: Not an estimate.
Explanation: supplied 2026-11-04: Customer Q ceased trading in May 2026 owing 7,300; management says it has not lost a customer balance of this size before.
Documents: D-05 matches B-410.
Look-back 2024-10-01 to 2025-09-30: same accounts 1 entry, 2,100.00; same counterparty none.
Flags: None.
Questions: None.

A5. Sale preparation adviser fees. Category: non-recurring. Amount: 11,000.00. Evidence status: Not traced.
Ledger: C-501, 2026-08-08, 6200, Supplier S, 8,000.00; G-230, 2026-03-05, 6200, Supplier L, 3,000.00. Linked entries in the test period: 11,000.00. Ties.
Calculation: Not an estimate.
Explanation: supplied 2026-11-04: Supplier S's preparation work and Supplier L's review of the sale documents.
Documents: D-06 matches C-501; G-230: no document.
Look-back 2024-10-01 to 2025-09-30: same accounts 2 entries, 9,700.00; same counterparty G-150, 2025-03-14, Supplier L, "Dispute advice", 4,200.00.
Flags: Recurs: Supplier L was also paid 4,200.00 in the look-back period (G-150). Overlap: G-230, 3,000.00, is also cited by A2.
Questions: Q4, Q5.

A6. Insurance proceeds for storm damage. Category: non-recurring. Amount: -6,000.00. Evidence status: Not traced.
Ledger: I-601, 2025-09-28, 4900, Insurer V, -6,000.00. Linked entries in the test period: 0.00. Does not tie: difference (adjustment minus linked entries in the test period) -6,000.00. Outside the test period: I-601, 2025-09-28, -6,000.00.
Calculation: Not an estimate.
Explanation: Not supplied.
Documents: D-07 matches I-601.
Look-back 2024-10-01 to 2025-09-30: same accounts 0 entries, 0.00; same counterparty none.
Flags: Outside test period: I-601, -6,000.00, is dated 2025-09-28, before the test period starts on 2025-10-01.
Questions: Q7, Q8.

4. Questions for management (draft; the engagement lead decides which are sent)
Q1. (A1) The calculation uses 150,000.00 as the yearly cost of a general manager. What is that figure based on, and which document supports it?
Q2. (A1) Do the 240,000.00 of salary in P-01 to P-04 and the 150,000.00 both include, or both exclude, employer payroll taxes and benefits?
Q3. (A1) Please supply the payroll records for P-01 to P-04, 60,000.00 each, posted to 6010 Salaries - directors.
Q4. (A2, A5) Please supply the invoice behind G-230, Supplier L, 3,000.00, 2026-03-05, and say how it divides between the distributor dispute (A2) and the sale document review (A5). Both adjustments cite the full 3,000.00.
Q5. (A2, A5) Supplier L was also paid 4,200.00 on 2025-03-14 (G-150, "Dispute advice"). Did that payment relate to the same dispute, another dispute or other work?
Q6. (A3) The fit-out, R-305, Supplier N, 5,000.00, is posted to 1610 Leasehold improvements, which the account map places outside EBITDA. Was this cost charged in arriving at the reported EBITDA of 842,600.00, and if not, why is it in the adjustments?
Q7. (A6) The insurance receipt I-601, Insurer V, -6,000.00, is dated 2025-09-28, before the test period starts on 2025-10-01. Is there an entry in the test period for these proceeds, and if not, why is the deduction made from the test period?
Q8. (A6) Please supply management's explanation for A6.

5. Decisions for the engagement lead
1. Which of management's 6 adjustments the firm accepts, in whole or in part. The evidence status above is not that decision.
2. Which of the questions are sent to management, and in what form.
3. A2 and A5, Recurs: Supplier L was paid 4,200.00 for "Dispute advice" in the look-back period (G-150). Does this bear on whether the A2 and A5 costs are one-off?
4. A2 and A5, Overlap: G-230, 3,000.00, is cited in full by both adjustments. How is it treated until management answers Q4?
5. A3, Outside EBITDA: R-305, 5,000.00, sits in an account the account map places outside EBITDA. Does it belong in the bridge?
6. A6, Outside test period: I-601, -6,000.00, is dated before the test period. Does the deduction belong in this test period?

6. Not assessed
Adjustments management did not propose. Entries management did not cite. Whether any document is genuine: documents were compared from the index on counterparty and amount only. Anything outside the look-back period supplied, 2024-10-01 to 2025-09-30. No check was skipped for a missing input.

Prepared from the files received 2026-11-06 for the Engagement lead's review. It changes no records and sends nothing.
```

Every figure traces to the inputs above. The six adjustments total 90,000.00 + 18,400.00 + 12,500.00 + 7,300.00 + 11,000.00 - 6,000.00 = 133,200.00, and 842,600.00 + 133,200.00 = 975,800.00, the figure management states. A1's ledger figure is 4 × 60,000.00 = 240,000.00, and 240,000.00 - 150,000.00 = 90,000.00. A2's entries add to 9,000.00 + 6,400.00 + 3,000.00 = 18,400.00; A3's to 7,500.00 + 5,000.00 = 12,500.00; A5's to 8,000.00 + 3,000.00 = 11,000.00. The look-back entries in 6200 are G-150 and G-160: 4,200.00 + 5,500.00 = 9,700.00. The Not traced total is 90,000.00 + 18,400.00 + 11,000.00 - 6,000.00 = 113,400.00, and 7,300.00 + 12,500.00 + 113,400.00 = 133,200.00.
