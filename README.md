# Assignment-02
Assignment 2: Data Cleaning and Transformation

(1) Missing values
Price missing: 3 rows
Category missing: 4 rows
Formula
Price missing count: =COUNTBLANK(D2:D35)
Category missing count: =COUNTBLANK(F2:F35)

(2) Inconsistent data
Product Name casing issues found:

laptop → Laptop
smartphone → Smartphone
headphones → Headphones
Category typo found:
Electroni → Electronics

Formula
Standardize product names: =PROPER(B2)
Standardize category: =IF(F2="Electroni","Electronics",F2)

(3) Duplicates
Duplicate rows found: 3 extra duplicate rows
Duplicated records

21-AUG-CA | Laptop Bag | Samsonite | 50 | 35 | Accessories
17-JUN-IN | Laptop | HP | 950 | 25 | Electronics
16-APR-ES | headphones | Bose | 250 | 20 | Electronics

Formula
Go to setting then data then remove duplicates then just enable only product id then duplicates will remove

(4) Split Product ID
Example: 28-JAN-US

Formulas
Manufacturing date part: =LEFT(A2,6)
Country code: =RIGHT(A2,2)
Merge Brand Name + Product Name
Formula=C2&" "&B2

(5) Number Formating
Format the data type of the "Price" column to currency format			
Select the "Price" column.Go to the Home tab on the top ribbon.Locate the Number group.Click the dropdown menu under the General/Number box and select Currency.

Manufacturing Date column.Right-click and choose Format Cells .Go to the Number tab and select Date from the category list.  select Custom from the category list.Enter DD-MM-YYYY in the Type input box and click OK.

(6) Conditional Formating
Price Conditional Formating
Highlight the cells in your "Price" column .Go to the Home tab on the top ribbon.Click on Conditional Formatting in the Styles group. Color Scales and select preferred style 

Conditional Formating Electronics Category
Select the data in your "Category" column .Go to the Home tab on the top ribbon.Click Conditional Formatting > New Rule...Select "Use a formula to determine which cells to format".Enter the following formula in the box :=$A2="Electronics"Click the Format... button, choose highlight color under the Fill tab, and click OK.

