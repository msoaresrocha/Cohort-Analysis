# Cohort-Analysis
Demonstration of how create a cohort analysis using Tableau.

## **ETL process using Tableau Prep Builder**

First step of all analysis, is to look of the quality of the data. Fortunately, this data was already cleaned and we have only one row that pursued a null value. As shows in the figure below.
![image](https://user-images.githubusercontent.com/47664466/152188628-377fcfcd-9efd-46c9-bfa3-923d638c5d9c.png)


For cleaning null values of your dataset, you can use a huge techniques. Since all columns follow the same patten, one row null, I decided to take it off of the dataset as showed in the next step. After that, as you can see, we filtered all the null values from the dataset.
![image](https://user-images.githubusercontent.com/47664466/152188763-e8957a13-8760-4617-be01-8044316999e5.png)

![image](https://user-images.githubusercontent.com/47664466/152188788-dd779e11-7b04-4f6b-9705-7b77d2a99f63.png)


Everything is alright with the dataset, the following steps is to make an output step. In the output configuration, you can use the type of file you want, but using a convention, I will make a CSV file.
![image](https://user-images.githubusercontent.com/47664466/152188852-f3883166-503a-4d53-a40f-9038cb133d66.png)


## **Analysing the data with Tableau**

To begin with, our first calculated field will be fix the date that one customer made his first purchase  in the store (Retail or Restaurant).  To create this field you will need to know about 2 basic functions and use 2  fields that already exists in the dataset. The function FIXED, the is used to fix some value with based in two fields, and MIN to catch the first purchase date made by the costumer/user.
![image](https://user-images.githubusercontent.com/47664466/152188981-c8fb36fc-8197-430e-8b84-30daee8bf495.png)

Another important calculated field is to remove the month of the Purchase Date. This is important because our visualization in a management point of view is to verify the amount of users that are purchasing again in the Restaurant/Retain each month since their first purchase. For that, the creation of a new field only pursuing the month is made by using the steps 1,2,3 and 4.
![image](https://user-images.githubusercontent.com/47664466/152189075-32ddbef3-dde2-4aa2-89f8-a24ff8b9c4d0.png)

![image](https://user-images.githubusercontent.com/47664466/152189052-ef680f21-c50d-41e8-acce-c2a7616c55db.png)


Other calculation needed is to create a period that shows the amount of months after the first purchase. For this calculation we need to know only one function that is DATEDIFF. Each period means one month before the actual month.
![image](https://user-images.githubusercontent.com/47664466/152189119-05d01e86-f2e5-4a9a-98f9-32d99b0910e1.png)

![image](https://user-images.githubusercontent.com/47664466/152189140-e1949179-a4f4-42fc-ab16-9ed686e61cbb.png)


Now is time for us to create some analysis  with this data and the new fields that we created. The first one is drag the fields period, purchase date and the purchase line. The graph below is a result of how many customers returned after the first purchase for each month. For example, in the row called June, you have in number 1 the quantity of new users, 2 the quantity of users purchasing for the second month consecutively and 3 the users purchasing again that the first purchase was in April.
![image](https://user-images.githubusercontent.com/47664466/152189186-6827579c-1be7-4a7c-9e36-81b6f538edfd.png)

Our analysis is done and after that, we can use it as a decision making for the company. For instance, if the company wants to increase the amount of users buying again after 5 months, or if they will look only for the previous 2 months. The analysis will be useful only as a base for the managers to make the right decision. 
