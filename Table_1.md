---
created: 2026-07-03T01:29:12+06:30
modified: 2026-07-03T01:32:59+06:30
---

# Table EWA

# COMPLETE EWA SYSTEM - MASTER DATA DICTIONARY (v2.0)
### All Modules (1–14) | Product-Centric + Service-Type Pricing

| **Module** | **No** | **Name** | **Value (Field Key)** | **Description** |
|------------|--------|----------|----------------------|-----------------|
| **Module 1: Corporate Master & Rule Policy Matrix** | 1 | Corp ID & Name | corpIdName | ကုမ္ပဏီ၏ သီးသန့် ID နှင့် ကုမ္ပဏီအမည် |
| | 2 | Legal Entity & Tax ID | legalEntityTaxId | တရားဝင်မှတ်ပုံတင်ထားသော ကုမ္ပဏီအမည်နှင့် အခွန်မှတ်ပုံတင်နံပါတ် |
| | 3 | Settlement Bank | settlementBank | ငွေပေးချေမှုအတွက် ချိတ်ဆက်ထားသော ဘဏ် |
| | 4 | Acct Manager | acctManager | တာဝန်ခံ Account Manager အမည် |
| | 5 | Approved Credit Limit | approvedCreditLimit | ခွင့်ပြုထားသော စုစုပေါင်း Credit ပမာဏ (MMK) |
| | 6 | Utilized Pool | utilizedPool | လက်ရှိအသုံးပြုထားသော Credit ပမာဏ |
| | 7 | Available Pool | availablePool | ကျန်ရှိ အသုံးပြုနိုင်သော Credit ပမာဏ |
| | 8 | Billing Freq | billingFreq | ငွေတောင်းခံမှုအကြိမ်ရေ (MONTHLY, BI_WEEKLY) |
| | 9 | Payout Day | payoutDay | ဝန်ထမ်းများထံ ငွေထုတ်ပေးမည့်ရက် |
| | 10 | Due Day | dueDay | ကုမ္ပဏီမှ ငွေပြန်ဆပ်ရမည့် နောက်ဆုံးရက် |
| | 11 | Grace Period | gracePeriod | ဒဏ်ကြေးမဲ့ နောက်ကျခွင့်ရက်အရေအတွက် |
| | 12 | Flat Fee | flatFee | ငွေထုတ်ယူမှုတစ်ခုအတွက် အခြေခံကောက်ခံမည့် အခကြေးငွေ (MMK) |
| | 13 | Variable Fee % | variableFeePercent | ငွေထုတ်ယူမှုပမာဏအပေါ် ကောက်ခံမည့် ရာခိုင်နှုန်း |
| | 14 | Base Late Fee % | baseLateFeePercent | သတ်မှတ်ရက်ကျော်လျှင် ကောက်ခံမည့် အခြေခံဒဏ်ကြေးရာခိုင်နှုန်း |
| | 15 | Daily Accrual Type | dailyAccrualType | ဒဏ်ကြေးတွက်ချက်ပုံစနစ် (SIMPLE / COMPOUND) |
| | 16 | EWA Limit Cap | ewaLimitCap | ဝန်ထမ်းတစ်ဦးအတွက် အများဆုံးထုတ်ယူခွင့် ကန့်သတ်ချက် |
| | 17 | Min Tenure | minTenure | EWA တွင်ပါဝင်ခွင့်ရရန် အနည်းဆုံးလုပ်သက်ရက် |
| | 18 | Min Days Worked | minDaysWorked | လက်ရှိလစာကာလအတွင်း အနည်းဆုံးအလုပ်လုပ်ရမည့်ရက် |
| | 19 | Total Roster | totalRoster | ကုမ္ပဏီတွင်ရှိသော စုစုပေါင်းဝန်ထမ်းဦးရေ |
| | 20 | Whitelisted | whitelisted | EWA အတွက် ခွင့်ပြုထားသော ဝန်ထမ်းဦးရေ |
| | 21 | Auto-Approve Limit | autoApproveLimit | အလိုအလျောက်အတည်ပြုနိုင်သည့် အများဆုံးငွေထုတ်ယူပမာဏ |
| | 22 | Risk Score | riskScore | ကုမ္ပဏီ၏ ဘေးအန္တရာယ်အဆင့်သတ်မှတ်ချက် |
| | 23 | Status | status | ကုမ္ပဏီ၏ EWA လုပ်ငန်းအခြေအနေ (ACTIVE, SUSPENDED) |
| | 24 | Last Audit | lastAudit | နောက်ဆုံးစစ်ဆေးခဲ့သည့်ရက်စွဲ |
| | 25 | Max Drawdown Rate | maxDrawdownRate | လစာ၏ ရာခိုင်နှုန်းအလိုက် ထုတ်ယူခွင့်ကန့်သတ်ချက် (%) |
| | 26 | Min Remaining Balance | minRemainingBalance | EWA ထုတ်ယူပြီးနောက် ဝန်ထမ်းလက်ကျန်တွင်ကျန်ရမည့် အနည်းဆုံးလစာပမာဏ |
| | 27 | Corporate Tier | corporateTier | ကုမ္ပဏီအဆင့်သတ်မှတ်ချက် (PREMIUM, STANDARD, BASIC) |
| | 28 | Early Settlement Discount | earlySettlementDiscount | သတ်မှတ်ရက်ထက်စော၍ ဆပ်လျှင် လျှော့ပေါင်းပေးမည့် ရာခိုင်နှုန်း |
| | 29 | Action | action | စီမံခန့်ခွဲမှုလုပ်ဆောင်ချက်ခလုတ် |
| **Module 2: Employee Payroll, Security & Lifecycle Master** | 1 | Emp ID | empId | ဝန်ထမ်း၏ သီးသန့် ID |
| | 2 | Full Name | fullName | ဝန်ထမ်းအမည်အပြည့်အစုံ |
| | 3 | Phone & Email | phoneEmail | ဆက်သွယ်ရန်ဖုန်းနံပါတ်နှင့် အီးမေးလ် |
| | 4 | National ID / Tax ID | nationalIdTaxId | မှတ်ပုံတင်နံပါတ် သို့မဟုတ် အခွန်ထမ်းအမှတ် |
| | 5 | Dept / Title | deptTitle | ဌာန နှင့် ရာထူး |
| | 6 | Corp Ref | corpRef | ဆက်စပ်ကုမ္ပဏီ ID |
| | 7 | Joined Date | joinedDate | အလုပ်စတင်ဝင်ရောက်သည့်ရက်စွဲ |
| | 8 | Base Salary (MMK) | baseSalary | အခြေခံလစာ (ကျပ်) |
| | 9 | Earned Velocity | earnedVelocity | ယခုလက်ရှိကာလအတွင်း ရရှိပြီးသောလစာပမာဏ |
| | 10 | Active Dues | activeDues | လက်ရှိပြန်ဆပ်ရန် ကျန်ရှိသော စုစုပေါင်းကြွေးကျန် |
| | 11 | Max EWA Cap | maxEwaCap | ဝန်ထမ်းတစ်ဦးအတွက် အများဆုံးထုတ်ယူနိုင်သည့်ပမာဏ |
| | 12 | YTD Drawn | ytdDrawn | ယခုနှစ်အတွင်း စုစုပေါင်းထုတ်ယူထားသည့်ပမာဏ |
| | 13 | Target Bank | targetBank | ငွေလွှဲပို့မည့် ဘဏ်အမည် |
| | 14 | Target Wallet/Acc | targetWalletAcc | ငွေလက်ခံမည့် ဘဏ်အကောင့်/ပိုက်ဆံအိတ်နံပါတ် |
| | 15 | L1: KYC | l1Kyc | အဆင့်-၁ ကိုယ်ရေးကိုယ်တာအထောက်အထားအတည်ပြုချက်အခြေအနေ |
| | 16 | L2: Whitelist | l2Whitelist | အဆင့်-၂ EWA ခွင့်ပြုစာရင်းဝင်မဝင် အခြေအနေ |
| | 17 | Lifecycle State | lifecycleState | ဝန်ထမ်း၏ လက်ရှိဘဝစက်ဝန်းအခြေအနေ (ACTIVE, BLACKLIST, RESIGNED) |
| | 18 | Reason | reason | Lifecycle State ပြောင်းလဲရခြင်းအကြောင်းရင်း |
| | 19 | Last HR Sync | lastHrSync | နောက်ဆုံး HR စနစ်နှင့် ဒေတာချိန်ကိုက်ခဲ့သည့်အချိန် |
| | 20 | EWA Usage Frequency | ewaUsageFrequency | လတစ်လအတွင်း EWA ထုတ်ယူအသုံးပြုမှုအကြိမ်ရေ |
| | 21 | Repayment History Score | repaymentHistoryScore | ပြန်ဆပ်မှုသမိုင်းအပေါ် အခြေခံသည့် Credit Score (1-100) |
| | 22 | Is EWA Eligible | isEwaEligible | EWA အတွက် အရည်အချင်းပြည့်မီမီ အခြေအနေ (TRUE/FALSE) |
| | 23 | Eligibility Expiry Date | eligibilityExpiryDate | EWA အရည်အချင်းသက်တမ်းကုန်ဆုံးမည့်ရက်စွဲ |
| | 24 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 3: Corporate Billing Cycle & Period Snapshot Ledger** | 1 | Cycle ID | cycleId | Billing Cycle သီးသန့်အမှတ် |
| | 2 | Corp Ref | corpRef | ဆက်စပ်ကုမ္ပဏီ ID |
| | 3 | Period Start | periodStart | Billing ကာလစတင်ရက်စွဲ |
| | 4 | Period End | periodEnd | Billing ကာလပြီးဆုံးရက်စွဲ |
| | 5 | Cutoff Date | cutoffDate | ငွေထုတ်ယူမှုများရပ်ဆိုင်းမည့်ရက်စွဲ |
| | 6 | Invoice Due Date | invoiceDueDate | ငွေတောင်းခံလွှာပြန်ဆပ်ရမည့် နောက်ဆုံးရက် |
| | 7 | Eligible Roster | eligibleRoster | ဤ Cycle အတွင်း EWA ထုတ်ယူခွင့်ရှိသော ဝန်ထမ်းဦးရေ |
| | 8 | Total EWA Vol | totalEwaVol | ဤ Cycle အတွင်းထုတ်ယူခဲ့သော စုစုပေါင်းငွေပမာဏ |
| | 9 | Service Fees | serviceFees | စုစုပေါင်းကောက်ခံခဲ့သော ဝန်ဆောင်ခ |
| | 10 | Expected Repay | expectedRepay | ပြန်ဆပ်ရန် မျှော်မှန်းထားသော စုစုပေါင်းပမာဏ |
| | 11 | Actual Paid | actualPaid | အမှန်တကယ်ပြန်ဆပ်ပြီးငွေ |
| | 12 | Unpaid Balance | unpaidBalance | မဆပ်ရသေးသော ကျန်ငွေ |
| | 13 | GL Recon | glRecon | စာရင်းညှိနှိုင်းမှုအခြေအနေ (UNRECON, PARTIAL, MATCHED) |
| | 14 | Cycle Status | cycleStatus | Cycle ၏ အခြေအနေ (ACTIVE, PROCESSING, PAST_DUE) |
| | 15 | Created By | createdBy | Cycle ဖန်တီးသူ (SYSTEM/USER) |
| | 16 | Cycle Utilization Rate | cycleUtilizationRate | ခွင့်ပြု Credit ပမာဏနှင့် အသုံးပြုမှုအချိုး (%) |
| | 17 | Average Drawdown Per Emp | avgDrawdownPerEmp | ဝန်ထမ်းတစ်ဦးချင်းစီ၏ ပျှမ်းမျှထုတ်ယူငွေပမာဏ |
| | 18 | Cycle Profitability | cycleProfitability | ဤ Cycle မှရရှိသော အမြတ်ပမာဏ |
| | 19 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 4: Dynamic EWA Request & Disbursal Hub** | 1 | Request ID | requestId | ငွေထုတ်ယူမှုတောင်းဆိုချက်အတွက် သီးသန့် ID |
| | 2 | Emp Ref | empRef | ငွေထုတ်ယူသူ ဝန်ထမ်း ID |
| | 3 | Cycle Ref | cycleRef | ဆိုင်ရာ Billing Cycle ID |
| | 4 | Req Timestamp | reqTimestamp | တောင်းဆိုချိန် ရက်စွဲနှင့်အချိန် |
| | 5 | IP / Device | ipDevice | တောင်းဆိုမှုပြုလုပ်သည့် IP လိပ်စာနှင့် စက်အမျိုးအစား |
| | 6 | Accrued Wages | accruedWages | တောင်းဆိုချိန်အထိ ဝန်ထမ်းရရှိထားသော လုပ်အားခ |
| | 7 | Request Amt | requestAmt | ထုတ်ယူရန်တောင်းဆိုသော ငွေပမာဏ |
| | 8 | Fee Charged | feeCharged | ကောက်ခံလိုက်သော ဝန်ဆောင်ခ |
| | 9 | Total Debit | totalDebit | ဝန်ထမ်းထံမှ ပြန်လည်ဖြတ်တောက်မည့် စုစုပေါင်းငွေ |
| | 10 | Net Disbursed | netDisbursed | ဝန်ထမ်းလက်ထဲသို့ အမှန်တကယ်ရောက်ရှိသောငွေ |
| | 11 | Target Bank | targetBank | ငွေလွှဲပို့မည့် ဘဏ်/ငွေကြေးဝန်ဆောင်မှု |
| | 12 | Remittance Ref | remittanceRef | ငွေလွှဲပြေစာအမှတ် / Bank Reference |
| | 13 | Appvl Channel | appvlChannel | အတည်ပြုသည့်လမ်းကြောင်း (AUTO/MANUAL) |
| | 14 | Status | status | ငွေထုတ်ယူမှု အခြေအနေ (DISBURSED, FAILED, PENDING) |
| | 15 | Error Code | errorCode | ငွေထုတ်ယူမှုပျက်ကွက်ပါက ဖော်ပြသော Error Code |
| | 16 | **Service Type** | **service_type** | **ဤ Transaction ၏ အမျိုးအစား (ပုံသေ: `DISBURSAL`). Fee Engine မှ ဤတန်ဖိုးကို အသုံးပြု၍ သက်ဆိုင်ရာ Fee Rule များကို ရွေးချယ်သည်။** |
| | 17 | Request Approval Time | requestApprovalTime | တောင်းဆိုချိန်မှ အတည်ပြုချိန်အထိ ကြာမြင့်ချိန် (မိနစ်) |
| | 18 | Disbursal Channel | disbursalChannel | ငွေထုတ်ယူသည့်လမ်းကြောင်း (MOBILE_APP, USSD, WEB, ATM) |
| | 19 | Is First Time User | isFirstTimeUser | ပထမဆုံးအကြိမ် EWA ထုတ်ယူသူလား (TRUE/FALSE) |
| | 20 | Promo Code Applied | promoCodeApplied | လျှော့စျေး/ပရိုမိုးရှင်း Code ထည့်သွင်းထားခြင်းရှိမရှိ |
| | 21 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 5: Bulk Repayment & Pro-Rata Allocator Master** | 1 | Batch ID | batchId | ငွေပြန်ဆပ်မှု Batch အမှတ် |
| | 2 | Corp Ref | corpRef | ဆက်စပ်ကုမ္ပဏီ ID |
| | 3 | Cycle Ref | cycleRef | ဆိုင်ရာ Billing Cycle ID |
| | 4 | Settled Date | settledDate | ငွေစာရင်းရှင်းလင်းသည့်ရက်စွဲနှင့်အချိန် |
| | 5 | Bank Slip Ref | bankSlipRef | ဘဏ်ငွေလွှဲပြေစာအမှတ် (File) |
| | 6 | Collection GL | collectionGL | ငွေလက်ခံရာ စာရင်းအကောင့် (GL Code) |
| | 7 | Base Invoice | baseInvoice | မူလငွေတောင်းခံလွှာပမာဏ |
| | 8 | Accrued Late Fees | accruedLateFees | ရက်လွန်ဒဏ်ကြေးစုစုပေါင်း |
| | 9 | Total Invoice | totalInvoice | စုစုပေါင်းတောင်းခံငွေ |
| | 10 | Actual Paid | actualPaid | အမှန်တကယ်ပေးသွင်းငွေ |
| | 11 | Coverage % | coveragePercent | စုစုပေါင်းတောင်းခံငွေအပေါ် ပေးသွင်းမှုရာခိုင်နှုန်း |
| | 12 | Pro-Rata Alloc | proRataAlloc | ဝန်ထမ်းများထံ အချိုးကျခွဲဝေပေးမည့် ပြန်ဆပ်ငွေပမာဏ |
| | 13 | Suspense Amt | suspenseAmt | ပိုလျှံ/လိုငွေ သို့မဟုတ် ခွဲဝေ၍မရသော ငွေပမာဏ |
| | 14 | Recon Status | reconStatus | စာရင်းညှိနှိုင်းမှုအခြေအနေ (MATCHED, PARTIAL, SUSPENSE) |
| | 15 | Maker | maker | ငွေစာရင်းစတင်ဖန်တီးသူ |
| | 16 | Checker | checker | အတည်ပြုသူ |
| | 17 | Repayment Efficiency | repaymentEfficiency | မျှော်မှန်းထားသော ပြန်ဆပ်ငွေနှင့် အမှန်တကယ်ရရှိငွေ အချိုး (%) |
| | 18 | Late Payment Ratio | latePaymentRatio | ဤ Batch အတွင်း ရက်လွန်ပြန်ဆပ်မှုနှုန်း (%) |
| | 19 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 6: Employee End-to-End Ledger History** | 1 | History ID | historyId | Ledger မှတ်တမ်း သီးသန့်အမှတ် |
| | 2 | Cycle Ref | cycleRef | ဆိုင်ရာ Billing Cycle ID |
| | 3 | Emp ID & Name | empIdName | ဝန်ထမ်း ID နှင့် အမည် |
| | 4 | Base Salary | baseSalary | ထိုကာလအတွက် အခြေခံလစာ |
| | 5 | Max Cap | maxCap | အများဆုံးထုတ်ယူနိုင်သည့် ပမာဏကန့်သတ်ချက် |
| | 6 | EWA Drawn | ewaDrawn | ထုတ်ယူသွားသော EWA ငွေပမာဏ |
| | 7 | Service Fee | serviceFee | ကောက်ခံခဲ့သော ဝန်ဆောင်ခ |
| | 8 | Days Late | daysLate | ပြန်ဆပ်ရက်ကျော်လွန်သည့် ရက်အရေအတွက် |
| | 9 | Late Fee Incrd | lateFeeIncrd | ရက်လွန်ဒဏ်ကြေးအဖြစ် တိုးလာသောပမာဏ |
| | 10 | Total Dues | totalDues | ပြန်ဆပ်ရမည့် စုစုပေါင်းကြွေးကျန် |
| | 11 | Bulk Paid (Pro-Rata) | bulkPaidProRata | Bulk Repayment မှ အချိုးကျခွဲဝေရရှိသော ပြန်ဆပ်ငွေ |
| | 12 | Final Repaid | finalRepaid | နောက်ဆုံးပြန်ဆပ်ပြီးငွေ |
| | 13 | Post Bal Left | postBalLeft | ပြန်ဆပ်ပြီးနောက် ကျန်ရှိကြွေးကျန် |
| | 14 | Repayment State | repaymentState | ပြန်ဆပ်မှုအခြေအနေ (FULLY_REPAID, PARTIAL, ARREARS) |
| | 15 | Clear Date | clearDate | ကြွေးကျန်အပြည့်ရှင်းလင်းသည့်ရက်စွဲ |
| | 16 | Lifetime EWA Value | lifetimeEwaValue | ဝန်ထမ်းတစ်ဦး၏ စုစုပေါင်း EWA ထုတ်ယူမှုသမိုင်း |
| | 17 | Average Repayment Days | avgRepaymentDays | ပျှမ်းမျှပြန်ဆပ်သည့်ရက်ကွာဟမှု |
| | 18 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 7: General Ledger (GL) Double-Entry Posting** | 1 | JE ID | jeId | Journal Entry သီးသန့်အမှတ် |
| | 2 | Txn Ref / Batch Ref | txnRefBatchRef | ဆက်စပ် Transaction (သို့) Batch Reference |
| | 3 | Date & Time | dateTime | စာရင်းသွင်းသည့် ရက်စွဲနှင့်အချိန် |
| | 4 | Txn Type | txnType | ငွေကြေးလုပ်ငန်းအမျိုးအစား (DISBURSAL, REPAYMENT, PREPAYMENT, FEE_EARN, PENALTY) |
| | 5 | Debit GL Code | debitGlCode | Debit ဖြစ်သည့် စာရင်းအကောင့်ကုဒ် |
| | 6 | Debit Name | debitName | Debit အကောင့်အမည် |
| | 7 | Credit GL Code | creditGlCode | Credit ဖြစ်သည့် စာရင်းအကောင့်ကုဒ် |
| | 8 | Credit Name | creditName | Credit အကောင့်အမည် |
| | 9 | Currency | currency | ငွေကြေးအမျိုးအစား (MMK) |
| | 10 | Amount | amount | စာရင်းသွင်းငွေပမာဏ |
| | 11 | Description | description | စာရင်းသွင်းခြင်းဆိုင်ရာ ဖော်ပြချက် |
| | 12 | Status | status | GL စာရင်းအခြေအနေ (POSTED, PENDING) |
| | 13 | Maker | maker | စာရင်းစတင်ဖန်တီးသူ |
| | 14 | Checker | checker | စာရင်းအတည်ပြုသူ |
| | 15 | Reconciliation Status | reconciliationStatus | စာရင်းကိုက်ညီမှုအခြေအနေ (RECONCILED, UNRECONCILED, PARTIAL) |
| | 16 | Audit Trail ID | auditTrailId | စာရင်းစစ်ဆေးမှုသမိုင်းခြေရာခံ ID |
| | 17 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 8: Central Notification & Exception Hub** | 1 | Exception ID | exceptionId | ချွင်းချက်ဖြစ်ရပ်၏ သီးသန့်အမှတ် |
| | 2 | Module Origin | moduleOrigin | ဖြစ်ပွားရာ Module အမည်နှင့် လုပ်ဆောင်ချက် |
| | 3 | Target Entity | targetEntity | သက်ရောက်သည့် အဓိကအစိတ်အပိုင်း (Emp ID/Corp ID) |
| | 4 | Severity | severity | ပြင်းထန်မှုအဆင့် (CRITICAL, HIGH, MEDIUM) |
| | 5 | Esc. Level | escLevel | တင်ပြရမည့် စီမံခန့်ခွဲမှုအဆင့် (L1/L2) |
| | 6 | Exception Code | exceptionCode | ချွင်းချက်အမျိုးအစားကုဒ် |
| | 7 | Raw Error Payload / Message | rawErrorPayload | မူရင်း Error သတင်းစကား (သို့) Payload |
| | 8 | Retry Count | retryCount | ပြန်လည်ကြိုးစားမှုအရေအတွက် |
| | 9 | Auto-Reverse | autoReverse | အလိုအလျောက်ပြန်လှန်မှုလုပ်ဆောင်ခြင်း ရှိ/မရှိ |
| | 10 | Assigned To | assignedTo | တာဝန်ပေးထားသူ |
| | 11 | Resolution State | resolutionState | ဖြေရှင်းမှုအခြေအနေ |
| | 12 | SLA | sla | သတ်မှတ်ထားသော ဝန်ဆောင်မှုအဆင့်အချိန် (မိနစ်) |
| | 13 | Notification Channel | notificationChannel | အကြောင်းကြားသည့်လမ်းကြောင်း (SMS, EMAIL, PUSH, IN-APP) |
| | 14 | Acknowledged By | acknowledgedBy | အကြောင်းကြားချက်ကို လက်ခံသိရှိသူ |
| | 15 | Acknowledged At | acknowledgedAt | အကြောင်းကြားချက် လက်ခံသိရှိသည့်အချိန် |
| | 16 | Action | action | စီမံခန့်ခွဲမှုခလုတ် |
| **Module 9: Employee Time, Attendance & Earnings Ledger** | 1 | Attendance ID | attendance_id | မှတ်တမ်း ID |
| | 2 | Emp ID | emp_id | ဝန်ထမ်း ID |
| | 3 | Attendance Date | attendance_date | အလုပ်လုပ်သောရက်စွဲ |
| | 4 | Shift Type | shift_type | DAY / NIGHT / OVERTIME |
| | 5 | Hours Worked | hours_worked | တစ်ရက်တာအတွင်း အလုပ်လုပ်သည့် နာရီ |
| | 6 | Hourly Rate | hourly_rate | တစ်နာရီ လုပ်အားခနှုန်း |
| | 7 | Daily Earned | daily_earned | ထိုရက်အတွက် ရရှိသော လစာငွေ |
| | 8 | Leave Type | leave_type | ခွင့်အမျိုးအစား (PAID/UNPAID) |
| | 9 | Status | status | APPROVED / PENDING |
| | 10 | Overtime Hours | overtime_hours | ပိုနာရီအလုပ်ချိန် (OT) |
| | 11 | Overtime Rate | overtime_rate | ပိုနာရီလုပ်အားခနှုန်း (Regular Rate × 1.5) |
| | 12 | Attendance Score | attendance_score | တက်ရောက်မှုအပေါ်အခြေခံသည့် Score (1-100) |
| | 13 | Action | action | စီမံခန့်ခွဲရန် |
| **Module 10: Withdrawal Limit Matrix** | 1 | Limit ID | limit_id | ကန့်သတ်ချက် ID |
| | 2 | Corp ID | corp_id | ကုမ္ပဏီ ID (Global Rule) |
| | 3 | Emp ID | emp_id | တစ်ဦးချင်း သီးသန့်ဆိုလျှင် ထည့်ရန် |
| | 4 | Limit Type | limit_type | PER_DAY / PER_WEEK / PER_MONTH / PER_TXN |
| | 5 | Max Amount | max_amount | အများဆုံးထုတ်ယူနိုင်သည့် ပမာဏ |
| | 6 | Max Count | max_count | အများဆုံးထုတ်ယူနိုင်သည့် အကြိမ်ရေ |
| | 7 | Is Active | is_active | အသုံးပြုနေသလား |
| | 8 | Custom Rule | custom_rule | JSON format ဖြင့် သတ်မှတ်နိုင်သော စိတ်ကြိုက်စည်းမျဉ်းများ |
| | 9 | Override Reason | override_reason | ပုံမှန်ကန့်သတ်ချက်ကို ကျော်လွန်ခွင့်ပြုရသည့် အကြောင်းရင်း |
| | 10 | Action | action | ပြင်ဆင်ရန် |
| **Module 11: Early Repayment (Prepayment)** | 1 | Prepayment ID | prepay_id | ကြိုတင်ပြန်ဆပ်မှု ID |
| | 2 | Emp ID | emp_id | ဝန်ထမ်း |
| | 3 | Request Amount | request_amount | ပြန်ဆပ်ရန်တောင်းဆိုငွေ |
| | 4 | Payment Method | payment_method | KBZPay / WavePay / Bank Transfer |
| | 5 | Payment Ref | payment_ref | ငွေလွှဲအထောက်အထား |
| | 6 | Status | status | PENDING / CONFIRMED / FAILED |
| | 7 | Early Repayment Discount | early_repayment_discount | စောစီးစွာပြန်ဆပ်ခြင်းအတွက် ရရှိမည့်လျှော့စျေး (%) |
| | 8 | Remaining Balance After Prepay | remaining_balance_after_prepay | ကြိုတင်ပြန်ဆပ်ပြီးနောက် ကျန်ရှိကြွေးကျန် |
| | 9 | **Service Type** | **service_type** | **ဤ Transaction ၏ အမျိုးအစား (ပုံသေ: `PREPAYMENT`). Fee Engine မှ ဤတန်ဖိုးကို အသုံးပြု၍ သက်ဆိုင်ရာ Fee Rule (သို့) Discount ကို ရွေးချယ်သည်။** |
| | 10 | Action | action | အတည်ပြုရန် |
| **Module 12: Fee Configuration & Tier Engine** | 1 | Fee Rule ID | fee_rule_id | သတ်မှတ်ထားသော Fee Rule ၏ သီးသန့် ID |
| | 2 | **Applicable Service Type** | **service_type** | **ဤ Fee Rule သက်ရောက်မည့် ဝန်ဆောင်မှု။ Select: `DISBURSAL`, `REPAYMENT`, `PREPAYMENT`** |
| | 3 | Corp ID | corp_id | ဤ Rule သက်ရောက်မည့် ကုမ္ပဏီ ID (NULL = Global) |
| | 4 | Fee Type | fee_type | `SERVICE_FEE` / `LATE_FEE` / `PREPAYMENT_DISCOUNT` |
| | 5 | Charge To | charge_to | မည်သူ့ကို ကောက်ခံမည်နည်း (`EMPLOYEE` / `CORPORATE`) |
| | 6 | Charge Timing | charge_timing | မည်သည့်အချိန်တွင် ကောက်ခံမည်နည်း (e.g., `ON_DISBURSAL`, `ON_REPAYMENT`, `ON_PREPAYMENT`) |
| | 7 | Calculation Method | calculation_method | `FLAT` / `PERCENTAGE` / `TIERED` |
| | 8 | Flat Amount | flat_amount | FLAT ဖြစ်ပါက ပုံသေပမာဏ (MMK) |
| | 9 | Percentage (%) | percentage_value | PERCENTAGE ဖြစ်ပါက ကောက်ခံမည့် ရာခိုင်နှုန်း |
| | 10 | Min Fee | min_fee | အနည်းဆုံးကောက်ခံမည့်ပမာဏ (floor) |
| | 11 | Max Fee | max_fee | အများဆုံးကောက်ခံမည့်ပမာဏ (cap) |
| | 12 | Tier Min Amount | tier_min_amount | ဤဆင့်၏ အနိမ့်ဆုံးထုတ်ယူပမာဏ |
| | 13 | Tier Max Amount | tier_max_amount | ဤဆင့်၏ အမြင့်ဆုံးထုတ်ယူပမာဏ |
| | 14 | Effective Start Date | effective_start_date | စတင်အကျုံးဝင်သည့်ရက် |
| | 15 | Effective End Date | effective_end_date | သက်တမ်းကုန်ဆုံးရက် |
| | 16 | Is Active | is_active | လက်ရှိအသုံးပြုနေမှု အခြေအနေ |
| | 17 | Fee Cap (Life-time) | fee_cap_amount | ဤ Service Type အတွက် စုစုပေါင်းကောက်ခံနိုင်သည့် အများဆုံးပမာဏ |
| | 18 | Action | action | စီမံရန် ခလုတ် |
| **Module 13: Employee Notification & Consent Center** | 1 | Consent ID | consent_id | သဘောတူညီချက်မှတ်တမ်း ID |
| | 2 | Emp ID | emp_id | ဝန်ထမ်း |
| | 3 | Agreement Type | agreement_type | TERMS / PRIVACY / FEE_POLICY |
| | 4 | Agreement Version | agreement_version | Version |
| | 5 | Consented At | consented_at | လက်ခံသည့်ရက်စွဲ |
| | 6 | Notify EWA Approved | notify_ewa_approved | EWA အတည်ပြုပါက အကြောင်းကြားလိုသလား |
| | 7 | Notify Repay Reminder | notify_repay_reminder | ပြန်ဆပ်ရန် သတိပေးချက် လိုသလား |
| | 8 | Consent Withdrawal Date | consent_withdrawal_date | သဘောတူညီချက် ရုပ်သိမ်းသည့်ရက်စွဲ |
| | 9 | Preferred Language | preferred_language | ကြိုက်နှစ်သက်သော ဘာသာစကား (MYANMAR/ENGLISH) |
| | 10 | Notification Read Receipt | notification_read_receipt | အကြောင်းကြားချက်ကို ဖတ်ရှုပြီးခြင်း အထောက်အထား |
| | 11 | Action | action | ပြင်ဆင်ရန် |
| **Module 14: Multi-Company Group / Parent Entity Master** | 1 | Group ID | group_id | Group သီးသန့် ID |
| | 2 | Group Name | group_name | Group အမည် |
| | 3 | Total Credit Limit | total_credit_limit | Group စုစုပေါင်း Credit ကန့်သတ်ချက် |
| | 4 | Status | status | ACTIVE / INACTIVE |
| | 5 | Group Risk Score | group_risk_score | Group အလိုက် စုစုပေါင်းဘေးအန္တရာယ်အဆင့် |
| | 6 | Consolidated Utilization | consolidated_utilization | Group အတွင်းရှိ ကုမ္ပဏီအားလုံး၏ ပေါင်းစပ်အသုံးပြုမှုနှုန်း (%) |
| | 7 | Action | action | ပြင်ဆင်ရန် |
