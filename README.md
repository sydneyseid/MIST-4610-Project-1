# MIST-4610-Project-1

## Team Name:
Sp24_61608_Group 5

## Team Members:
1. Sydney Seid [@sydneyseid](https://www.github.com/sydneyseid)
2. Albert Sun [@Glockgeta](https://www.github.com/glockgeta)
3. Avanish Thota [@avanish-thota27](https://www.github.com/avanish-thota27)
4. Haley Ford [@HaleyFord](https://www.github.com/Haleyford)
5. Manafie Kabir [@manafiekabir](https://www.github.com/manafiekabir)
6. Nicholas Price [@nickprice347](https://www.github.com/nickprice347)

## Problem Description:
The current scenario involves creating a relational database for a tennis club to ensure all data is properly allocated, and the business runs smoothly and efficiently. The majority of the model is centered around the entity “Members”. Members are at the forefront of the business since they determine which transactions take place, what divisions and leagues to join, what courts to reserve in conjunction with the coaches, which coaching programs to be a part of, and more. In addition to members, the club also employs a variety of general staff employees who can fulfill maintenance requests on various courts. The goal of the model is to accurately use and generate data, show the relationships between the various entities, and allow for queries to promptly be asked and solved to easily allow the analysis of data.

## Data Model:
Explanation of data model:

<img width="675" alt="Screenshot 2024-03-26 at 5 51 03 PM" src="https://github.com/sydneyseid/MIST-4610-Project-1/assets/163012786/1e50319f-7b1b-43bd-8836-84b731bc2026">


*Numbers Match Up With Our Client’s Points*

 
Our model is structured around a tennis club and its various entities are representative of key daily functions. The members entity is
a key aspect of our model, and therefore is present in multiple different relationships. 

1. & 2.

Starting with entities one and two from our client, we created a many to many relationship between members and courts. Members can reserve many courts and courts can have multiple members present on them. The many to many relationship resulted in an associative entity, court reservations. 

3. 
Next, members can belong to many coaching programs and coaching programs have multiple members present in them. These two entities form an associative entity, sessions. Coaching programs and members may also at times have no sessions. 
Additionally, the coaching programs are led by coaches. Coaches have a one to many relationship with coaching programs, as one coach can teach many coaching programs, but a coaching program can only be led by one coach at a time. 
Additionally, the coaches entity has a one to many relationship with the court reservation entity as a coach can make multiple court reservations, but a reservation can only belong to one coach.  

4.
Members can belong to many tennis leagues, and a tennis league is made up of many members. These two entities have a many to many relationship, which results to an associative entity divisions. 

5.
The Pro Shop Inventory entity can belong to many transactions, and the transactions can consist of multiple pro shop items. These two entities resulted in an associative entity, transaction details. Additionally, members can make multiple transactions from the proshop, but a singular transaction can only belong to one member. 

6. & 7.

Our general staff entity can perform maintenance on multiple courts, and each court can have multiple faculty working on its upkeep. Thus an associative entity maintenance request is created to symbolize this many to many relationship. 

<img width="660" alt="finalGroupDM" src="https://github.com/sydneyseid/MIST-4610-Project-1/assets/163012786/8d400012-40f0-47a9-bf03-24ee7d14485d">

## Data Dictionary:

<img width="521" alt="coachingprograms" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/f4a7c03f-5774-4bd5-9c5b-9ebd96393c7f">

<img width="521" alt="coaches" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/ee58d532-33d9-4435-bd41-e2f862629e5a">

<img width="521" alt="courtreservations" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/94e3fae8-699c-4d80-9620-691e7eacaafc">

<img width="521" alt="courts" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/a8437356-5131-4eb3-b04f-35b7fae73bd2">

<img width="521" alt="divisions" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/79abd6de-8f63-4bae-8bdc-af5981993b06">

<img width="521" alt="generalstaff" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/335d16f8-82b8-4aa5-86fa-96f28ab49ac4">

<img width="521" alt="leagues" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/fc90c7f3-d017-4d19-b314-3ccb9d960a0c">

<img width="521" alt="maintenancerequest" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/afed42cc-eb1e-4fe8-9d0c-614261bb46d9">

<img width="521" alt="members" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/cf57082e-c707-49bd-ba90-eba1fa1345f5">

<img width="521" alt="proshopinv" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/9df5c742-d384-44eb-92ff-98724a55ce27">

<img width="521" alt="session" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/cf615fdd-0777-42e3-b9fb-eac4a687d5f3">

<img width="521" alt="transactiondetails" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/dee313f5-5a2a-48ff-bdd4-4ce215c08c3b">

<img width="521" alt="transactions" src="https://github.com/nickprice347/MIST4610-Project-1/assets/163012519/824b9845-0bbe-4329-b5c1-a2008e4a9dbf">



## Queries:
<img width="779" alt="Screenshot 2024-03-26 at 6 21 22 PM" src="https://github.com/sydneyseid/MIST-4610-Project-1/assets/163012786/1d9230b5-cf6d-437f-b41a-1de9d9576a9f">


Query 1 Description:

Query 1 lists the first and last names of the members who have not made any court reservations at the time. 

<img width="663" alt="Screenshot 2024-03-26 at 6 36 02 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/ad2a5f52-f230-4d0b-b8bb-a38f2811dcf1">

Query 1 allows managers to see which members have not reserved a court. This can be beneficial so that managers can inquire about if there is a reason why the member is being inactive, or if they need assistance with the reservation process. This can also be helpful for managers to determine which members they need to be marketing their services to more to increase revenues.


Query 2 Description: 

Query 2 lists the item type, the item brand, and the sum of the quantity ordered to determine the most popular item. The results are ordered by quantity ordered in descending order. 

<img width="789" alt="Screenshot 2024-03-26 at 6 34 58 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/fb23a890-fe87-4530-b375-95c0433642c6">


Managers are keen on identifying which item is the most popular. Understanding which item is in high demand will allow managers to make informed decisions related to inventory management and ensure enough items are in stock for customer demand. 


Query 3 Description: 

Query 3 lists how many coaches are assigned to each age group, and the court locations where they conduct coaching sessions

<img width="854" alt="Screenshot 2024-03-26 at 6 34 16 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/ca0b327b-1124-413b-ba7e-9cdc254e28f8">


Proper resource allocation is critical for a business’s longevity. If there’s a higher demand for coaching sessions from a specific age group, assigning more coaches to said age group would result in improved member experience. Knowing court locations and where coaching sessions are being conducted may minimize conflicts with other club activities, thus having strategic planning over such variables will be useful for analysts to anticipate future demand and make keen decisions. 


Query 4 Description:

Query 4 lists the total transaction value for members whose individual total transaction value exceeds the average total transaction value across all members. 

<img width="838" alt="Screenshot 2024-03-26 at 6 11 26 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/a25ed783-fe07-4ee0-88b3-66d7d8b01f7c">



Contemporary marketing strategies to maximize consumer loyalty and profit earnings place heavy emphasis on marketing toward the most loyal, highest-spending individuals. Such marketing tactics may include personalized promotions, discounts, or incentives that could sway loyal members to spend even more. Cultivating such strong relationships with said members, may attract new members who aspire to receive similar treatment.  








Query 5 Description: 

Query 5 lists the staff members who have more than 1 maintenance request with a “Pending” status. It lists the staff member’s ID, the location of the court, and the total number of “Pending” requests that the staff member has. 

<img width="737" alt="Screenshot 2024-03-26 at 4 39 12 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/fb9599b5-ca96-41b3-bd54-df94f33dee78">


Query 5 allows the manager to see which staff members have “Pending” or uncompleted tasks. This data will show the manager if there are staff members who are not completing their work which is essential for performance reviews, and promotion decisions. This also makes sure that the manager is up to date on what still needs to be completed to ensure the right staff members are spoken to so that jobs are completed effectively and efficiently.


Query 6 Description: 

Query 6 lists the items in the pro shop’s inventory that are the brand Nike. The results are ordered in ascending order of the item price.

<img width="425" alt="Screenshot 2024-03-26 at 4 58 10 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/35134449-5037-4cab-b4b9-8be93ba7570c">


Query 6 shows which items are the brand Nike. This is helpful in that the pro shop staff will be able to track the popularity of the brand and see if the brand should continue to be ordered and in what quantity. Nike is a popular brand and it is important to keep a lot in stock for members.


Query 7 Description: 
Query 7 lists the membership ID, member’s first name, and member’s last name of those who have a balance greater than the average balance of all members and became a member of the club in the year 2018. 

<img width="635" alt="Screenshot 2024-03-26 at 6 13 59 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/3b30941c-eb27-4828-b30b-899e8d19d404">


Query 7 allows management to see the financial behavior of members who joined in 2018 and compare the behavior with members who joined the club in other years. The information is useful in 


Query 8 Description:
Query 8 lists the type of item and the total sales generated by that item in the ProShopInventory.

<img width="807" alt="Screenshot 2024-03-26 at 6 33 01 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/aa7379ef-6095-4285-b485-fd41b3533cee">


Query 8 allows us to see which items are producing the most revenue, and therefore determine profits from that. Managers may use a query like this to determine if items or segments are worth keeping based on their profitability.


Query 9 Description: 

Query 9 counts the number of members per league, including leagues with no members, the league’s ID, and the name of the league, grouped by the league.

<img width="773" alt="Screenshot 2024-03-26 at 6 15 22 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/c2310253-d570-4265-8455-706a5613ffb2">


Query 9 could be useful for management to see what leagues are popular and can make considerations for price changes in accordance to demand. Another use case could be determining allocation of marketing funds based on leagues that would generate the most profit.



Query 10 Description:

Query 10 counts the number of members in each experience level category and groups them accordingly, this is useful for our manager.


<img width="480" alt="Screenshot 2024-03-26 at 6 15 41 PM" src="https://github.com/avanish-thota27/MIST4610GroupProject01/assets/152564332/6547e719-960c-4b7a-9264-2e59c756e53a">


Query 10 could be useful for management to see what staffing needs are by looking at the experience level of members, allowing them to hire coaches that fit the needs of the members. Another use case could be figuring out what kinds of tournaments to host based on the experience level and number of players in each.



## Database Information:

Name of our database: ns_Sp24_61608_Group5

Each query listed above is marked in the database using stored procedures. The procedures can be called using the following format: CALL TP_Qx(); (where ‘x’ is replaced by the query number)


