# CleanSalone: Community Waste Reporting System (Design)

**Course:** PROG101 Principles of Programming Logic and Design
**Assignment:** Assignment 1, Designing Logical Solutions for Sierra Leone Community Challenges
**Institution:** Limkokwing University of Creative Technology, Sierra Leone
**Student:** STUDENT NAME (STUDENT ID)

## Problem
Uncollected waste builds up in streets, markets and drains in Sierra Leone, causing flooding and disease. Residents have no simple way to report it, and councils have no organised way to decide which sites to clean first.

## Solution
CleanSalone is a logical design (algorithm, pseudocode and flowcharts only, no source code) for a system where residents submit waste reports. The system validates each report, calculates an urgency score, assigns High, Medium or Low priority, and tracks the status Pending, Assigned or Collected.

### Priority rules
Score = severity (1 to 3), plus 3 if hazardous (Medical or Chemical), plus 2 if uncollected for more than 7 days, plus 2 if near a drain.
High: 7 or more. Medium: 4 to 6. Low: below 4.

## Repository structure
| Folder | Contents |
|---|---|
| `algorithm/` | Step-by-step algorithm and sub-algorithms |
| `pseudocode/` | Full pseudocode of all modules |
| `flowcharts/` | Five flowcharts (PNG) and the editable `.drawio` file |
| `expected-outputs/` | Sample scenarios and expected results |
| `report/` | Final report (PDF or Word) |

## Modules
DisplayMenu, SubmitReport, ValidateReport, CalculateScore, GetPriority, ViewStatus, UpdateStatus.

## Sustainable Development Goals
SDG 11 (Sustainable Cities and Communities), SDG 6 (Clean Water and Sanitation), SDG 3 (Good Health and Well-being), SDG 13 (Climate Action).

## Open Source and Digital Public Good
The design is shared under the MIT licence so that councils, schools and developers can reuse and improve it. Possible contributions: Krio translation, an SMS or USSD interface, a map module and a council dashboard.

## Viewing the flowcharts
Open `flowcharts/CleanSalone_Flowcharts.drawio` at https://app.diagrams.net (File, Open from, Device) to edit all five flowcharts.

## Licence
MIT. See `LICENSE`.
