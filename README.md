# test

```Create Table statement for the data included:
CREATE TABLE testAssignmentTable (
id int(10) NOT NULL AUTO_INCREMENT,
DOS date DEFAULT NULL,
LocationCode char(5) DEFAULT NULL,
InsuranceCode char(5) DEFAULT NULL,
InsuranceFC char(5) DEFAULT NULL,
ChargesExpected decimal(10,2) DEFAULT NULL,
ChargeUnits mediumint(9) DEFAULT NULL,
PaidToCharges decimal(10,2) DEFAULT NULL,
AdjustedByExpected decimal(10,2) DEFAULT NULL,
NewPatients mediumint(9) DEFAULT NULL,
Visits mediumint(9) DEFAULT NULL,
PRIMARY KEY (id),
KEY DOS (DOS),
KEY InsuranceCode (InsuranceCode),
KEY InsuranceFC (InsuranceFC),
KEY LocationCode (LocationCode)
) ENGINE=InnoDB AUTO_INCREMENT=196606 DEFAULT CHARSET=latin1
```
Column explanation:

DOS - The date the appointment took place on. 
LocationCode - The location code for the clinic the appointment took place at. 
InsuranceCode - The insurance responsible for covering the charges of the appointment. 
InsuranceFC - Grouping of insurances of similar type/rules. 
ChargesExpected - Charges expected to receive from the insurance for the appointment. 
ChargeUnits - Metric of how many billable procedures/multiples of a procedure were performed. 
PaidToCharges - Payments. 
AdjustedByExpected - Charges that are written off for various reasons. 
NewPatients - Number of patients who had their first visit. Visits - Total visits.

Table explanation:

This is an aggregate table for high level business reporting, it takes the data off of many visits and aggregates it by location, insurance, FC and DOS totals to cut down on the data size for quicker reporting.

Assignments:

1. Provided that the data set included is static, how would you improve the table structure from what is defined in the CREATE TABLE above? (With explanations)

2. Using the data in the data.csv, build a few example graphs/charts that you feel would be informative. You can use whatever software you like for the visualization (ie. Excel if it's the easiest)

3. Provide a MySQL query that produces the insurancecode and the average payments per visit for the insurancecode that had the highest average payments per visit in 2017.
