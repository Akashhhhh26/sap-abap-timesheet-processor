# sap-abap-timesheet-processor
ABAP utility to validate and summarize legacy HR Timesheet data
## Business Problem
HR's legacy payroll system exports flat files of daily clock-in/clock-out
records with no validation. This utility reads, validates, and reports
anomalies automatically.

## What it does
- Parses a flat file into structured internal tables
- Flags records where clock-out is earlier than clock-in
- Flags records exceeding 12 hours worked
- Outputs a clean report split into valid records and exceptions

## Technical concepts used
- Custom structure (TYPES) matching file layout
- Standard internal table for raw records
- String parsing (SPLIT)
- IF/CASE-based business rule validation
- WRITE-based structured reporting

## Files
- `timesheet_processor.abap` — main program source
- `timesheet.txt` — sample input file
- `output_screenshot.png` — sample report output
