# EnrollmentDataMacro
This Macro was written to expedite creating enrollment and disenrollment
dates to use during ACA affordability and compliance testing. It takes a 
raw data filefrom UMR that will have multiple ranges listed for employees 
and dependents. The issue with this is that it will show a new line for 
any changes even when there is no break in coverage. For ACA affordability 
and compliance testing purposes we needed to have just the basic ranges of 
when someone is enrolled or not. This macro will transform the following 
information into what my company needed.

Example Data:

JAN | FEB | MAR | APR | ...etc. --> Enroll   | Disenroll
 0  |  1  |  1  |  0  | ...etc. --> 2/1/20XX | 3/31/20XX

This code is for adding the Enrollment and Disenrollment dates for Unique 
IDs based on whether there is a one or a zero(blank) for each month. It 
will also account for breaks in coverage and add an additional line as 
needed.(Multiple times if necessary)
