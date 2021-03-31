## Vehicle-Service-Dataset-Handling-Errors-during-ETL-using-SSIS

Problem : Cleaning  and removing errors in the dataset containing over 1 million rows in Microsoft Visual studio

#### About Data

Vehicle service Dataset consists of 1050000 rows consisting of Customer ID, Date since the customer is tied to the company, name of the vehicle, 2014 and 2015 service cost in dollars and 2016 estimated service cost in dollars.

#### Cleaning data using Excel and Notepad++

Duplicate file is created for vehicleservice.csv and transformations in data type is done on this file

The file is opened in excel by first converting to .txt and using text to columns and using semicolon as demiliter

Date format choosen is yyyy-mm-dd and dollar sign is removed in 2014,2015,2016E columns(Vehicle service cost)

![image](https://user-images.githubusercontent.com/80466173/113104679-73898a80-921e-11eb-87e0-1597be810755.png)

#### Data flow
![5](https://user-images.githubusercontent.com/80466173/113103638-2527bc00-921d-11eb-8a2b-60e2c1e7cca9.PNG)

Input is fed in Flat file source

Conditional split is created to get the bad records since an extra column is created as shown(Column 6)

![4](https://user-images.githubusercontent.com/80466173/113104984-bd727080-921e-11eb-844d-7bb074f53de8.PNG)

![image](https://user-images.githubusercontent.com/80466173/113105121-dc710280-921e-11eb-8b99-169314e95ec1.png)

The rest of the records(good records are connected into OLE DB Destination and then Run is clicked
