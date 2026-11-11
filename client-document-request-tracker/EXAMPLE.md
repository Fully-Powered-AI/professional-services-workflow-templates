# Client document request tracker: an invented example

*Illustrative example with invented data.* The firm, the client, the people, the files and every figure below are invented. The firm is an invented 40-person accounting and advisory practice. Its client, called Client A here, is an invented regional distributor. The engagement manager is waiting on Client A's records for the third quarter of 2026, and the client has just uploaded its first batch. People are named by role. First come the inputs, in full, then the update the capability returned. The update is the recorded run in `trial.md` with a few findings and decisions worded a little more fully for reading; the states, counts and figures are the same.

## The inputs

### 1. Engagement settings

```
Engagement: Quarter-three records, Client A
Client: Client A
Client contact: Finance manager at Client A
Engagement manager: Engagement manager
Check date: Tuesday 10 November 2026
Reply requested by: Friday 13 November 2026
File naming rule: three parts separated by underscores: client code, document, period
```

### 2. Request list

```
item_id,document,period_start,period_end,required,due,expected_total
R01,Operating account bank statement,2026-07-01,2026-07-31,yes,2026-11-06,
R02,Operating account bank statement,2026-08-01,2026-08-31,yes,2026-11-06,
R03,Operating account bank statement,2026-09-01,2026-09-30,yes,2026-11-06,
R04,Payroll register,2026-07-01,2026-07-31,yes,2026-11-06,
R05,Payroll register,2026-08-01,2026-08-31,yes,2026-11-06,
R06,Payroll register,2026-09-01,2026-09-30,yes,2026-11-06,
R07,Receivables aging report,2026-09-30,2026-09-30,yes,2026-11-06,212480.00
R08,Term loan statement,2026-07-01,2026-09-30,yes,2026-11-06,
R09,Trial balance,2026-07-01,2026-09-30,yes,2026-11-06,
R10,Insurance schedule,2026-09-30,2026-09-30,no,2026-11-06,
R11,Fixed asset additions listing,2026-07-01,2026-09-30,yes,2026-11-20,
```

### 3. Delivery log

```
file_id,file_name,received_on,sender,document,period_start,period_end,readable,total_shown,note
F01,ClientA_Bank-operating_2026-07-to-08.pdf,2026-11-03,Client A finance manager,Operating account bank statement,2026-07-01,2026-08-20,yes,,
F02,ClientA_Bank-operating_2026-09.pdf,2026-11-03,Client A finance manager,Operating account bank statement,2026-09-01,2026-09-30,no,,Opens blank after page 1
F03,ClientA_Payroll-register_2026-07.xlsx,2026-11-04,Client A payroll clerk,Payroll register,2026-07-01,2026-07-31,yes,,
F04,ClientA_Payroll-register_2025-08.xlsx,2026-11-04,Client A payroll clerk,Payroll register,2025-08-01,2025-08-31,yes,,
F05,ClientA_Receivables-aging_2026-09-30.pdf,2026-11-05,Client A finance manager,Receivables aging report,2026-09-30,2026-09-30,yes,209330.00,
F06,ClientA_Trial-balance_2026-09.xlsx,2026-11-05,Client A finance manager,Trial balance,2026-07-01,2026-09-30,yes,,
F07,vehicles list final v2.xlsx,2026-11-09,Client A finance manager,Vehicle list,2026-01-01,2026-09-30,yes,,
```

### 4. Client messages

```
Email, Thursday 5 November 2026, from the finance manager at Client A:
Payroll for September is still being closed, so the September register will come on Thursday 12 November. The lender statement for the term loan comes through our bank contact, who I have asked for it. Our year-end is still 31 December.

Call note, Monday 9 November 2026, taken by the engagement manager:
Finance manager says our broker holds the current insurance schedule.
```

### 5. Previous status list

Not supplied. This is the first update.

## The output

**CLIENT DOCUMENT REQUEST TRACKER: Quarter-three records, Client A**

For: Engagement manager. Client: Client A. Check date: Tuesday 10 November 2026. Reply requested by: Friday 13 November 2026.
Supplied: request list (11 rows, 10 required); delivery log (7 files); client messages (2); previous status list (not supplied).

Position: required rows 10: 3 Received, 3 Incomplete, 2 Mentioned only, 2 Missing. Optional rows 1: 0 Received, 0 Incomplete, 1 Mentioned only, 0 Missing. Received means usable files cover the period; it is not a judgment that they are sufficient.

**Request list by document**

*Operating account bank statement*

- R01, 1 to 31 July 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F01. F01 covers 1 July to 20 August 2026.
- R02, 1 to 31 August 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F01. F01 covers 1 to 20 August 2026. Not covered: 21 to 31 August 2026, 11 days. Overdue by 4 days.
- R03, 1 to 30 September 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F02 (not counted: unreadable). F02 arrived Tuesday 3 November 2026; note: "Opens blank after page 1". No usable file for the period. Overdue by 4 days.

*Payroll register*

- R04, 1 to 31 July 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F03. F03 covers 1 to 31 July 2026.
- R05, 1 to 31 August 2026. Required. Due Friday 6 November 2026. Status: Missing. Files: none. No message mentions August. Overdue by 4 days.
- R06, 1 to 30 September 2026. Required. Due Friday 6 November 2026. Status: Mentioned only. Files: none. Email from the finance manager at Client A, Thursday 5 November 2026: the September register will come on Thursday 12 November 2026. Overdue by 4 days.

*Receivables aging report*

- R07, 30 September 2026. Required. Due Friday 6 November 2026. Status: Incomplete. Files: F05. F05 covers 30 September 2026. Total shown 209,330.00; total expected 212,480.00; difference 3,150.00, shown lower. Overdue by 4 days.

*Term loan statement*

- R08, 1 July to 30 September 2026. Required. Due Friday 6 November 2026. Status: Mentioned only. Files: none. Email from the finance manager at Client A, Thursday 5 November 2026: the statement comes through the bank contact, who has been asked; no date given. Overdue by 4 days.

*Trial balance*

- R09, 1 July to 30 September 2026. Required. Due Friday 6 November 2026. Status: Received. Files: F06. F06 covers 1 July to 30 September 2026.

*Insurance schedule*

- R10, 30 September 2026. Optional. Due Friday 6 November 2026. Status: Mentioned only. Files: none. Call note, Monday 9 November 2026, reporting the finance manager: the broker holds the current schedule; no date given. Overdue by 4 days.

*Fixed asset additions listing*

- R11, 1 July to 30 September 2026. Required. Due Friday 20 November 2026. Status: Missing. Files: none. Due in 10 days.

**Received but not requested**

- F07, vehicles list final v2.xlsx, Vehicle list, 1 January to 30 September 2026, received Monday 9 November 2026.

**Files that match no requested row**

- F04, ClientA_Payroll-register_2025-08.xlsx, Payroll register, 1 to 31 August 2025, received Wednesday 4 November 2026. Reason: period shares no day with any requested payroll period.

**File names that break the naming rule**

- F07, vehicles list final v2.xlsx: one part, not three; no underscores.

**Changed since the last update**

- No previous list supplied.

**Follow-up draft (not sent)**

> Thank you for the 7 files received between Tuesday 3 November and Monday 9 November 2026. We are still waiting on the items below:
>
> - Operating account bank statement, 21 to 31 August 2026: the file received covers 1 to 20 August.
> - Operating account bank statement, 1 to 30 September 2026: the file received will not open, please resend.
> - Payroll register, 1 to 31 August 2026: no file received for this period.
> - Payroll register, 1 to 30 September 2026: we understand it will follow on Thursday 12 November.
> - Receivables aging report, 30 September 2026: the file shows a total of 209,330.00 against 212,480.00 expected, a difference of 3,150.00.
> - Term loan statement, 1 July to 30 September 2026: we understand it is being requested through your bank contact.
>
> Please send these items, or let us know of any delay, by Friday 13 November 2026.
>
> [Engagement manager]

**Not in the draft**

- R10: optional row.
- R11: not yet due; due in 10 days.

**For the Engagement manager to decide: 6**

1. Approve, change or hold the follow-up draft.
2. R02: the bank statement for 1 to 20 August 2026 arrived and 21 to 31 August did not. Start on what arrived, or wait for the rest?
3. R07: the receivables aging report shows 209,330.00 against an expected 212,480.00. Start on what arrived, or wait for the rest?
4. R01, R04 and R09 are Received. Are the files sufficient?
5. F04 is a payroll register for August 2025, not requested. Ask the client about it, or set it aside?
6. F07 is a vehicle list, not on the request list. Ask the client about it, or set it aside?

Prepared for the Engagement manager's approval. Nothing has been sent to the client, filed or changed.
