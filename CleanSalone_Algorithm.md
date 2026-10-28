# CleanSalone Algorithm

## Main algorithm
1. Start.
2. Set `running` to TRUE.
3. While `running` is TRUE, repeat steps 4 to 9.
4. Display the main menu (1 Submit a report, 2 View report status, 3 Update report status, 4 Exit).
5. Read the user's choice.
6. If the choice is 1, run Submit Report.
7. Else if the choice is 2, run View Status.
8. Else if the choice is 3, run Update Status.
9. Else if the choice is 4, set `running` to FALSE. Otherwise display "Invalid choice".
10. Display "Thank you for keeping Sierra Leone clean".
11. Stop.

## A. Submit Report
1. Read location, wasteType, severity, daysUncollected and nearDrain.
2. Run Validate Report with location, severity and daysUncollected.
3. If FALSE, display "Invalid data, try again", read the three values again and return to step 2.
4. If wasteType is "Medical" or "Chemical", set isHazardous to TRUE, otherwise FALSE.
5. Run Calculate Score and store the result in score.
6. Run Get Priority with score and store the result in priority.
7. Add 1 to reportID.
8. Set status to "Pending".
9. Save the report.
10. Display reportID, priority and status.

## B. Validate Report
1. Receive location, severity and daysUncollected.
2. If location is not empty AND severity is between 1 and MAX_SEVERITY AND daysUncollected is 0 or more, return TRUE.
3. Otherwise return FALSE.

## C. Calculate Score
1. Receive severity, isHazardous, daysUncollected and nearDrain.
2. Set score equal to severity.
3. If isHazardous is TRUE, add 3.
4. If daysUncollected is greater than LATE_DAYS (7), add 2.
5. If nearDrain is TRUE, add 2.
6. Return score.

## D. Get Priority
1. Receive score.
2. If score >= HIGH_SCORE (7), return "High".
3. Else if score >= MEDIUM_SCORE (4), return "Medium".
4. Otherwise return "Low".

## E. View Status
1. Read reportID.
2. Set found to FALSE.
3. For each saved report, if its ID equals reportID, display its details and set found to TRUE.
4. If found is FALSE, display "Report not found".

## F. Update Status
1. Read reportID and newStatus.
2. If reportID does not exist, display "Report not found" and stop.
3. If newStatus is "Pending", "Assigned" or "Collected", set the report's status to newStatus and display "Updated".
4. Otherwise display "Invalid status".
