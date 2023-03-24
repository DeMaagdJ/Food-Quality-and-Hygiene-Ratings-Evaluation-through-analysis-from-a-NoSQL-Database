# NoSQL-Challenge
Module 12 HW Assignment


Opening Statement:
Source (https://courses.bootcampspot.com/courses/2864/assignments/46383?module_item_id=855821)

"The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles."

Methods:

The NoSQL_setup_starter.ipynb contains the architecture to setup and load the information from establishments.json within jupyternotebook.  A document called Uk_food was created and the establishments.json was imported as a collection via MongoDB Compass.  The syntax to import the data via the terminal has been provided in the markdown for others to utilize the data. 

After creating an instance of the Mongo Client within the notebook we assigned the database and collection to allow for further query.

![Screenshot 2023-03-23 at 9 18 19 PM](https://user-images.githubusercontent.com/119906575/227427407-3dbe05ea-828c-4d8c-bf34-e3f484b68b81.png)


In NoSQL_analysis_starter.ipynb we have several questions to be answered.  The queries were explored by utilizing the count_documents() to enumerate how many queried establishments exist.  The $gte and &lte functions were used to query data to find restaurants with a specified rating or, to localize establishments within a 0.01 degree from a local restaurant (Penang Flavours).  The queried data was transformed into a dataframe using pandas for readability. To answer question 4, a pipeline query was used to match the common hygiene score, group them by their Local Authorities, and sort in descending order.  A printout is provided in this readme file.

1. Which establishments have a hygiene score equal to 20?

Answer: There are 41 documents with a hygiene score equal to 20.

2. Which establishments in London have a `RatingValue` greater than or equal to 4?

Answer: There are 34 documents with a RatingValue greater than or equal to 4.

3. What are the top 5 establishments with a `RatingValue` rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

Answer: Howe and Co Fish and Chips - Van 17, Atlantic Fish Bar, Plumstead Manor Nursery, Iceland, Volunteer

4. How many establishments in each Local Authority area have a hygiene score of 0?

Answer: There are 55 documents that have a hygiene score of 0.
	
![Screenshot 2023-03-23 at 9 33 48 PM](https://user-images.githubusercontent.com/119906575/227427457-1812a085-dd7f-4720-8d50-eb7bffe0dcdf.png)
