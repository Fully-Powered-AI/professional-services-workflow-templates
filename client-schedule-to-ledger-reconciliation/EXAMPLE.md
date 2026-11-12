# Client schedule to ledger reconciliation: an invented example

*Illustrative example with invented data.* The client, the customers, the people, the documents and the figures below are all invented. Client X is an invented 40-person furniture maker whose accounts are kept by an invented outsourced accounting practice. Its receivables schedule for October does not agree to the trial balance. First come the inputs the practice supplied, in full, then the worksheet the workflow template returned.

## The inputs

### 1. Settings

```
Client: Client X
Subledger: Accounts receivable
Control account: 1200 Trade debtors
Reporting date: 2026-10-31
Period start: 2026-10-01
Files run on: 2026-11-10
Currency: dollars (all amounts)
Subledger opening balance: 41200.00
Subledger closing balance per the subledger report: 56270.00
Ledger opening balance: 41200.00
Tolerance: 0.00
Look for late postings up to: 2026-11-10
Responsible accountant: Responsible accountant
Client contact: Client X finance contact
```

### 2. Trial balance extract

```
As at: 2026-10-31
account_code,account_name,debit,credit
1100,Bank,22140.00,
1200,Trade debtors,53480.00,
2100,Trade creditors,,18760.00
```

### 3. Subledger schedule

```
doc_ref,doc_date,customer,doc_type,amount
INV-3070,2026-10-02,Customer A,invoice,4800.00
INV-3071,2026-10-05,Customer B,invoice,3150.00
RCT-5521,2026-10-08,Customer A,receipt,-6000.00
INV-3077,2026-10-12,Customer D,invoice,6540.00
INV-3080,2026-10-15,Customer C,invoice,2950.00
RCT-5530,2026-10-19,Customer B,receipt,-3150.00
CN-0212,2026-10-21,Customer F,credit note,-720.00
INV-3088,2026-10-27,Customer E,invoice,5100.00
INV-3091,2026-10-30,Customer B,invoice,2400.00
RCT-5540,2026-11-03,Customer C,receipt,-1800.00
```

### 4. Journal detail for the control account

```
journal_id,doc_ref,posting_date,source,description,amount
J-4401,INV-3070,2026-10-02,AR,Sales invoice Customer A,4800.00
J-4402,INV-3071,2026-10-05,AR,Sales invoice Customer B,3150.00
J-4403,RCT-5521,2026-10-08,CB,Receipt Customer A,-6000.00
J-4404,INV-3077,2026-10-12,AR,Sales invoice Customer D,6450.00
J-4405,INV-3080,2026-10-15,AR,Sales invoice Customer C,2950.00
J-4406,RCT-5530,2026-10-19,CB,Receipt Customer B,-3150.00
J-4407,CN-0212,2026-10-21,AR,Credit note Customer F,-720.00
J-4408,MJ-0457,2026-10-28,MJ,Reclass deposit received to receivables,1500.00
J-4409,INV-3088,2026-10-27,AR,Sales invoice Customer E,5100.00
J-4410,RCT-5540,2026-10-30,CB,Receipt Customer C,-1800.00
J-4411,INV-3091,2026-11-02,AR,Sales invoice batch AR-1102 Customer B,2400.00
```

### 5. Last reconciliation and client notes

```
Last reconciliation, at 2026-09-30: subledger 41200.00, ledger 41200.00, difference 0.00, no open items.

Client note received 2026-11-09 from the Client X finance contact: Cash book receipt RCT-5540 from Customer C was entered on 30 October and allocated to the invoice in the subledger on 3 November.
```

## The worksheet

```
CLIENT SCHEDULE TO LEDGER RECONCILIATION: Client X, Accounts receivable to control account 1200 Trade debtors, as at 31 October 2026

Prepared for: Responsible accountant. Files as supplied on 10 November 2026.

1. Source balances
Subledger: opening 41,200.00; 9 lines dated up to 31 October 2026, net 15,070.00; closing 56,270.00. Agrees to the subledger report, 56,270.00. 1 line dated after the reporting date: RCT-5540, 3 November 2026, -1,800.00, left out of the closing balance.
Ledger: opening 41,200.00, which agrees to the last reconciliation; 10 journals posted up to 31 October 2026, net 12,280.00; closing 53,480.00. Agrees to the trial balance, 53,480.00. 1 journal posted after the reporting date: J-4411, 2 November 2026, 2,400.00.
Difference (trial balance minus schedule): -2,790.00.

2. Result
Difference -2,790.00. Explained by timing: -4,200.00 (2 items). Not yet explained: 1,410.00 net (2 items). Remainder after all items: 0.00. Tie-out: -4,200.00 + 1,410.00 + 0.00 = -2,790.00.

3. Proof
Schedule closing balance 56,270.00
Less INV-3091, in the schedule and posted to the ledger after the reporting date: -2,400.00
Less RCT-5540, in the ledger and entered in the subledger after the reporting date: -1,800.00
Add MJ-0457, in the ledger with no schedule line: 1,500.00
Less INV-3077, posted to the ledger 90.00 below the schedule: -90.00
Equals trial balance 53,480.00. Difference to the trial balance: 0.00.

4. Matched
7 documents, same reference and same amount on both sides, net 6,130.00: INV-3070, INV-3071, RCT-5521, INV-3080, RCT-5530, CN-0212, INV-3088.

5. Timing differences (proposed; the responsible accountant confirms each)
T1. INV-3091, Customer B, invoice 2,400.00. Schedule: dated 30 October 2026. Ledger: J-4411 posted 2 November 2026, batch AR-1102. Effect on difference (signed as its effect on trial balance minus schedule): -2,400.00. Client's stated reason: none supplied. Step: ask the Client X finance contact why batch AR-1102 posted after the reporting date, and whether the invoice belongs in October.
T2. RCT-5540, Customer C, receipt -1,800.00. Schedule: dated 3 November 2026. Ledger: J-4410 posted 30 October 2026. Effect on difference (signed as its effect on trial balance minus schedule): -1,800.00. Client's stated reason: the receipt was entered in the cash book on 30 October and allocated in the subledger on 3 November (client note, 9 November 2026, not yet checked to a document). Step: ask for the cash book entry and the bank date of the receipt.

6. Unexplained entries
U1. MJ-0457, manual journal J-4408 posted 28 October 2026, "Reclass deposit received to receivables", 1,500.00. In the ledger only: no schedule line, no other journal, no note. Effect on difference (signed as its effect on trial balance minus schedule): 1,500.00. Step: ask for the journal's support and the customer it relates to.
U2. INV-3077, Customer D, invoice. Schedule 6,540.00; ledger J-4404 6,450.00. Difference 90.00. The two amounts hold the same digits in a different order, which may be a keying slip; this is a hint, not a finding. Effect on difference (signed as its effect on trial balance minus schedule): -90.00. Step: ask for the invoice copy to see which amount is right.

7. Investigation steps in order
1. U1: support for MJ-0457 (largest unexplained amount).
2. U2: invoice copy for INV-3077.
3. T1: reason for the late posting of batch AR-1102.
4. T2: cash book entry and bank date for RCT-5540.

8. Correcting entries that may be needed (none prepared or posted)
If the invoice copy shows 6,540.00, the ledger is 90.00 short on INV-3077; the offsetting account is not known from the files. If MJ-0457 has no support, whether to reverse it is for the responsible accountant to agree with the client. Timing items T1 and T2 need no entry if confirmed.

9. Decisions for the responsible accountant
1. Whether T1 and T2 are accepted as timing.
2. How U1 and U2 are resolved with the client.
3. Whether a correcting entry is agreed for either.

10. Not assessed
All items in the lists supplied were assessed. Items from before the period start (1 October 2026) were not compared, because the opening balances agree to the last reconciliation.

This worksheet shows how Accounts receivable and 1200 Trade debtors differ at 31 October 2026 and what the files say about each item. It does not show that any entry is right, and it gives no audit, tax or assurance opinion. The responsible accountant confirms each explanation. The worksheet changes no records and sends nothing.
```

Every figure traces to the five inputs above. The schedule's nine lines dated up to 31 October net 15,070.00, so 41,200.00 + 15,070.00 = 56,270.00. The ledger's ten journals posted up to 31 October net 12,280.00, so 41,200.00 + 12,280.00 = 53,480.00. The matched seven net 6,130.00, and both sides then add their own items: 6,130.00 + 6,540.00 + 2,400.00 = 15,070.00 and 6,130.00 + 6,450.00 - 1,800.00 + 1,500.00 = 12,280.00.
