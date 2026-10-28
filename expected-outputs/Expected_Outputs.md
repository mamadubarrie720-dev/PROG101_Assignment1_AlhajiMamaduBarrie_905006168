# Expected Outputs (Sample Scenarios)

Score = severity + 3 (hazardous) + 2 (days > 7) + 2 (near drain).
High: 7 or more. Medium: 4 to 6. Low: below 4.

| No. | Type | Waste | Severity | Days | Near drain | Score | Expected result |
|---|---|---|---|---|---|---|---|
| 1 | Normal | Medical | 3 | 2 | Yes | 8 | High, ID 1, Pending |
| 2 | Normal | Household | 1 | 9 | No | 3 | Low, ID 2, Pending |
| 3 | Normal | Household | 2 | 8 | Yes | 6 | Medium, ID 3, Pending |
| 4 | Invalid | Household | 2 | 3 | Yes | n/a | Empty location: "Invalid data, try again" |
| 5 | Invalid | Household | 5 | 3 | No | n/a | Severity out of range: "Invalid data, try again" |
| 6 | Boundary | Chemical | 1 | 0 | No | 4 | Medium |
| 7 | Boundary | Household | 2 | 7 | No | 2 | Low (7 is not above 7) |
| 8 | Boundary | Medical | 2 | 3 | Yes | 7 | High |

## View and update
| Scenario | Input | Output |
|---|---|---|
| 9 | View ID 1 | `1 / Kissy Road Market / High / Pending` |
| 10a | Update ID 1 to "Assigned" | `Updated` |
| 10b | Update ID 1 to "Done" | `Invalid status` |
| 10c | Update ID 99 to "Collected" | `Report not found` |
| 11 | View ID 99 | `Report not found` |
