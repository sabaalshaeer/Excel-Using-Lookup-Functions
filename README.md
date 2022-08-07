# Excel-Using-Lookup-Functions
Use the XMATCH function to identify the row that contains the employee record.
    In the Employees worksheet, select cell C4 and enter the formula =XMATCH(C3,B11:B61,0)
    Verify that employee 1001 is found in row 2 of the dataset.
Find the employee name in the dataset based on the row ID by using the INDEX function.
    Select cell C5 and enter the formula =INDEX(Data,C4,2)
    Note: You will use the array variation of the INDEX function and the range name Data for the array argument.
    Verify that the employee name displayed is Jacques Charon.
Find the employee's department by using the VLOOKUP function based on the employee ID.
    Select cell C6 and enter the formula =VLOOKUP(C3,Data,3,FALSE)
    Verify that the department identified for Jacques is Accounting.
Identify the region of employee 1001.
    Select cell C7 and enter the formula =VLOOKUP(C3,Data,XMATCH(B7,B11:G11,0),FALSE)
    Note: The XMATCH function is nested within the VLOOKUP function to identify the column from which the function will return the value (col_index_num).
    Verify that the region identified for Jacques is Southeast.
Identify the manager and extension of the employee.
    Select cell C8 and enter the formula =VLOOKUP(C3,Data,5,FALSE)
    In cell C9 enter the formula =VLOOKUP(C3,Data,6,FALSE)
    Verify that Jacques' manager is Marlon Pellham and his extension is 4459.
Change the employee ID to identify the information for another employee.
    Select cell C3 and enter 1046
    Verify that all the employee information updates.
Enter a formula to look up the employee name based on the telephone extension.
    Select cell F4 and enter the formula =XLOOKUP(F3,G11:G61,C11:C61,"not found")
    Rosie Newton has extension 4717.
    Change cell F3 to 9999
    The "not found" message is shown.
