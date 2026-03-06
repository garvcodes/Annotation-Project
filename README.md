# Annotated Dataset of Clinical Case Report Abstracts

## Overview

This dataset contains open-access clinical case report abstracts collected from PubMed Central (PMC), annotated for **perceived diagnostic clarity** from a lay reader's perspective. The goal is to study how clearly the diagnostic process is communicated in medical narratives, without requiring medical expertise from annotators.

## Dataset

`case_reports_abstracts.csv` contains 500 abstracts with the following fields:

| Field | Description |
|-------|-------------|
| `pmcid` | PubMed Central identifier |
| `pmid` | PubMed identifier |
| `license` | Copyright/license information for the article |
| `abstract` | Full abstract text |

## Annotation Scheme

Each abstract receives two labels. Annotators should focus on the **case description and conclusion** sections, where the diagnostic narrative is typically found.

### Label 1: Perceived Diagnostic Clarity

| Label | Description |
|-------|-------------|
| Clear | The diagnosis is presented confidently and directly, with little or no discussion of diagnostic difficulty or alternative explanations. |
| Somewhat Uncertain | The abstract includes some ambiguity or competing possibilities, but the diagnostic story is mostly resolved. |
| Highly Uncertain | The abstract emphasizes diagnostic difficulty — misdiagnosis, prolonged workup, or conflicting evidence. |

### Label 2: Primary Source of Diagnostic Uncertainty

1. Diagnostic revision or misdiagnosis
2. Multiple competing diagnoses
3. Conflicting or inconclusive tests
4. Delayed recognition or prolonged diagnostic workup
5. Unusual symptom presentation
6. No clear source of uncertainty
7. Other

**Note:** Labels cannot be assigned by keyword rules alone (e.g., "initially suspected," "misdiagnosed"). Annotators must evaluate the overall tone and narrative context.

## Sample

`sample.txt` contains a single annotated example drawn from the dataset.

## Data Source & Licensing

Articles are sourced from the **PMC Open Access Subset** (2015–2020), restricted to English-language case reports indexed in PMC. Each article retains its original license (recorded in the `license` field). This dataset may only be used in accordance with the individual license terms of each article.

This dataset should **not** be used to:
- Make clinical decisions
- Estimate true diagnostic complexity
- Identify or profile individuals

## Ethical Considerations

- All abstracts are from published, de-identified case reports
- Abstracts (not full text) are used to minimize re-identification risk
- Any abstract containing unusually specific identifying details has been excluded
