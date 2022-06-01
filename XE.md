Note: Dear Eman and Daniel, please take into consideration that the acceptance cretirea you attached to the task differs from actual release (e.g. the 6th point), 
hence some acceptance criteria mentioned in the task are not valid for the current design. However, I wrote the test cases based on actual development as it semmed more 
reasonable. Please also note that I didn't waste much time on the order of test cases and payed more attention to priority. In reality related test cases should follow each other.


Test case 1: Checking the layout of currency converter.

Steps to reproduce:
1. Open the following link: https://www.xe.com/currencyconverter/
2. Verify the layout of the currency converter.

Expected result:
The currency converter should have the following layout: ![XE](https://user-images.githubusercontent.com/39699423/171394568-14738139-630b-40d0-b752-ed7b41091d40.jpg)


Test case 2: Checking if the amount is prefilled.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.

Steps to reproduce:
Verify the Amount field.

Expected result: 
"$1" should be prefilled in Amount field when opening currency convertor.


Test case 3: Checking if From currency is prefilled.

Preconditions:
User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
Verify From field.

Expected result: 
"USD - US Dollar" should be preselected in From field when opening currency convertor.


Test case 4: Checking if To currency is prefilled.

Preconditions:
User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
Verify To field.

Expected result: 
"EUR - Euro" should be preselected in To field when opening currency convertor.


Test case 5: Inserting an integer in Amount field.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.

Steps to reproduce:
Insert 156 in amount field.

Expected result: 
"$156.00" should be shown in Amount field.


Test case 6: Inserting a decimal in Amount field.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.

Steps to reproduce:
Insert 156.15 in amount field.

Expected result: 
"$156.15" should be shown in Amount field.


Test case 7: Inserting a decimal with more than 2 digits after the point in Amount field (round up).

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.

Steps to reproduce:
Insert 156.1575 in amount field.

Expected result: 
"$156.16" should be shown in Amount field.


Test case 8: Inserting a decimal with more than 2 digits after the point in Amount field (round down).

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.

Steps to reproduce:
Insert 156.1515 in amount field.

Expected result: 
"$156.15" should be shown in Amount field.


Test case 9: Inserting a letter in Amount field.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.
3. EUR is selected in To field.

Steps to reproduce:
Insert "a" in amount field.

Expected result: 
The following error message should be shown: "Please enter a valid amount".

Test case 10: Inserting a symbol in Amount field.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.
3. EUR is selected in To field.

Steps to reproduce:
Insert "&^%" in amount field.

Expected result: 
The following error message should be shown: "Please enter a valid amount".


Test case 11: Inserting a negativ number in Amount field.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.
3. EUR is selected in To field.

Steps to reproduce:
Insert "-50" in amount field.

Expected result: 
The System should show results for 50 USD.


Test case 12: Selecting From currency.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. USD is selected in From field.

Steps to reproduce:
1. Click on From dropdown list.
2. Select another currency, e.g. GBP.

Expected result: 
GBP should be shown as From currency.


Test case 13: Selecting To currency.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/
2. EUR is selected in To field.

Steps to reproduce:
1. Click on To dropdown list.
2. Select another currency, e.g. GBP.

Expected result: 
GBP should be shown as To currency.


Test case 14: Checking that all necessary info is shown afteer clicking Convert.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in Amount field.
2. Select Eur as From currency.
3. Select USD as To currency.
4. Click Convert.

Expected result: 
The folloing info should be shown:
- 10 Euros = *** US Dollars
- 1 EUR = *** USD
- 1 USD = *** EUR
 ![Results](https://user-images.githubusercontent.com/39699423/171397102-52b4a4bd-d5e9-4d54-bbf0-464829dd1f9f.jpg)


Test case 15: Checking that calculation is correct.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in Amount field.
2. Select Eur as From currency.
3. Select USD as To currency.
4. Click Convert.

Expected result: 
The calculation should be mathematically correct. E.g. if 1 EUR = 1.07174 USD. then 10 EUR should equal to 10.7174 USD.


Test case 14: Swapping source and target currencies.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Select GBP in From field.
2. Select AMD in To field.
3. Click on blue convert button between the currencies.

Expected result: 
AMD should be shown in From field, GBP should be shown in To field.


Test case 15. Checking that the calculations are updated after swapping currencies.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in amount field.
2. Select GBP in From field.
3. Select AMD in To field.
4. Click Convert.
5. Verify that calculation for 10 GBP to AMD is shown, as well as 1 GBP and 1 AMD conversion rates. (*Actually these kind of steps are introduced as expected reulst
for the previous step but I put it here to keep it simple).
7. Click on blue convert button between the currencies.

Expected result: 
1. AMD should be shown in From field, GBP should be shown in To field.
2. Calculation should be shown in GBP for 10 AMD (10 AMD = X GBP).
3. AMD conversion rate should be shown after calculation.
4. GBP conversion rate should be shown at the end.
![Swap](https://user-images.githubusercontent.com/39699423/171399456-a1c543ef-167f-4587-9908-dde25e4b45b3.jpg)


Test case 16. Checking the dropdown lists.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Click on From dopdown.

Expected result: 
1. The list of most popular currencies should be shown followed by other currencies in alphabetical order.
***To be updated to include currency lists provided by business side.


Test case 17. Checking the URI after conversion.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in Amount field.
2. Select Eur as From currency.
3. Select USD as To currency.
4. Click Convert.
5. Verify the URI.

Expected result: 
The URI should be as follows:'https://www.xe.com/currencyconverter/convert/?Amount=10&From=EUR&To=USD'
It should include the info on amount, from and to currencies.



Test case 18. Checking the URI is updated after every conversion.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in Amount field.
2. Select Eur as From currency.
3. Select USD as To currency.
4. Click Convert.
5. Change From to GBP.
6. Verify the URI.

Expected result: 
From currency should be changed to GBP in the URI: 'https://www.xe.com/currencyconverter/convert/?Amount=10&From=GBP&To=USD'


Test case 19. Checking the URI is updated after every conversion.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in Amount field.
2. Select Eur as From currency.
3. Select USD as To currency.
4. Click Convert.
5. Copy the URI: 'https://www.xe.com/currencyconverter/convert/?Amount=10&From=EUR&To=USD'
6. Open any other tab in any browser.
7. Paste the copied URI.

Expected result: 
XE converter page should be shown with the info and results provided in steps (10 EUR to USD).


Test case 20. Checking that the calculations are automatically updated after clicking Convert when changing any parameter.

Preconditions:
1. User is on currency converter page: https://www.xe.com/currencyconverter/

Steps to reproduce:
1. Insert 10 in Amount field.
2. Select Eur as From currency.
3. Select USD as To currency.
4. Click Convert.
5. Verify that tha calculations are shown.
6. Change From to GBP.
7. Verify the calculations.

Expected result: 
The info should be shown for 10 GBP to USD.
