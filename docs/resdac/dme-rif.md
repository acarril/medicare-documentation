# Durable Medical Equipment RIF

??? note "Source"
    [https://www.resdac.org/cms-data/files/dme-rif](https://www.resdac.org/cms-data/files/dme-rif)

## Overview

The Durable Medical Equipment (DME) file contains final action, fee-for-service claims submitted by Durable Medical Equipment suppliers. This file includes:

- diagnosis, (ICD-9 diagnosis),
- services provided (CMS Common Procedure Coding System (HCPCS) codes),
- dates of service,
- reimbursement amounts,
- DME provider number, and
- beneficiary demographic information.

Availability: CY 1999 - 2015

The 12-month run-off final action claims for 2016 will be available in the beginning of 2018.

## Data Documentation

### Durable Medical Equipment RIF

|   Index | SAS Name               | Variable Name                                                                                                                                                                          | Limitation   | Code Table   |
|--------:|:-----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|:-------------|
|       1 | `BENE_ID`              | [Encrypted CCW Beneficiary ID](https://www.resdac.org/cms-data/variables/encrypted-ccw-beneficiary-id)                                                                                 |              |              |
|       2 | `CLM_ID`               | [Claim ID](https://www.resdac.org/cms-data/variables/Claim-ID)                                                                                                                         | *            |              |
|       3 | `RIC_CD`               | [NCH Near Line Record Identification Code](https://www.resdac.org/cms-data/variables/NCH-Near-Line-Record-Identification-Code)                                                         |              | *            |
|       4 | `CLM_TYPE`             | [NCH Claim Type Code](https://www.resdac.org/cms-data/variables/nch-claim-type-code)                                                                                                   |              | *            |
|       5 | `FROM_DT`              | [Claim From Date](https://www.resdac.org/cms-data/variables/Claim-Date)                                                                                                                |              |              |
|       6 | `THRU_DT`              | [Claim Through Date](https://www.resdac.org/cms-data/variables/Claim-Through-Date)                                                                                                     |              |              |
|       7 | `WKLY_DT`              | [NCH Weekly Claim Processing Date](https://www.resdac.org/cms-data/variables/NCH-Weekly-Claim-Processing-Date)                                                                         |              |              |
|       8 | `ENTRY_CD`             | [Carrier Claim Entry Code](https://www.resdac.org/cms-data/variables/Carrier-Claim-Entry-Code)                                                                                         |              |              |
|       9 | `DISP_CD`              | [Claim Disposition Code](https://www.resdac.org/cms-data/variables/Claim-Disposition-Code)                                                                                             |              | *            |
|      10 | `CARR_NUM`             | [Carrier Number](https://www.resdac.org/cms-data/variables/Carrier-Number)                                                                                                             |              | *            |
|      11 | `PMTDNLCD`             | [Carrier Claim Payment Denial Code](https://www.resdac.org/cms-data/variables/Carrier-Claim-Payment-Denial-Code)                                                                       |              | *            |
|      12 | `PMT_AMT`              | [Claim Payment Amount](https://www.resdac.org/cms-data/variables/Claim-Payment-Amount-0)                                                                                               | *            |              |
|      13 | `PRPAYAMT`             | [Carrier Claim Primary Payer Paid Amount*](https://www.resdac.org/cms-data/variables/Carrier-Claim-Primary-Payer-Paid-Amount)                                                          |              |              |
|      14 | `ASGMNTCD`             | [Carrier Claim Provider Assignment Indicator Switch](https://www.resdac.org/cms-data/variables/Carrier-Claim-Provider-Assignment-Indicator-Switch)                                     |              | *            |
|      15 | `PROV_PMT`             | [NCH Claim Provider Payment Amount*](https://www.resdac.org/cms-data/variables/NCH-Claim-Provider-Payment-Amount)                                                                      |              |              |
|      16 | `BENE_PMT`             | [NCH Claim Beneficiary Payment Amount*](https://www.resdac.org/cms-data/variables/NCH-Claim-Beneficiary-Payment-Amount)                                                                |              |              |
|      17 | `SBMTCHRG`             | [NCH Carrier Claim Submitted Charge Amount*](https://www.resdac.org/cms-data/variables/NCH-Carrier-Claim-Submitted-Charge-Amount)                                                      |              |              |
|      18 | `ALOWCHRG`             | [NCH Carrier Claim Allowed Charge Amount*](https://www.resdac.org/cms-data/variables/NCH-Carrier-Claim-Allowed-Charge-Amount)                                                          |              |              |
|      19 | `DEDAPPLY`             | [Carrier Claim Cash Deductible Applied Amount*](https://www.resdac.org/cms-data/variables/Carrier-Claim-Cash-Deductible-Applied-Amount)                                                |              |              |
|      20 | `HCPCS_YR`             | [Carrier Claim HCPCS Year Code](https://www.resdac.org/cms-data/variables/Carrier-Claim-HCPCS-Year-Code)                                                                               |              |              |
|      21 | `PRNCPAL_DGNS_CD`      | [Claim Principal Diagnosis Code](https://www.resdac.org/cms-data/variables/Primary-Claim-Diagnosis-Code)                                                                               |              |              |
|      22 | `PRNCPAL_DGNS_VRSN_CD` | [Primary Claim Diagnosis Code Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Primary-Claim-Diagnosis-Code-Diagnosis-Version-Code-ICD-9-or-ICD-10) |              | *            |
|      23 | `ICD_DGNS_CD1`         | [Claim Diagnosis Code I](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-I)                                                                                             |              |              |
|      24 | `ICD_DGNS_VRSN_CD1`    | [Claim Diagnosis Code I Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-I-Diagnosis-Version-Code-ICD-9-or-ICD-10)             |              | *            |
|      25 | `ICD_DGNS_CD2`         | [Claim Diagnosis Code II](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-II)                                                                                           |              |              |
|      26 | `ICD_DGNS_VRSN_CD2`    | [Claim Diagnosis Code II Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-II-Diagnosis-Version-Code-ICD-9-or-ICD-10)           |              | *            |
|      27 | `ICD_DGNS_CD3`         | [Claim Diagnosis Code III](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-III)                                                                                         |              |              |
|      28 | `ICD_DGNS_VRSN_CD3`    | [Claim Diagnosis Code III Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-III-Diagnosis-Version-Code-ICD-9-or-ICD-10)         |              | *            |
|      29 | `ICD_DGNS_CD4`         | [Claim Diagnosis Code IV](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-IV)                                                                                           |              |              |
|      30 | `ICD_DGNS_VRSN_CD4`    | [Claim Diagnosis Code IV Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-IV-Diagnosis-Version-Code-ICD-9-or-ICD-10)           |              | *            |
|      31 | `ICD_DGNS_CD5`         | [Claim Diagnosis Code V](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-V)                                                                                             |              |              |
|      32 | `ICD_DGNS_VRSN_CD5`    | [Claim Diagnosis Code V Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-V-Diagnosis-Version-Code-ICD-9-or-ICD-10)             |              | *            |
|      33 | `ICD_DGNS_CD6`         | [Claim Diagnosis Code VI](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-VI)                                                                                           |              |              |
|      34 | `ICD_DGNS_VRSN_CD6`    | [Claim Diagnosis Code VI Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-VI-Diagnosis-Version-Code-ICD-9-or-ICD-10)           |              | *            |
|      35 | `ICD_DGNS_CD7`         | [Claim Diagnosis Code VII](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-VII)                                                                                         |              |              |
|      36 | `ICD_DGNS_VRSN_CD7`    | [Claim Diagnosis Code VII Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-VII-Diagnosis-Version-Code-ICD-9-or-ICD-10)         |              | *            |
|      37 | `ICD_DGNS_CD8`         | [Claim Diagnosis Code VIII](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-VIII)                                                                                       |              |              |
|      38 | `ICD_DGNS_VRSN_CD8`    | [Claim Diagnosis Code VIII Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-VIII-Diagnosis-Version-Code-ICD-9-or-ICD-10)       |              | *            |
|      39 | `ICD_DGNS_CD9`         | [Claim Diagnosis Code IX](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-IX)                                                                                           |              |              |
|      40 | `ICD_DGNS_VRSN_CD9`    | [Claim Diagnosis Code IX Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-IX-Diagnosis-Version-Code-ICD-9-or-ICD-10)           |              | *            |
|      41 | `ICD_DGNS_CD10`        | [Claim Diagnosis Code X](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-X)                                                                                             |              |              |
|      42 | `ICD_DGNS_VRSN_CD10`   | [Claim Diagnosis Code X Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-X-Diagnosis-Version-Code-ICD-9-or-ICD-10)             |              | *            |
|      43 | `ICD_DGNS_CD11`        | [Claim Diagnosis Code XI](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-XI)                                                                                           |              |              |
|      44 | `ICD_DGNS_VRSN_CD11`   | [Claim Diagnosis Code XI Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-XI-Diagnosis-Version-Code-ICD-9-or-ICD-10)           |              | *            |
|      45 | `ICD_DGNS_CD12`        | [Claim Diagnosis Code XII](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-XII)                                                                                         |              |              |
|      46 | `ICD_DGNS_VRSN_CD12`   | [Claim Diagnosis Code XII Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Claim-Diagnosis-Code-XII-Diagnosis-Version-Code-ICD-9-or-ICD-10)         |              | *            |
|      47 | `RFR_UPIN`             | [DMERC Claim Ordering Physician UPIN Number](https://www.resdac.org/cms-data/variables/DMERC-Claim-Ordering-Physician-UPIN-Number)                                                     |              |              |
|      48 | `RFR_NPI`              | [DMERC Claim Ordering Physician NPI Number](https://www.resdac.org/cms-data/variables/DMERC-Claim-Ordering-Physician-NPI-Number)                                                       |              |              |
|      49 | `CCLTRNUM`             | [Clinical Trial Number](https://www.resdac.org/cms-data/variables/Clinical-Trial-Number)                                                                                               |              |              |
|      50 | `DOB_DT`               | [Date of Birth from Claim (Date)](https://www.resdac.org/cms-data/variables/Date-Birth-Claim-Date)                                                                                     |              |              |
|      51 | `GNDR_CD`              | [Gender Code from Claim](https://www.resdac.org/cms-data/variables/Gender-Code-Claim)                                                                                                  |              | *            |
|      52 | `RACE_CD`              | [Race Code from Claim](https://www.resdac.org/cms-data/variables/Race-Code-Claim)                                                                                                      |              | *            |
|      53 | `CNTY_CD`              | [County Code from Claim (SSA)](https://www.resdac.org/cms-data/variables/County-Code-Claim-SSA)                                                                                        |              |              |
|      54 | `STATE_CD`             | [State Code from Claim (SSA)](https://www.resdac.org/cms-data/variables/state-code-claim-ssa)                                                                                          |              | *            |
|      55 | `ZIP_CD`               | [Zip Code of Residence from Claim](https://www.resdac.org/cms-data/variables/Zip-Code-Residence-Claim)                                                                                 |              |              |
|      56 | `CLM_BENE_PD_AMT`      | [Carrier Claim Beneficiary Paid Amount](https://www.resdac.org/cms-data/variables/carrier-claim-beneficiary-paid-amount)                                                               |              | *            |

### LINE FILE

|   Index | SAS Name                 | Variable Name                                                                                                                                                        | Limitation   | Code Table   |
|--------:|:-------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|:-------------|
|       1 | `BENE_ID`                | [Encrypted CCW Beneficiary ID](https://www.resdac.org/cms-data/variables/encrypted-ccw-beneficiary-id)                                                               |              |              |
|       2 | `CLM_ID`                 | [Claim ID](https://www.resdac.org/cms-data/variables/Claim-ID)                                                                                                       | *            |              |
|       3 | `CLM_LN`                 | [Claim Line Number](https://www.resdac.org/cms-data/variables/Claim-Line-Number)                                                                                     |              |              |
|       4 | `CLM_TYPE`               | [NCH Claim Type Code](https://www.resdac.org/cms-data/variables/nch-claim-type-code)                                                                                 |              | *            |
|       5 | `THRU_DT`                | [Claim Through Date](https://www.resdac.org/cms-data/variables/Claim-Through-Date)                                                                                   |              |              |
|       6 | `TAX_NUM`                | [Line Provider Tax Number](https://www.resdac.org/cms-data/variables/Line-Provider-Tax-Number)                                                                       |              |              |
|       7 | `HCFASPCL`               | [Line HCFA Provider Specialty Code](https://www.resdac.org/cms-data/variables/Line-HCFA-Provider-Specialty-Code)                                                     |              | *            |
|       8 | `PRTCPTG`                | [Line Provider Participating Indicator Code](https://www.resdac.org/cms-data/variables/Line-Provider-Participating-Indicator-Code)                                   |              | *            |
|       9 | `SRVC_CNT`               | [Line Service Count](https://www.resdac.org/cms-data/variables/Line-Service-Count)                                                                                   |              |              |
|      10 | `TYPSRVCB`               | [Line HCFA Type Service Code](https://www.resdac.org/cms-data/variables/Line-HCFA-Type-Service-Code)                                                                 |              | *            |
|      11 | `PLCSRVC`                | [Line Place Of Service Code](https://www.resdac.org/cms-data/variables/line-place-service-code)                                                                      |              | *            |
|      12 | `EXPNSDT1`               | [Line First Expense Date](https://www.resdac.org/cms-data/variables/Line-First-Expense-Date)                                                                         |              |              |
|      13 | `EXPNSDT2`               | [Line Last Expense Date](https://www.resdac.org/cms-data/variables/Line-Last-Expense-Date)                                                                           |              |              |
|      14 | `HCPCS_CD`               | [Health Care Common Procedure Coding System](https://www.resdac.org/cms-data/variables/Line-HCFA-Common-Procedure-Coding-System)                                     |              |              |
|      15 | `MDFR_CD1`               | [Line HCPCS Initial Modifier Code](https://www.resdac.org/cms-data/variables/Line-HCPCS-Initial-Modifier-Code)                                                       |              |              |
|      16 | `MDFR_CD2`               | [Line HCPCS Second Modifier Code](https://www.resdac.org/cms-data/variables/Line-HCPCS-Second-Modifier-Code)                                                         |              |              |
|      17 | `BETOS`                  | [Line NCH BETOS Code](https://www.resdac.org/cms-data/variables/Line-NCH-BETOS-Code)                                                                                 |              | *            |
|      18 | `LINEPMT`                | [Line NCH Payment Amount](https://www.resdac.org/cms-data/variables/Line-NCH-Payment-Amount)                                                                         |              |              |
|      19 | `LBENPMT`                | [Line Beneficiary Payment Amount](https://www.resdac.org/cms-data/variables/Line-Beneficiary-Payment-Amount)                                                         |              |              |
|      20 | `LPRVPMT`                | [Line Provider Payment Amount](https://www.resdac.org/cms-data/variables/Line-Provider-Payment-Amount)                                                               |              |              |
|      21 | `LDEDAMT`                | [Line Beneficiary Part B Deductible Amount](https://www.resdac.org/cms-data/variables/Line-Beneficiary-Part-B-Deductible-Amount)                                     |              |              |
|      22 | `LPRPAYCD`               | [Line Beneficiary Primary Payer Code](https://www.resdac.org/cms-data/variables/Line-Beneficiary-Primary-Payer-Code)                                                 |              | *            |
|      23 | `LPRPDAMT`               | [Line Beneficiary Primary Payer Paid Amount](https://www.resdac.org/cms-data/variables/Line-Beneficiary-Primary-Payer-Paid-Amount)                                   |              |              |
|      24 | `COINAMT`                | [Line Coinsurance Amount](https://www.resdac.org/cms-data/variables/Line-Coinsurance-Amount)                                                                         |              |              |
|      25 | `PRPYALOW`               | [Line Primary Payer Allowed Charge Amount](https://www.resdac.org/cms-data/variables/Line-Primary-Payer-Allowed-Charge-Amount)                                       |              |              |
|      26 | `LSBMTCHG`               | [Line Submitted Charge Amount](https://www.resdac.org/cms-data/variables/Line-Submitted-Charge-Amount)                                                               |              |              |
|      27 | `LALOWCHG`               | [Line Allowed Charge Amount](https://www.resdac.org/cms-data/variables/Line-Allowed-Charge-Amount)                                                                   |              |              |
|      28 | `PRCNGIND`               | [Line Processing Indicator Code](https://www.resdac.org/cms-data/variables/Line-Processing-Indicator-Code)                                                           |              | *            |
|      29 | `PMTINDSW`               | [Line Payment 80%/100% Code](https://www.resdac.org/cms-data/variables/Line-Payment-80100-Code)                                                                      |              |              |
|      30 | `DED_SW`                 | [Line Service Deductible Indicator Switch](https://www.resdac.org/cms-data/variables/Line-Service-Deductible-Indicator-Switch)                                       |              | *            |
|      31 | `LINE_ICD_DGNS_CD`       | [Line Diagnosis Code](https://www.resdac.org/cms-data/variables/Line-Diagnosis-Code)                                                                                 |              |              |
|      32 | `LINE_ICD_DGNS_VRSN_CD`  | [Line Diagnosis Code Diagnosis Version Code (ICD-9 or ICD-10)](https://www.resdac.org/cms-data/variables/Line-Diagnosis-Code-Diagnosis-Version-Code-ICD-9-or-ICD-10) |              | *            |
|      33 | `DME_PURC`               | [Line DME Purchase Price Amount](https://www.resdac.org/cms-data/variables/Line-DME-Purchase-Price-Amount)                                                           |              | *            |
|      34 | `SUPLRNUM`               | [DMERC Line Supplier Provider Number](https://www.resdac.org/cms-data/variables/DMERC-Line-Supplier-Provider-Number)                                                 |              |              |
|      35 | `SUP_NPI`                | [DMERC Line Item Supplier NPI Number](https://www.resdac.org/cms-data/variables/DMERC-Line-Item-Supplier-NPI-Number)                                                 |              |              |
|      36 | `PRCNG_ST`               | [DMERC Line Pricing State Code](https://www.resdac.org/cms-data/variables/DMERC-Line-Pricing-State-Code)                                                             |              | *            |
|      37 | `PRVSTATE`               | [DMERC Line Provider State Code](https://www.resdac.org/cms-data/variables/DMERC-Line-Provider-State-Code)                                                           |              | *            |
|      38 | `SUP_TYPE`               | [DMERC Line Supplier Type Code](https://www.resdac.org/cms-data/variables/DMERC-Line-Supplier-Type-Code)                                                             |              | *            |
|      39 | `MDFR_CD3`               | [DMERC Line HCPCS Third Modifier Code](https://www.resdac.org/cms-data/variables/DMERC-Line-HCPCS-Third-Modifier-Code)                                               |              |              |
|      40 | `MDFR_CD4`               | [DMERC Line HCPCS Fourth Modifier Code](https://www.resdac.org/cms-data/variables/DMERC-Line-HCPCS-Fourth-Modifier-Code)                                             |              |              |
|      41 | `SCRNSVGS`               | [DMERC Line Screen Savings Amount](https://www.resdac.org/cms-data/variables/DMERC-Line-Screen-Savings-Amount)                                                       |              | *            |
|      42 | `DME_UNIT`               | [DMERC Line Miles/Time/Units/Services Count](https://www.resdac.org/cms-data/variables/DMERC-Line-MilesTimeUnitsServices-Count)                                      |              |              |
|      43 | `UNIT_IND`               | [DMERC Line Miles/Time/Units/Services Indicator Code](https://www.resdac.org/cms-data/variables/DMERC-Line-MilesTimeUnitsServices-Indicator-Code)                    |              | *            |
|      44 | `HCTHGBRS`               | [Hematocrit/Hemoglobin Test Results](https://www.resdac.org/cms-data/variables/HematocritHemoglobin-Test-Results)                                                    |              |              |
|      45 | `HCTHGBTP`               | [Hematocrit/Hemoglobin Test Type Code](https://www.resdac.org/cms-data/variables/HematocritHemoglobin-Test-Type-Code)                                                |              | *            |
|      46 | `LNNDCCD`                | [Line National Drug Code](https://www.resdac.org/cms-data/variables/Line-National-Drug-Code)                                                                         |              |              |
|      47 | `LINE_OTHR_APLD_IND_CD1` | [Line Other Applied Indicator 1st Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-1st-code)                                             |              | *            |
|      48 | `LINE_OTHR_APLD_IND_CD2` | [Line Other Applied Indicator 2nd Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-2nd-code)                                             |              | *            |
|      49 | `LINE_OTHR_APLD_IND_CD3` | [Line Other Applied Indicator 3rd Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-3rd-code)                                             |              | *            |
|      50 | `LINE_OTHR_APLD_IND_CD4` | [Line Other Applied Indicator 4th Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-4th-code)                                             |              | *            |
|      51 | `LINE_OTHR_APLD_IND_CD5` | [Line Other Applied Indicator 5th Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-5th-code)                                             |              | *            |
|      52 | `LINE_OTHR_APLD_IND_CD6` | [Line Other Applied Indicator 6th Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-6th-code)                                             |              | *            |
|      53 | `LINE_OTHR_APLD_IND_CD7` | [Line Other Applied Indicator 7th Code](https://www.resdac.org/cms-data/variables/line-other-applied-indicator-7th-code)                                             |              | *            |
|      54 | `LINE_OTHR_APLD_AMT1`    | [Line Other Applied Amount for 1st Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-1st-code)                                               |              | *            |
|      55 | `LINE_OTHR_APLD_AMT2`    | [Line Other Applied Amount for 2nd Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-2nd-code)                                               |              | *            |
|      56 | `LINE_OTHR_APLD_AMT3`    | [Line Other Applied Amount for 3rd Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-3rd-code)                                               |              | *            |
|      57 | `LINE_OTHR_APLD_AMT4`    | [Line Other Applied Amount for 4th Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-4th-code)                                               |              | *            |
|      58 | `LINE_OTHR_APLD_AMT5`    | [Line Other Applied Amount for 5th Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-5th-code)                                               |              | *            |
|      59 | `LINE_OTHR_APLD_AMT6`    | [Line Other Applied Amount for 6th Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-6th-code)                                               |              | *            |
|      60 | `LINE_OTHR_APLD_AMT7`    | [Line Other Applied Amount for 7th Code](https://www.resdac.org/cms-data/variables/line-other-applied-amount-7th-code)                                               |              | *            |

### Demonstrations/Innovations Code File

|   Index | SAS Name           | Variable Name                                                                                            | Limitation   | Code Table   |
|--------:|:-------------------|:---------------------------------------------------------------------------------------------------------|:-------------|:-------------|
|       1 | `BENE_ID`          | [Encrypted CCW Beneficiary ID](https://www.resdac.org/cms-data/variables/encrypted-ccw-beneficiary-id)   |              |              |
|       2 | `CLM_ID`           | [Claim ID](https://www.resdac.org/cms-data/variables/Claim-ID)                                           | *            |              |
|       3 | `CLM_TYPE`         | [NCH Claim Type Code](https://www.resdac.org/cms-data/variables/nch-claim-type-code)                     |              | *            |
|       4 | `DEMO_ID_SQNC_NUM` | [Demonstration sequence number](https://www.resdac.org/cms-data/variables/demonstration-sequence-number) |              |              |
|       5 | `DEMO_ID_NUM`      | [Demonstration number](https://www.resdac.org/cms-data/variables/demonstration-number)                   |              | *            |
|       6 | `DEMO_INFO_TXT`    | [Demo information text](https://www.resdac.org/cms-data/variables/demo-information-text)                 |              |              |