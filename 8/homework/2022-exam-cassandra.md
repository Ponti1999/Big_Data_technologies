# Examination

## Exercise 1

**Narrative:** 

* Print the percentage of vaccinated people in Hungary for the dates between `2022-03-01` and `2022-03-30`, inclusive. 
* We are only interested in the columns `country`, `date` and `people_vaccinated_per_hundred`.
* The data should be sorted by date in descending order (newest first).
* Use the column `iso_code` and the value `HUN` to identify rows for Hungary.

**Instructions:**

* Use the [Vaccinations thema](https://github.com/medvekoma/cassandra-workshop/tree/main/thema/vaccinations) 
* Import the data from [country_vaccinations.csv](https://github.com/medvekoma/cassandra-workshop/blob/main/thema/vaccinations/country_vaccinations.csv) into a Cassandra table that has the right PRIMARY KEY to support the query described in the Narrative.
* Write the select statement that returns the data specified in the Narrative.

**Hints:**
* The essence of the exercise is to find the right PRIMARY KEY for the table, so that the query above can be executed.
* Make sure that the query runs as efficiently as possible.
* You can name the date field as `date1` in order to avoid conflicts with the reserved word `date`.

**To send**:
* The CREATE TABLE statement
* The SELECT query that returns the data specified above
* The output of the SELECT statement

## Exercise 2

**Narrative:**

* List the top 30 countries by the highest percentage of vaccinated people 
on the day `2022-03-29`. Use the field `people_vaccinated_per_hundred` for this purpose.
* We are only interested in the columns `country`, `date` and `people_vaccinated_per_hundred`.

**Instructions and Hints:**

* Same as above

**To send:**
* The CREATE TABLE statement
* The SELECT query that returns the data specified above
* The output of the SELECT statement