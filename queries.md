![Ironhack Logo](https://i.imgur.com/1QgrNNw.png)

# Answers

## Iteration 2

### 1. All the companies whose name match 'Babelgum'. Retrieve only their `name` field.

<!-- Your Code Goes Here -->
{name:/babelgum/i}
{name:1}
### 2. All the companies that have more than 5000 employees. Limit the search to 20 companies and sort them by **number of employees**.

<!-- Your Code Goes Here -->
{number_of_employees: {$gt: 5000}}
Limit 20
### 3. All the companies founded between 2000 and 2005, both years included. Retrieve only the `name` and `founded_year` fields.

<!-- Your Code Goes Here -->
{{founded_year: {$gte: 2000}}, {founded_year:{$lte: 2005}}}
{name: 1, founded_year: 1}
### 4. All the companies that had a Valuation Amount of more than 100.000.000 and have been founded before 2010. Retrieve only the `name` and `ipo` fields.

<!-- Your Code Goes Here -->
{founded_year: {$lt:2010}, "ipo.valuation_amount": {$gt: 100000000}}
{name: 1, ipo: 1}
### 5. All the companies that don't include the `partners` field.

<!-- Your Code Goes Here -->
{partners: {$exists: false}}

### 6. All the companies that have a null value on the `category_code` field.

<!-- Your Code Goes Here -->
{category_code: {$type: 'null'}}
### 7. Order all the companies by their IPO price in a descending order.

<!-- Your Code Goes Here -->
Sort {'ipo.valuation_amount': -1}
### 8. Retrieve the 10 companies with most employees, order by the `number of employees`

<!-- Your Code Goes Here -->
{number_of_employees: -1} Limit 10
### 9. All the companies founded on the second semester of the year (July to December). Limit your search to 1000 companies.

<!-- Your Code Goes Here -->
{founded_month: {$gte: 7}} Limit 1000
### 10. All the companies that have been founded on the first seven days of the month, including the seventh. Sort them by their `acquisition price` in a descending order. Limit the search to 10 documents.

<!-- Your Code Goes Here -->
{founded_day: {$lte: 7}}
sorting {'acquisition.price_amount': -1}
limit 10
<br>

## Iteration 3 (Bonus)

### 1. All the companies that have been acquired after 2010, order by the acquisition amount, and retrieve only their `name` and `acquisition` field.

<!-- Your Code Goes Here -->

### 2. Order the companies by their `founded year`, retrieving only their `name` and `founded year`.

<!-- Your Code Goes Here -->

### 3. All the companies on the 'web' `category` that have more than 4000 employees. Sort them by the amount of employees in ascending order.

<!-- Your Code Goes Here -->

### 4. All the companies whose acquisition amount is more than 10.000.000, and currency is 'EUR'.

<!-- Your Code Goes Here -->

### 5. All the companies that have been founded between 2000 and 2010, but have not been acquired before 2011.

<!-- Your Code Goes Here -->
