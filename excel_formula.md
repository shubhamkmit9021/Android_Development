### General Excel Formulas

1. **Mathematical Formulas:**
   - Addition: `=A1 + B1`
   - Subtraction: `=A1 - B1`
   - Multiplication: `=A1 * B1`
   - Division: `=A1 / B1`

2. **Statistical Formulas:**
   - Average: `=AVERAGE(A1:A10)`
   - Sum: `=SUM(A1:A10)`
   - Count: `=COUNT(A1:A10)`
   - Max: `=MAX(A1:A10)`
   - Min: `=MIN(A1:A10)`

3. **Text Formulas:**
   - Concatenate: `=CONCATENATE(A1, " ", B1)`
   - Length: `=LEN(A1)`
   - Left: `=LEFT(A1, 5)`
   - Right: `=RIGHT(A1, 5)`
   - Mid: `=MID(A1, 2, 3)`

4. **Date and Time Formulas:**
   - Today's date: `=TODAY()`
   - Current time: `=NOW()`
   - Date difference: `=DATEDIF(A1, B1, "D")`
   - Date functions: `=YEAR(A1)`, `=MONTH(A1)`, `=DAY(A1)`

5. **Logical Formulas:**
   - IF statement: `=IF(A1 > B1, "True", "False")`
   - AND: `=AND(A1 > 0, B1 > 0)`
   - OR: `=OR(A1 > 0, B1 > 0)`

6. **Lookup and Reference Formulas:**
   - VLOOKUP: `=VLOOKUP(A1, Range, 2, FALSE)`
   - HLOOKUP: `=HLOOKUP(A1, Range, 2, FALSE)`
   - INDEX-MATCH: `=INDEX(ColumnToReturn, MATCH(LookupValue, LookupColumn, 0))`

7. **Financial Formulas:**
   - Future value: `=FV(rate, nper, pmt, pv)`
   - Present value: `=PV(rate, nper, pmt, fv)`
   - Payment: `=PMT(rate, nper, pv, fv)`

8. **Math Functions:**
   - Square root: `=SQRT(A1)`
   - Power: `=POWER(A1, B1)`
   - Round: `=ROUND(A1, 2)`
