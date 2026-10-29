# China Fixed Income Analysis

Bond valuation, bond-fund screening and a corporate credit case using historical Chinese market observations from March 2023.

The project addresses three distinct research questions: calculating bond yields, selecting bond funds for a conservative investor, and investigating unusually large bond-price changes. The sections combine valuation calculations, product comparison and credit analysis.

## Three Research Questions

### 1. Bond Valuation: What Yield Does the Market Price Imply?

**Purpose:** Translate observed bond prices into yields using the timing and amount of the promised cash flows.

**Approach:** Reconstruct the coupon schedules for 010504, 018020 and 184575, calculate accrued interest, and solve for YTM. Distinguish annual coupon rates, nominal YTM and effective annual yields, and plot how fixed-cash-flow prices respond to required yields.

**Finding:** Under the stated clean-price and settlement assumptions, reconstructed nominal yields are **1.916%, 2.595% and 2.718%**, close to the quoted yields recorded in the coursework. Differences between calculations must be assessed using consistent payment and quotation conventions; they do not establish that quoted YTM ignores compounding.

### 2. Bond-Fund Screening: Which Funds Fit a Conservative Allocation?

**Purpose:** Build a fund-selection process around a conservative investor's risk and income objectives.

**Approach:** Compare a five-fund historical sample using mandate, interest-rate exposure, credit and liquidity risk, fees, management and performance measured over consistent periods.

**Finding:** The original coursework preferred **Nuode Anhong Pure Bond A (010440)**. This edition presents the screening framework and retains that historical preference, without turning ratio figures with unspecified calculation methods into a new numerical ranking.

### 3. Credit Analysis: Why Did Two Bonds from the Same Issuer Move So Differently?

**Purpose:** Investigate an unusually large price divergence. The research team selected **20 Yuanzi 01 (175093)** and **21 Yuanzi 01 (175670)** because of their contrasting price changes in the original March 2023 observations.

**Approach:** Calculate returns on the recorded price pairs and examine repayment horizons, put rights, amended payment arrangements and issuer credit risk. Use an event timeline and a possible-explanations table to separate contractual facts, subsequent disclosures and hypotheses about the price changes.

**Finding:** The supplied price pairs imply **-7.79%** for 20 Yuanzi 01 and **+106.06%** for 21 Yuanzi 01. Different repayment expectations offer a possible explanation, but the observations do not isolate the cause of the divergence. An approaching put date does not ensure payment or a price increase.

## Report and Model

- [Read the full report](report/China_Fixed_Income_Report.md)
- [Download the Excel model](models/China_Fixed_Income_Model.xlsx)

## Bond Yield Results

Prices are treated as clean prices per RMB100 face value. Settlement is assumed to be 13 March 2023.

| Bond code | Quoted price | Reconstructed nominal YTM | Effective annual yield |
| --- | ---: | ---: | ---: |
| 010504 | 104.648 | 1.916% | 1.925% |
| 018020 | 99.957 | 2.595% | 2.595% |
| 184575 | 100.000 | 2.718% | 2.718% |

The 184575 yield-to-put scenario is **2.716%**, assuming valid exercise and par payment on the contractual put date of 14 September 2025. The maturity scenario holds its coupon constant after the reset option.

## Price–Yield Curves

![Bond price–yield curves with model base cases marked](assets/Price_Yield_Curves.png)

The curves hold promised cash flows constant. Dots mark the model base cases. The 184575 curve assumes its coupon remains unchanged after the 2025 reset option. This image is a static export; the Excel **Price_Yield** worksheet contains the linked price grid and editable chart.

## Credit-Event Timeline

The report and model trace the original bond horizons, the 2022 change to 20 Yuanzi 01's payment arrangement, and the March 2023 price observations. The report separately identifies later May and June 2023 put notices. The June notice warns that the funds for the registered put claims had not been secured.

A **possible explanation / evidence needed** table in the report considers repayment expectations, liquidity, comparison-price effects and issuer credit information. Later disclosures provide context without being treated as causes established for the March price changes.

## Workbook Contents

| Worksheet | Contents |
| --- | --- |
| Overview | Linked results and model conventions |
| Tbond_010504 | Semiannual coupon schedule, accrual, yield and price sensitivity |
| CDB_018020 | Annual coupon schedule, accrual, yield and price sensitivity |
| Nanjing_184575 | Maturity yield, separate put scenario and fixed-cash-flow sensitivity |
| Credit_Case | Price-return calculations and a dated chronology of bond events and subsequent notices |
| Price_Yield | Formula-linked clean-price curves across a 0%–8% nominal-yield grid |

Each bond worksheet includes a visible formula-based yield calculation below its cash-flow schedule. No macros or external workbook links are required. The Clean / Full selector changes the interpretation of the historical quoted price. Updating settlement beyond the stated coupon period requires rebuilding the schedule.

## Modelling Assumptions

Historical prices and quoted yields are taken from the preserved coursework. Clean-price interpretation, same-day settlement and the post-reset coupon path are modelling assumptions. Later issuer reports are identified as retrospective sources. The results are historical illustrations rather than current investment recommendations.

## Project Origin

Developed from an undergraduate group assignment in Introduction to Asset Pricing. Jiarong Xu prepared the reconstructed Excel model and revised portfolio analysis. Original student identifiers and third-party PDFs are excluded.

## References

The report contains input-level references and links to public bond documents. Key sources include Shanghai Stock Exchange disclosures, Ministry of Finance issue information, the supplied 2007 PBOC formula attachment and Caks (1977), *The Coupon Effect on Yield to Maturity*. The event timeline also cites the issuer’s put notices published on 9 May and 7 June 2023.
